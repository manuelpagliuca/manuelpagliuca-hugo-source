---
title: Efficient representations of high‑resolution polygonal surfaces, adding anisotropy control to the Micro‑Mesh schema
summary: My Master's Thesis argument
tags:
  - Computer Graphics
  - Math
  - Geometry Processing
date: "2023-10-25T09:42:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption:
  focal_point: Smart

links:

url_code: "https://github.com/manuelpagliuca/anisotropic-micromesh"
# url_pdf: "uploads/MANUEL_PAGLIUCA_ANISOTROPIC_MM_Master_s_Thesis__Integral_.pdf"
url_slides: "uploads/Slides_Master.pdf"
url_video: ""
# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.

#slides: example
---
Master's Thesis, October 2023, M.Sc. in Computer Science @UniMI

![](dragon_render.png)

### [Abstract](/uploads/Abstract_Master_s_Thesis__en_.pdf)

This [thesis](/uploads/MANUEL_PAGLIUCA_ANISOTROPIC_MM_Master_s_Thesis__Integral_.pdf) aims to empirically investigate the imaginable performance for data structures suitable for effectively representing extreme-resolution 3D polygonal surfaces designed for multi-resolution rendering on GPUs.

To this end, supporting algorithms will be designed, implemented, and tested that transform "traditional" (i.e., indexed) high-resolution triangular meshes into the analyzed data structures, and then measure the approximation errors introduced through appropriate geometric measurements.

Other alternative schemes will be studied, which are considered variants of the so-called "micro-meshes" scheme offered by the latest generation of vendor-specific GPU hardware. These data structures are characterized by the use of a semi-regular subdivision of a medium-resolution "base mesh," followed by displacement of the generated vertices. Variants introduced may include the adoption of an anisotropic subdivision step, the adoption of an irregular recursive subdivision scheme, or others.

## Dependencies

* [Qt](https://www.qt.io/)
* [OpenGL Mathematics](https://glm.g-truc.net/0.9.9/index.html)
  * The headers are placed in the directory `Dependencies\GLM`
* [PyMeshLab](https://pymeshlab.readthedocs.io/en/latest/installation.html)

## Sample models

As sample models in this repository, I've prepared different versions of [Pallas Cat](https://free3d.com/3d-model/pallas-cat-v1--576987.html) by *printable_models*

## Python script (empirical analysis)

Executing this script will generate **n** samples for both subdivision schemes (current and variant). A table (as a text file) containing the face quality values (according to the inradius/circumradius metric) will be built for both batches of samples.

The table will be ordered by a factor **F** used, this will allow the comparison of one sample of a table with a sample of the other table, the factor modulates the intensity of subdivisions.

In the [thesis](https://manuelpagliuca.github.io/uploads/MANUEL_PAGLIUCA_ANISOTROPIC_MM_Master_s_Thesis__Integral_.pdf), the comparison is also described using the face area coefficent of variation

The commands generate two batches of samples, and multiple executions of the commands are used for the analysis since multiple models are tested.

```batch
python face-stats.py --base-mesh=base.obj --target-mesh=target.obj
```

Default values if you *omit* some of the options:

* `--base-mesh = pallas_124.obj`
* `--target-mesh = pallas_5000.obj`

## Graphical User Interface

### Sample loading

![](sample_loading.gif)

### Scheme subdivisions

![](subdivisions.gif)

#### Displacement

![](displacement.gif)

### CLI commands

#### Generate a single subdivided sample

**Exports** the given base mesh's subdivided (not displaced) mesh.

```cmd
anisotropic-micromesh.exe --base-mesh=base.obj --microfaces=100
```

> In this example the base mesh is being subdivided by the amount of micro-faces passed (`F` can't be passed, since it works in function of the target mesh) using the current scheme ("isotropic" scheme).

#### Generate sample

**Exports** the subdivided and displaced mesh given the inputs

```cmd
anisotropic_micromesh.exe gen-sample --base-mesh=base.obj --target=target.obj --scheme=aniso --factor=3.5
```

> In this example the base mesh will be subdivided using the `anisotropic` subdivision scheme, with a factor `F=3.5` (subdividing x3.5 times the faces of the target mesh).
