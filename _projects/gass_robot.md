---
layout: page
title: Gecko Adhesion based Sea Star Crawler Robot
description:
img: assets/img/gass/gass-crawler.png
importance: 3
category: Research
related_publications: 10.3389/frobt.2023.1209202
show: true
---

<h5> Project Abstract </h5>

Over the years, efforts in bioinspired soft robotics have led to mobile systems that emulate features of natural animal locomotion. This includes combining mechanisms from multiple organisms to further improve movement. In this work, we seek to improve locomotion in soft, amphibious robots by combining two independent mechanisms: sea star locomotion gait and gecko adhesion. Specifically, we present a sea star-inspired robot with a gecko-inspired adhesive surface that is able to crawl on a variety of surfaces. It is composed of soft and stretchable elastomer and has five limbs that are powered with pneumatic actuation. The gecko-inspired adhesion provides additional grip on wet and dry surfaces, thus enabling the robot to climb on 25° slopes and hold on statically to 51° slopes.

<div class="display: block; margin-left: auto; margin-right: auto; width: 50%;">
    <center>{% include figure.html path="assets/img/gass/gass-crawler.png" title="GASS Robot" class="img-fluid rounded z-depth-1" %}</center>
</div>
<div class="caption">
The Gecko Adhesion based Sea Star (GASS) Robot.
</div>

<h5> Control Architecture </h5>

In this project, I was responsible for the design and implementation of the control architecture for the robot. The crawling motion of the robot was visualized as the linear combination of five movement vectors corresponding to each limb in the x-y plane.

<p>
    The desired direction of the robot movement determined the magnitude of the movement vector for each limb following the control law:
    \[l_{limb} = l_{max} + cos(\theta_{cmd} - \theta_{limb})\]
    Here, \(l_{limb}\) denotes the magnitude of each limb’s extension where \(limb = 1, ..., 5 \), while \(\theta_{limb}\) he angle of the limb, which is fixed related to the position of the limb in the robot’s body. \(\theta_{cmd}\) denotes the commanded desired direction of movement of the robot, and \(l_{max}\) denotes the maximum magnitude of movement vector, which is a constant determined by the maximum extension for the limbs. This contol equation finally determines the required limb extension for each of the five limbs according to the desired direction of motion for the robot.
</p>

<div class="display: block; margin-left: auto; margin-right: auto; width: 50%;">
    <center>{% include figure.html path="assets/img/gass/gass_control.jpg" title="GASS Robot Control" class="img-fluid rounded z-depth-1" %}</center>
</div>
<div class="caption">
Control Architecture for the GASS robot. <b>(A)</b> Schematic vector diagram of limbs for movement of GASS Robot. <b>(B)</b> The timing diagram for the basic crawling gait. Here, “Ext” and “Con” refer to extension and contraction of soft limbs respectively, and “E” and “DE” refer to engagement and disengagement of the gecko patch with the surface.
</div>

<p>
    Based on the robot’s desired direction of motion, the movement vectors \(l_{limb}\) were calculated for each limb to execute the required motion and the robot followed a basic crawling gait for locomotion. To explain the crawling gait cycle, the limbs in the direction of robot motion and the corresponding gecko adhesion patches were called front limbs and front patches. The remaining limbs and gecko adhesion patches were called rear limbs and rear patches. The crawling gait of the robot involves four motions for each locomotion cycle. In the first phase, the front limbs were extended according to the \(l_{front limb}\) calculated by the controller, and the rear patches were engaged to start the movement. The second phase was the “pull phase”, where the front patches were engaged, rear patches were disengaged, and the front limbs were contracted to pull the robot in the direction of motion. The third phase was the “push phase”, where the front patches were disengaged, rear patches were engaged, and the rear limbs were extended to push the robot in the direction of motion, with a magnitude \(l_{rear limb}\) calculated by the controller. In the fourth phase, the front patches were engaged, the rear patches were disengaged and the rear limbs were contracted, and finally, the front patches were disengaged to end the gait cycle.
</p>

The limbs and the gecko adhesion patches were operated in a sequential manner, as mentioned above, by an open-loop controller code, such that the motion of the front limbs and rear limbs does not affect each other during the gait cycle. Since the control strategy was open-loop, it did not account for the different behaviour of the limbs of the soft robot, even if the commanded input was the same or for any deviation that occurred during the robot’s motion.

<div class="display: block; margin-left: auto; margin-right: auto; width: 50%;">
    <center>{% include figure.html path="assets/img/gass/gass_control2.jpg" title="GASS Robot Control" class="img-fluid rounded z-depth-1" %}</center>
</div>
<div class="caption">
<b>(A)</b> Schematic of GASS robot. <b>(B)</b> Disengaged (left) and engaged (right) position of the gecko patch on the robot foot. <b>(C)</b> States of linear actuators. <b>(D)</b> Sequence of GASS robot motion phases for one cycle of motion.
</div>