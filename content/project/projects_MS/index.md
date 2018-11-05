+++
title = "MS project, Mechatronics of a Humanoid Robot Nino"
date = 2018-11-04T13:20:17-06:00
draft = false

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = []

# Project summary to display on homepage.
summary = "My MS's main project: design the bipedal mechanim and the eletronics of a human-sized humanoid robot."

# Slides (optional).
#   Associate this page with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references 
#   `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides = "content/post/bipedal_robot_development/index.md"

# Optional external URL for project (replaces project detail page).
external_link = ""

# Links (optional).
url_pdf = ""
url_code = ""
url_dataset = ""
url_project = "https://sites.google.com/site/slongzchao/research-and-projects/graduate-works/developments-and-designs-for-a-biped-mechanism-of-a-humanoid-robot-and-mobile-robots"
url_slides = ""
url_video = ""
url_poster = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
url_custom = [{icon_pack = "fab", name="News", url = "https://spectrum.ieee.org/automaton/robotics/humanoids/ntu-taiwan-humanoid-sign-language"}]

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""
  
[[gallery_item]]
album = "1"
image = "mechanism_evolution.jpg"
caption = "Design evolutions"
    
[[gallery_item]]
album = "1"
image = "mechanism_designed.jpg"
caption = "The highlight mechanisms designed by Ken"
  
+++

In my second year of MS study, my main task is to build the bipedal mechanism for a human-sized humanoid robot (which called Nino later on) from a prototype design within a year (so that it can match my graduation plan). Since there was no human-sized bipedal robot has been successfully built in our lab before, it was a chanllenging task at that moment. With a carefully-planned scheulde, the efficient executaion, and the great team work, we managed to built the bipedal robot and tested the ZMP-based walking on it.

## Mechanism design of the biped mechanism with trunk
{{< gallery album="1" >}}
As shown in the figure above, I mainly designed the thigh and torso mechanisms. My main responsibilities of mechanism design include:

1. The complete mechanism design (SolidWorks).
2. Performed FEA analysis (CATIA and SolidWorks) with different mechanism groups to optimize the strucutre (as shown below).
3. Checked the design with walking simulation.
4. Chose proper mechanical components (bearings, timly belts/pullies, harmonic drives and motors) to meet the requirements (from simulation).
5. Generated CAD drawings, exploded views and documentations for mechanism fabrication and assembly.

{{< figure src="mechanism_fea.jpg"  >}}

## Electronics development of the biped robot
We used the distributed control system (with CAN Bus with USB) through the bipedal mechanism (as shown below). My mentor - Jiu-Lou Yan deisnged the main PCB boards for motor control, and I assisted him to solder and test those control boards and the firmware/software integration to complete the control system.
My main responsibilities of mechanism design include:

1. Soldered the motor control board (motor driver with MCU), test it with torso mechanism to confirm its quality.
2. Arranged the wiring of the entier bipedal mechanism and trouble-shoot.
3. Wrote the firmare of the MCU (in motor control board) for the (joint) homing mode with proximity sensor.
4. Designed the PCB for CAN Bus to USB adapter.
5. Wrote the firmare of the MCU for the CAN Bus to USB adapter.

{{< figure src="electronics.jpg"  >}}
