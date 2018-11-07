+++
title = "MathWorks, Safe trajectory tracking using Sawyer"
date = 2018-11-04T12:26:41-06:00
draft = false

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["Contact Control", "Experiment"]

# Project summary to display on homepage.
summary = "This is the project I contributed as a feature example in Robotics System Toolbox (RST) for MATLAB 2018a."
# Slides (optional).
#   Associate this page with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references 
#   `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides = ""

# Optional external URL for project (replaces project detail page).
external_link = ""

# Links (optional).
url_pdf = ""
url_code = ""
url_dataset = ""
url_project = "https://www.mathworks.com/help/robotics/examples/perform-safe-trajectory-tracking.html"
url_slides = ""
url_video = ""
url_poster = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{icon_pack = "fab", icon="twitter", name="Follow", url = "https://twitter.com"}]
url_custom = [{name="Extended Video", url = "https://youtu.be/q4mIAX-Rcmg"}]
# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""

+++
This is my last project at MathWorks Robotics Team (who develops the [Robotics System Toolbox (RST)](https://www.mathworks.com/products/robotics.html)).
Inspired by [Haddadin's famous demo](https://youtu.be/dnUwqngH0bM), the idea is to demonstrate manipulator algorithms in RST for the safe robot-environment interaction to a ROS-enabled robot. In this project I implemented [Haddadin's time scaling method](https://ieeexplore.ieee.org/document/4650764) to achieve safe trajectory tracking on the Sawyer from Rethink Robotics. The purpose of this project is threefold:

1. Contributed an simulation in Simulink with Simscape Multibody to showcase the usage of Robotics Manipulator Blocks.
2. Using RST to test different APIs with the experiments on Sawyer through Robot Operating System (ROS), including the MATLAB code with ROS functions, the Simulink implementation with ROS blocks, and C++ code generated the from Simulink as a ROS node that can directly run on Sawyer.
3. As part of the demonstrations presented in an annual company-wise event.

In the Simulink example, I also implemented a simple contact model (as a spring damper system) to simulate the interaction between the end-effector of the Sawyer and the environment.
The extended (marketing) video adapted from this project has been posted on [MATLAB Facebook page](https://www.facebook.com/MATLAB/videos/325771224655005/?__xts__[0]=68.ARDt0ptLsgfVkzCU3V7-uwTiwfc_D3clLJzEuxHzvDAzO48f4UYHd6cUfQv5DxGmaEnhHdnUXYY38WsYs6AJutGi_037CT8Gd41HSJIoXe5yBlkkxleZ3HaImMZs7ji7tsQBEY2UnGSdRuVQuUr7vJEocX3WOpY7K5-S-dPT2mLGtpwr2Dhu&__tn__=-R) since this September and currently got 15k views!