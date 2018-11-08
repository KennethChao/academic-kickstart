+++
title = "PhD project, QP-based Controller to Unify COM Planning and Torque Control"
date = 2018-11-02T17:02:41-06:00
draft = false
math = true

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["Optimal Control"]

# Project summary to display on homepage.
summary = "A method of combining real-time walking pattern generation and constrained nonlinear control to achieve robotic walking under Zero-Moment Point (ZMP) constraints."

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
url_project = ""
url_slides = "https://docs.google.com/presentation/d/12TdJH6Q65cA29AywosrSKkaVhY2FmexZOyymU0W1-l4/edit?usp=sharing"
url_video = ""
url_poster = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{icon_pack = "fab", icon="twitter", name="Follow", url = "https://twitter.com"}]
# url_custom = [{name="Preprint", url = "../../files/preprint_qp.pdf"}]

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""
+++
In this work we designed a QP-based controller combining real-time walking pattern generation and constrained nonlinear control to achieve robotic walking under Zero-Moment Point (ZMP) and torque constraints. 

This method utilize the fact that existing solutions to both walking pattern generation and constrained nonlinear control (summarized in the following table) have been independently constructed as Quadratic Programs (QPs, as shown below) and that these constructions can be related through an equality constraint on the instantaneous acceleration of the center of mass (COM). 

{{< figure src="CLFQP.jpg" title="The QP of constrained nonlinear control." >}}

{{< figure src="MPCQP.jpg" title="The QP of COM planning (in the form of MPC) with linear inverted pendulum (LIP)." >}}


| Controller                    | Walking Pattern Generation     | QP controller with RES-CLF     |
| ------------------------------| ------------------------------ | ------------------------------ |
| Purpose                       | COM planning for LIP			 | Tracking control for nonlinear system					      |
| Pros                          | ZMP constraints over the horizon  | instantaneous ZMP, torque, and CLF constraints for nonlinear dynamics						  |
| Cons                          | The LIP might not reflect the nonlinear dyanmics | The ZMP constraints over the horizon cannot be guaranteed

To summarize, this unified controller (as shown below) solves a single Quadratic Program which incorporates elements from Model Predictive Control (MPC) based center of mass planning and from rapidly exponentially stabilizing control Lyapunov function (RES-CLF). The resulting QP-based controller simultaneously solves for a COM trajectory that satisﬁes ZMP constraints over a future horizon while also producing joint torques consistent with instantaneous acceleration, torque, ZMP and RES-CLF constraints.

{{< figure src="UniQP.jpg" title="The unified framework as single QP." >}}