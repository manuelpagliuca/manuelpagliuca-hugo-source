---
title: CUDA Ray Tracer
summary: Implementation, Comparison and Profiling of GPU and CPU implementation of the same Ray Tracer.
tags:
  - GP-GPU
  - Computer Graphics
date: "2021-06-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Render of the scene that i used for the comparison
  focal_point: Smart

links:

url_code: "https://github.com/manuelpagliuca/Ray-Tracer-CUDA"
url_pdf: "uploads/GPU_COMPUTING___RAY_TRACER.pdf"
url_slides: ""
url_video: ""
url_files: "uploads/GPU_COMPUTING_RENDERS.zip"
# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.

#slides: example
---
GPU Computing Course, July 2021, M.Sc. in Computer Science @UniMi

## About the project
During the course of **GPU Computing** I decided to implement my old version of the Ray Tracer (based on the
*Ray Tracing in One
    Weekend* from {{< staticref "https://raytracing.github.io/books/RayTracingInOneWeekend.html" "newtab">}}Peter Shirley{{< /staticref >}})
    on **CUDA**. In {{< staticref "uploads/GPU_COMPUTING___RAY_TRACER.pdf" "newtab">}}this{{< /staticref >}} paper I compared
the two Ray Tracers underlining the
huge differences in rendering speed (even without achieving the best warp efficiency).<br><br>
For the comparison I used the same scene in both the implementation composed by 8 different spheres with
different
materials between *lambertian*, *metal* and *dielectrics*. I highly recommend to check the comparisons
and metrics at the end of the paper, the GitHub repository is at {{< staticref "https://github.com/manuelpagliuca/Ray-Tracer-CUDA" "newtab">}}this{{< /staticref >}} link if you want to see some
render just download {{< staticref "uploads/GPU_COMPUTING_RENDERS.zip">}}this{{< /staticref >}} zip.
