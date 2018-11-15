+++
title = "PhD project, Bipedal walking on various terrains towards to human-like motions"
date = 2018-11-05T15:09:22-06:00
draft = false

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["Optimal Control"]

# Project summary to display on homepage.
summary = "The recent work of walking motion generation on various terrains (stairs and slopes) using hybrid trajectory optimization."

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
url_slides = "https://docs.google.com/presentation/d/1QBZAclL6Vy0BMRYatpN--DuODKhMf3h4lkZVD6jbZyw/edit?usp=sharing"
url_video = ""
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
In this project, I implemented the hybrid trajectory optimization and explore the walking generation on different terrains. As shown in the following figure, the optimization formulation contains modulaized constraints, so that it will be easier to customize different combinations of constraints.
The current visualization results are rendered with SimScape Multi-Body as shown in the following videos (More videos of slope and stair walking are in preparation):

{{< figure src="opt.jpg" title="The overall opt formulation">}}

Normal walking (flat-terrain):
{{< video src="AMBER3_Visual_Walking.mp4" controls="yes" >}}

Normal walking (flat-terrain) with a different view angle:
{{< video src="AMBER3_Visual_Walking_Ground.mp4" controls="yes" >}}

Down-slope (0.1 radian) walking:
{{< video src="AMBER3_Visual_Walking_Ground_DS01.mp4" controls="yes" >}}

Down-slope (0.2 radian) walking with smaller range of torso sawying behaves more cautiouly.
{{< video src="AMBER3_Visual_Walking_Ground_DS02_Small_TorsoAngle.mp4" controls="yes" >}}