+++
title = "PhD project, Walking with foot rolling motion on various terrains"
date = 2018-11-05T15:09:22-06:00
draft = false

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["Optimal Control", "Experiment"]

# Project summary to display on homepage.
summary = "By genealizing the contact constraints, we extended HZD gait optimization to generate walking motion on flat ground, stairs and slopes."

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
url_slides = ""
url_video = "https://youtu.be/wYKrLmk7nRY"
url_poster = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{icon_pack = "fab", icon="twitter", name="Follow", url = "https://twitter.com"}]

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""
  
  # Down-slope (0.3 radian) walking:
  # {{< video src="AMBER3_Visual_Walking_Ground_DS03.mp4" controls="yes" >}}
  # Up-slope (0.3 radian) walking:
  # {{< video src="AMBER3_Visual_Walking_Ground_US03.mp4" controls="yes" >}}
+++
In this project, I implemented the hybrid zero dynamics (HZD) gait optimization and explore the walking generation on different terrains. As shown in the following figure, the optimization formulation contains modulaized constraints, so that it will be easier to customize for different contact sequence.

{{< figure src="opt.jpg" title="The overall opt formulation">}}
The following videos show the visualizations of optimization results (which are rendered with Simulink and SimScape Multi-Body), and current experiment results as the validations:

{{< youtube wYKrLmk7nRY >}}



A set of walking motion comparison between optimization results and human walking is compared in this video, where the similar trends and the differences are highlighted and discussed.

{{< youtube vQxLmPpmtMA >}}
