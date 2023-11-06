---
layout: page
title: Waste Pile Rearrangement
description: Rearranging waste piles for Robotic Waste Sorting in Recycling Facilities
img: assets/img/waste_pile_rearragement/cross_pile.gif
importance: 5
category: Research
related_publications:
show: true
---

Project conducted at the MER Lab, Worcester Polytechnic Institute, under the guidance of <a href="https://www.wpi.edu/people/faculty/bcalli">Prof. Berk Calli</a>.

<h5> Project Abstract </h5>

This innovative approach seeks to address key challenges within the recycling industry by leveraging robotic technology. The primary focus is on optimizing waste sorting processes, specifically the categorization of materials such as plastics, paper, metal, glass, and non-recyclables. The system incorporates advanced robotic manipulation and object classification techniques, enabling robots to effectively operate within cluttered materials recovery facilities (MRFs).

The primary objective of this research is to develop a secure human-robot collaboration framework that enhances operational efficiency and profitability while also prioritizing the safety and job satisfaction of MRF workers. The project implements a conveyor system integrated with robots to facilitate waste recognition and picking experiments. Notably, the gripper design is tailored to enable efficient waste picking, regardless of potential damage to the target items. This approach holds promise for transforming the recycling industry, making it more environmentally sustainable and improving working conditions for laborers.

<div class="display: block; margin-left: auto; margin-right: auto; width: 50%;">
    <center>{% include figure.html path="assets/img/waste_pile_rearragement/conveyer_setup.png" title="Robotic Waste Sorting Setup at MER Lab" class="img-fluid rounded z-depth-1" %}</center>
</div>
<div class="caption">
    The Robotic Waste Sorting setup at MER Lab, WPI. The setup consists of a conveyor belt, integrated with systems used for waste recognition and picking.
</div>

<h5> Waste Pile Rearrangement </h5>

In this project, I am working on developing a novel approach for rearranging waste piles to facilitate robotic waste sorting. Specifically, I am using depth images and point clouds to effectively reconfigure waste piles on a conveyor belt using a robotic manipulator in order to uncover occluded and completely covered objects in the waste stream. The entire waste rearrangement pipeline is implemented in ROS and Python. The simulation is performed in Unity.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/waste_pile_rearragement/sim_env.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/waste_pile_rearragement/node_graph.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    ROS pipeline for Waste Pile Rearrangement. <b>Left:</b> Simulation environment in Unity. We use a UR3e robot with an end plate to simulate rearrangement of the waste pile. <b>Right:</b> ROS node graph for the Waste Pile Rearrangement pipeline.
</div>

We formulate the pile rearrangement task as a pile flattening problem - the goal is to flatten the pile such that majority of the pile objects are visible to the robot. The current objectives are to perform the pile flattening ina a single action on a stationary pile. We use a UR3e robot with an end plate to simulate rearrangement as sweeping through the waste pile. An overhead RGB-D camera is used to collect depth images of the pile in front of the robot. The depth images are processed to obtain a point cloud of the pile. The point cloud is then used to compute the best sweeping direction as a 3D straight line trajectory. The robot then sweeps through the pile in the computed direction.

<!-- TODO: add current results and images -->

<p style="text-align: center;"><em> This project is still under development. More details and results will be updated soon. </em></p>