---
layout: page
title: RoboTRAC - Autonomous Vascular Access Robot
description: Robot to get autonomous vascular access for trauma care in resource-limited settings
img: assets/img/tracir/tracir.png
importance: 4
category: Research
related_publications: 10160651
show: true
---

Project conducted at the Biorobotics Lab, Carnegie Mellon University, under the guidance of <a href="https://www.ri.cmu.edu/ri-faculty/howie-choset/">Prof. Howie Choset</a> and <a href="https://www.ri.cmu.edu/ri-faculty/john-galeotti/">Prof. John Galeotti</a>.

---

<h5> Project Abstract </h5>

Ensuring timely and effective vascular access is critical for the survival of trauma patients. Vascular access serves as a vital route for delivering anesthesia, resuscitative fluids, diagnostic contrast, and monitoring physiological parameters during primary resuscitation. This is particularly crucial in cases of severe trauma where hemorrhaging is a leading cause of early death, necessitating rapid intervention to replace lost blood volume and treat coagulopathy. Central venous lines play a crucial role in large-volume resuscitation by facilitating the rapid administration of significant quantities of fluids and medications, which may be impractical through peripheral veins. In addition, the integration of robot-guided catheter insertion has the potential to provide essential medical care quickly, especially in situations where medical personnel are not readily available, further emphasizing the importance of timely access to vascular intervention in trauma cases.


<div class="display: block; margin-left: auto; margin-right: auto; width: 50%;">
    <center>{% include figure.html path="assets/img/tracir/tracir.png" title="TRACIR Robot" class="img-fluid rounded z-depth-1" width=400 %}</center>
</div>
<div class="caption">
    The RoboTRAC Robot: a linear array ultrasound transducer attached to the end-effector of a 6-DoF Universal Robots UR3e serial manipulator, along with an in-house developed autonomous needle insertion mechanism.
</div>

<h5> Segmentation of Ultrasound Images </h5>

In this project, I conducted comparison studies for segmentation of ultrasound images using multiple deep learning frameworks. The frameworks I studied include: 2D U-Net for Image Segmentation, YOLO for Vessel Detection, YOLO + Spokes Ellipse Algorithm for Vessel Segmentation in YOLO detection boxes. To perform these comaprison studies, I curated a dataset consisting of over 14,000 ultrasound images, taken from around 13 porcine experiments. The network performance metric used was IoU score. I compared all these methods for both, single-class segmentation (vessels) and multi-class segmentation (arteries and veins). Here are some of the results that I collected:

<!-- U-Net -->
<div class="display: block; margin-left: auto; margin-right: auto; width: 50%;">
    <center>{% include figure.html path="assets/img/tracir/tracir_unet.svg" title="2D U-Net" class="img-fluid rounded z-depth-1" %}</center>
</div>
<div class="caption">
    2D Vanilla U-Net for Vessel Segmentation, with results and IoU scores for single class and multi class segmentation.
</div>

<!-- YOLO -->
<div class="display: block; margin-left: auto; margin-right: auto; width: 50%;">
    <center>{% include figure.html path="assets/img/tracir/tracir_yolo.svg" title="YOLO v3-tiny" class="img-fluid rounded z-depth-1" %}</center>
</div>
<div class="caption">
    YOLO v3-tiny for Vessel Detection, with results and IoU scores for single class and multi class segmentation.
</div>

<!-- YOLO + Spokes Ellipse Flow -->
<div class="display: block; margin-left: auto; margin-right: auto; width: 50%;">
    <center>{% include figure.html path="assets/img/tracir/tracir_yoloflow.svg" title="YOLO + Spokes Ellipse Algorithm" class="img-fluid rounded z-depth-1" %}</center>
</div>
<div class="caption">
    The YOLO + Spokes Ellipse Fitting Algorithm for vessel segmentation. This was introduced by Brattain, Laura J et al. “AI-Enabled, Ultrasound-Guided Handheld Robotic Device for Femoral Vascular Access.” (Biosensors, 2021) from MIT Lincoln Labs.
</div>

<!-- Spokes Ellipse -->
<div class="display: block; margin-left: auto; margin-right: auto; width: 50%;">
    <center>{% include figure.html path="assets/img/tracir/tracir_spokesellipse.svg" title="Spokes Ellipse Fitting Algorithm" class="img-fluid rounded z-depth-1" %}</center>
</div>
<div class="caption">
    The Spokes Ellipse Fitting Algorithm. The algorithm works by generating multiple spokes from a seed point, like the spokes of a wheel. The length of the spokes is determined by the change in the intensity in the image. The algorithm then fits an ellipse to the spokes, which is the final segmentation.
</div>

<!-- YOLO + Spokes Ellipse Flow -->
<div class="display: block; margin-left: auto; margin-right: auto; width: 50%;">
    <center>{% include figure.html path="assets/img/tracir/tracir_yolospokes.svg" title="YOLO + Spokes Ellipse Algorithm Results" class="img-fluid rounded z-depth-1" %}</center>
</div>
<div class="caption">
    Results of the YOLO + Spokes Ellipse Fitting Algorithm for vessel segmentation.
</div>


<!-- TODO: Add volume reconstruction -->
<!-- <h5> 3D Volume Reconstruction </h5> -->
