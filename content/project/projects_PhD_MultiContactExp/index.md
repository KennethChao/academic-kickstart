+++
title = "PhD project, Towards to human-like walking gait"
date = 2018-11-03T15:09:15-06:00
draft = false

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["Optimal Control", "Experiment"]

# Project summary to display on homepage.
summary = "In this project we modified the trajectory optimization thorugh contact, and added several schemes to adjust the gait to be more human-like."

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
url_slides = "https://docs.google.com/presentation/d/18OSoZUJWWeYjSfg0VlNfK2zQoQqfuqTBjJZmfM3Wbr8/edit?usp=sharing"
url_video = "https://youtu.be/4QS9QBgkGrQ"
url_poster = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{icon_pack = "fab", icon="twitter", name="Follow", url = "https://twitter.com"}]
url_custom = [{name="Preprint", url = "../../files/preprint_opt_through_contact.pdf"}]
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
	image = "SACC.gif"
	caption = "Walking gait with SACC constraint"
    
[[gallery_item]]
	album = "1"
	image = "NSCC.gif"
	caption = "Walking gait with NSCC constraint"
	
[[gallery_item]]
	album = "2"
	image = "fc.gif"
	caption = "Walking gait with SACC constraints after the kinematic optimization"	
+++
This is a project using **_trajectory optimization with direct collocation framework_**. The objective is to generate multi-domain walking for bipedal robot AMBER 3. Modified from [Michael Posa's Trajectory Optimization through Contact](http://journals.sagepub.com/doi/abs/10.1177/0278364913506757), we used the Hermite-Simpson transcription to improve the dynamic accruacy for the collocation points approximated as the nodes on cubic splines. In this work we also compared the optimization results with three different contact constraints:

* Sliding allowed contact constraints (SACC, right animation below)
* Non-sliding contact constraints (NSCC, left animation below)
* NSCC with one-sided spring constraints (OSS)

where different styles of walking gaits can be generated with different constraints.
{{< gallery album="1" >}}

The cost and the double support ratio of those three constraints are shown below, where the optimization result of OSS is probably premature because the additional complementary constraints to describe one-sided springs complicate the original formulation more.

| Constraints                   | SACC                           | NSCC               		      |OSS
| ------------------------------| ------------------------------ | ------------------------------ |------------------------------ |
| Cost of transport             | 0.048         				 | 0.049					      |2.664
| Double support percentage     | 31.37%                     	 |35.48%						  |35.48%



In addition, towards to generate human-like motion, we added several schemes:

* Virtual springs on ankles to adjust the foot-rolling motion (e.g. adjust the gait to have clearer toe-off or heel-strike motions) and a aditional penalty cost to limit the activation of springs.
* An kinematic optimization as post-processing to increase the foot clearance as shown below:
{{< gallery album="2" >}}

The experiment is still undergoing, but the current result has shown the capability of bipedal locomotion towards to a more human-like movement:
{{< youtube 4QS9QBgkGrQ >}}
