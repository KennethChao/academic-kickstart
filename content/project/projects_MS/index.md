+++
title = "MS project, Mechatronics of a Humanoid Robot Nino"
date = 2018-11-02T13:20:17-06:00
draft = false

#ToDo: Change Project Link


# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["Experiment"]

# Project summary to display on homepage.
summary = "My MS's main project: design the bipedal mechanism and the electronics of a human-sized humanoid robot."

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
url_project = ""
url_slides = ""
url_video = "https://youtu.be/RYdu1ux4G_I?t=74"
url_poster = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
#url_custom = [{icon_pack = "fab", name="News", url = "https://spectrum.ieee.org/automaton/robotics/humanoids/ntu-taiwan-humanoid-sign-language"}]
#url_custom = [{name="IEEE Specturm", url = "https://spectrum.ieee.org/automaton/robotics/humanoids/ntu-taiwan-humanoid-sign-language"}]

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
  
[[gallery_item]]
album = "2"
image = "biped_robot_design1.jpg"
caption = "Mechanism design for large range of motion and circuit board housing"
    
[[gallery_item]]
album = "2"
image = "biped_robot_design2.jpg"
caption = "The actual integration of mechanism with electronics"  
+++

In my second year of MS study, my main research objective is to build the bipedal mechanism for a human-sized humanoid robot (which called Nino later on) from a prototype design and run the developed ZMP-based walking on it. Since there was no human-sized bipedal robot has been successfully built in our lab before, it was a challenging task at that moment. one year later, with a well-planned schedule, the efficient execution, and the great team work, we managed to built the bipedal robot and the ZMP-based walking was successfully tested.

## Mechanism design of the biped mechanism with trunk
{{< gallery album="1" >}}
As shown in the figure (the highligt parts) above, I mainly designed the thigh and torso mechanisms. My main responsibilities of mechanism design include:

1. The mechanism design (SolidWorks).
2. Performed FEA analysis (CATIA and SolidWorks) with different mechanism groups to optimize the structure (as shown below).
3. Checked the design with walking simulation.
4. Chose proper mechanical components (bearings, timely belts/pulleys, harmonic drives and motors) to meet the requirements (from simulation).
5. Generated CAD drawings, exploded views and documentations for mechanism fabrication and assembly.

{{< figure src="mechanism_fea.jpg">}}

## Electronics development of the biped robot
{{< figure src="electronics.jpg"  >}}
We used the distributed control system (with CAN Bus and USB) for the bipedal mechanism (as shown above). My mentor - Jiu-Lou Yan designed the main PCB boards for motor control, and I assisted him to solder those control boards, tested them and integrated the firmware/software to complete the entire system.
My main responsibilities of the development of eletronics  include:

1. Soldered the control boards (motor driver with MCU) with motor testing.
2. Arranged the wiring of the eletronics and trouble-shoot (as shown below).
3. Wrote the firmware of the MCU (in control board) for the (joint) homing.
4. Designed the PCB for CAN Bus to USB adapter, and wrote its firmware.

{{< gallery album="2" >}}

