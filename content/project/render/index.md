---
title: Deferred renderer
summary: Implementation of deferred rendering technique in Vulkan
tags:
  - Computer Graphics
  - Misc
date: "2021-06-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Normals of the basic scene
  focal_point: Smart

links:

url_code: "https://github.com/manuelpagliuca/Vulkan-Deferred-Renderer"
url_pdf: "uploads/DEFERRED_RENDERING___RTGP.pdf"
url_slides: ""
url_video: "https://www.youtube.com/watch?v=V7PxEpzkY1c"
# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.

#slides: example
---
Real-Time Graphics Programming Course, July 2021, M.Sc. in Computer Science @UniMi

## About the project
This was a project I made for the course of Real-time Graphics Programming. The course provided extensive knowledge about real-time computer graphics. (You can check the {{< staticref "uploads/Appunti_RTGP.pdf" "newtab" >}}notes{{< /staticref >}} I took.) At the end of the course, in addition to an oral exam, there was a project related to graphic programming to be developed with OpenGL. I asked Prof. Gadia if there was the possibility of developing it with Vulkan, he granted me the possibility to take this extra-step, it was very tiring but fruitful from the point of view of learning.

The project consists in a deferred renderer to improve the overall efficiency of the application in the usage of lights. The scene is composed of three models of the same character, a floor and twenty lights (whose movement and color can be modified), there is the {{< staticref "uploads/DEFERRED_RENDERING___RTGP.pdf" "newtab" >}}notes{{< /staticref >}} containing the various metrics obtained using a different number of lights. The GitHub repository is accessible at {{< staticref "https://github.com/manuelpagliuca/Vulkan-Deferred-Renderer" "newtab" >}}this{{< /staticref >}} link.

