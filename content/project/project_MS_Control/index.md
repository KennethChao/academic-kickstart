+++
title = "MS project, Walking Control under Step Height Uncertainty"
date = 2018-11-01T00:35:59-06:00
draft = false

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["Contact Control"]

# Project summary to display on homepage.
summary = "The walking controller I developed to adapt step hieght uncertainty with 6-axis force sensor, assumed without the knowledge of the terrain profile."

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
url_video = "https://youtu.be/8SCTs2_kofE"
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
+++

This controller was degined to adapt uncertained step height. Two controllers are applied in different levels (as shown in the following figure):

1. The ladning modification (triggered by impulse detection) determines the updated level height, holds the landing foot position, and switchs the state machine to double support when the impact occurs.
2. Due to the impact, the flat contacts on both feet might break (which is not desired in double support). In this case, the ankle stabilizer adjusts the ankle orientations based on a simplified model to restore the flat contacts.
{{< figure src="1" src="GC.jpg">}}

In the following simulation, the upper body motion is controlled to cancel the  momentum about the vertical axis induced by the lower body movement, to mitigate the slipping in the walking simulation.
{{< youtube 8SCTs2_kofE >}}