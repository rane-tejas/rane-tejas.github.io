---
layout: defaults/page
permalink: about.html
narrow: true
title: About Me
images:
  - https://images.unsplash.com/photo-1421789665209-c9b2a435e3dc?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=5b1016b885e7438c4633109d77368d4d&auto=format&fit=crop&w=1651&q=80
  - https://images.unsplash.com/photo-1476514525535-07fb3b4ae5f1?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=468a8c18f5d811cf03c654b653b5089e&auto=format&fit=crop&w=1650&q=80
  - https://images.unsplash.com/photo-1504626835342-6b01071d182e?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=975855d515c9d56352ee3bfe74287f2b&auto=format&fit=crop&w=1651&q=80
---

## Biography

{% include components/intro.md %}

I have contributed majorly in numerous projects across the numerous facets of Robotics. But I am primarily interested in the fields of Modular Robotics and Bio-inspired Robotics. With the advancements in the fields of Mechatronics and Artificial Intelligence, many institutes have created robotic platforms which mimic living beings closely. On integrating this with Modularity, the result is a fascinating system whose abilities can be altered to suit the demands of the environment. Such systems can operate seamlessly without any boundaries whatsoever. They can also perform collaborative tasks with human beings and enhance our efficiency. These are the types of systems that I wish to work on and advance further.

Being interested in designing mechanisms and thinking of efficient ways to manufacture them, I joined the Mechanical Engineering program at BITS Pilani, Goa Campus in August, 2017. From the very beginning, I have been an integral part of the technical clubs on campus, like the Electronics and Robotics Club (link) and the Aerodynamics Club (link). I worked on a variety of projects with these clubs, to finally find my interests in Bio-inspired Robotics and Biomimetic Systems. Working on projects with professors and my fellow colleagues gave me a lot of hands-on experience. It also introduced me to other aspects of Robotics like Control Systems, Software Development, Reinforcement Learning, and basic Electronic Systems. 

As of now, I have extensive experience working with CAD/CAM software like SolidWorks and Fusion 360, and with programming languages like MATLAB and Python. In my free time, I work on implementation of Reinforcement Learning algorithms and building custom environments. I am also proficient with equipment like 3D Printers and Laser Cutters.

Apart from learning about new technologies, I like cycling and traveling to new places. I am a huge Formula 1 fan, and I also enjoy gaming as a pass time.

<hr />

## Professional Experience

<div class="card mb-4" style="width: 100;">
    <div class="card-body">
        <h4 class="card-title mb-2">
             Robert Bosch Centre for Cyber-Physical Systems, IISc Bangalore 
        </h4>
        <h6 class="card-subtitle mb-2 text-secondary">
            June 2020 - Present
        </h6>
        <div class="card-text mb-0">
            Research Intern
        </div>
    </div>
</div>

<div class="card mb-4" style="width: 100;">
    <div class="card-body">
        <h4 class="card-title mb-2">
            Department of Mechanical Engineering, BITS Pilani 
        </h4>
        <h6 class="card-subtitle mb-2 text-secondary">
            January 2020 - Present
        </h6>
        <div class="card-text mb-0">
            Academic Research Assistant
        </div>
    </div>
</div>

<div class="card mb-4" style="width: 100;">
    <div class="card-body">
        <h4 class="card-title mb-2">
            Department of Electrical and Electronics Engineering, BITS Pilani 
        </h4>
        <h6 class="card-subtitle mb-2 text-secondary">
            January 2019 - December 2019
        </h6>
        <div class="card-text mb-0">
            Academic Research Assistant
        </div>
    </div>
</div>

<div class="card mb-4" style="width: 100;">
    <div class="card-body">
        <h4 class="card-title mb-2">
            UltraTech Cement, Aditya Cement Works, Shambhupura 
        </h4>
        <h6 class="card-subtitle mb-2 text-secondary">
            May 2019 - July 2019
        </h6>
        <div class="card-text mb-0">
            Summer Intern, Mechanical 1 Department
        </div>
    </div>
</div>

<hr />

## Technical Skills

<div class="row">
  <div class="col-sm-6">
    <div class="card mb-2">
      <div class="card-body">
        <h5 class="card-title">CAD/CAM Software</h5>
        <p class="card-text">SolidWorks, Autodesk Fusion 360, AutoCAD, PTC Creo</p>
      </div>
    </div>
  </div>
  <div class="col-sm-6">
    <div class="card mb-2">
      <div class="card-body">
        <h5 class="card-title">Simulation Software</h5>
        <p class="card-text">SolidWorks Simulations, ANSYS APDL, AutoDesk Flow Design</p>
      </div>
    </div>
  </div>
</div>
<div class="row">
  <div class="col-sm-6">
    <div class="card mb-2">
      <div class="card-body">
        <h5 class="card-title">Programmimg Skills</h5>
        <p class="card-text">Python, ROS, MATLAB, C++</p>
      </div>
    </div>
  </div>
  <div class="col-sm-6">
    <div class="card mb-2">
      <div class="card-body">
        <h5 class="card-title">Equipment</h5>
        <p class="card-text">3D Printers, CNC Laser Cutter</p>
      </div>
    </div>
  </div>
</div>

<hr />

## Achievements

- Secured Second Place in the Alumni Relations Cell (BITS Pilani) Research Scholarship, 2019 for the paper titled: 3DoBot - A modular robot for wheel and chain coordinate structures

<hr />

<div id="carouselExampleControls" class="carousel slide mb-4" data-ride="carousel">
    <div class="carousel-inner">
        {% for img in page.images %}
            <div class="carousel-item {% if forloop.first %}active{% endif %}">
                <img src="{{ img }}" class="d-block w-100" alt="">
            </div>
        {% endfor %}
    </div>
    <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
    </a>
    <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
    </a>
</div>

The images are from various projects done with Electronics and Robotics Club and the Aerodynamics Club.