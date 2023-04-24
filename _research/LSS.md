---
title: "Simulating Cosmic Structure"
layout: single-portfolio
excerpt: "<img src='/images/research/LSS_icon.png' alt=''>"
collection: research
order_number: 10
header: 
  og_image: "research/LSS_icon.png"
---



![LSS](/images/research/LSS.png)
**Figure 0:** Filamentary structures of intergalactic gas spanning tens of Megaparsecs, produced by the [Nyx Simulation Suite](https://amrex-astro.github.io/Nyx/).

# Section 0: Introduction

What follows is a visual guide for anyone curious about the Large Scale Structure of the Cosmos, what we can learn by mapping it, and how we can simulate its formation on a computer.

# Section 1: Cosmic Cartography

![Sloan Digital Sky Survey](/images/research/SDSS.svg)
**Figure 1:** A 3D map of galaxies in the local universe (z<0.15), reconstructed using galaxy spectra by the [Sloan Digital Sky Survey](https://classic.sdss.org/).



![Deep](/images/research/Deep_Survey.png)
**Figure 2:** A deeper map of galaxies in the more distant universe (z<5), reconstructed using galaxy and quasar spectra by the [Sloan Digital Sky Survey](https://classic.sdss.org/), adapted from a figure made by [mapoftheuniverse.net](https://mapoftheuniverse.net/) showing the cosmic microwave background in the distance.



![Absorb](/images/research/Absorb.svg)
**Figure 3:** Light from a distant quasar is absorbed by intergalactic gas clouds on its way to earth.



![QSO](/images/research/QSO_Spectra.png)
**Figure 4:** High resolution (FWHM ~ 6.6 km/s) spectrum of a quasar at z = 3.62, taken with the Keck High Resolution Echelle Spectrometer (HIRES). Data from [Womble et al (1996)](https://arxiv.org/pdf/astro-ph/9511035.pdf).


![Skewer](/images/research/Skewers.svg)
**Figure 5:** Surveying many distant quasars and Lyman-break galaxies allows us to reconstuct an approximate map of the gas ocacity in the distant universe which we can use for statistical analysis.

# Section 2: Analysis Pipeline

![Pipeline](/images/research/LSS_Pipeline.png)
**Figure 5:** Data analysis pipeline for obtaining constraints on cosmological parameters from observations of cosmic structure.

# Section 3: Digital Universes

### Dark Matter and Gravity Simulation

 
<p align="center"><video width="640" height="480" autoplay muted>
  <source src="/images/research/NBody.mp4" type="video/mp4">
</video></p>

**Video 1:** Simulation of self-gravitating dark matter particles forming structure. 

![Expand](/images/research/Expand.svg)
**Figure 6:** Dark matter structure can be simulated using an N-Body simulation in an expanding spacetime. Many particles gravitationally attract eachother while the frame they inhabit is slowly stretched out.

<p align="center"><iframe src="https://openprocessing.org/sketch/1900476/embed/?plusEmbedHash=NGUxNzEzNTI3NDhkZTRhOTUyZmRhNzQ0ZDhlYzFmYjFmZGE4N2Y1MDc4ZTUzZTAzYmE5OGM1OTUzM2ZhODgwZDFmZDAzNTg3Nzg2NDdkZTE3YzZhOWVlYjlmYjQ5NDA4ZTQwOGIzZDliYmZkOGMwMDk3YThhYjcxNDQ1YWQwNGJXcy8zc0pkeUxVMWFvTUNkeEdYTGxnS2FUanh6STU2aFhJU3ZhZE5JSFBkN3pIYUZuNzlHY0p2WURPZUtzODlQdUsrcEFzMzNTM2VuVnpidVhJRUMxZz09" width="620" height="640"></iframe></p>

### Initial Conditions

![CMB](/images/research/CMB_PS.svg)
**Figure 7:** Observations of the CMB provide constraints on the initial conditions of the overdensity fluctuations as modeled by a guassian random field.


### Visible Matter and Fluid Simulation


<iframe width="560" height="315" src="https://www.youtube.com/embed/4IIEJlSwuXo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
**Video 2:** Evolution of cosmic structure including baryon hydrodynamics. View is 10 Mpc wide, taken from the [TNG100 simulation](https://www.tng-project.org/).



![Advect](/images/research/Advection.png)
**Figure 8:** Fluid transport (ie. Advection) on an Eulerian Grid is done by distributing the density in given cell to the cells nearest the tip of the velocity vector extending from the start cell.

![Diffuse](/images/research/Diffusion.png)
**Figure 9:** Density Diffusion and Fluid Viscosity on an Eulerian Grid are modeled similarly by diffusing a each field slightly each timestep using convolution with some discrete gaussian kernel.

<p align="center"><iframe src="https://openprocessing.org/sketch/1052845/embed/?plusEmbedHash=YmEzYTllYTJjMDI0MmM1NmM3YThkNWM5NWVmZGVhYjcyZjUyMzI3MTdjZTliMTAwZDFiNTY0MWQyNTM2NjdjY2ViMmMyMGRmMmFhNWI5Yjk4MTM5NjY4NzMxNjJlZGNlZWU4MWUxOWY5YjY3YTAzYmFkMTgzMmNjNTAxMWU5ZTlhYWJscXNmZk1Vd2ZoUTVQV1BJWFlubmMrR0Q4dGtsUzVISW90MTBQTFBKalg4YUI1K29qYW1mN2ZNblp6cGF1c0FqVkphYXNuTTZkVVlWK2RaSUtOZz09" width="620" height="640"></iframe></p>
**Appliction 1:** Combining the above concepts yields a visually striking fluid model. Click and drag to induce flow.


<p align="center"><iframe src="https://openprocessing.org/sketch/1052684/embed/?plusEmbedHash=YTE5OWVlOTRmZWUxMzk2ZjAzYjFjNzQ0NmNjOGY1YmQ2ODliYzU5N2U0NTkxMjZkZDQ2Y2U4YmYyNWExODVjOTRlODcwMDBiYWI4NGI1NGExM2MwMjFkMDdlM2FkYzBhNjI1MTk2ZGRkMDIyMzVkYjlmNjgxNWQ1OTU0ZmUzZTRiWUt4ZVo3ak9Zai9vWXl3YlJmYlljU1RPbm9nUHppYXROd2hBVCtkdWNWUjJzai9hT1kvYkorVEhNVHFvb0pYcmQvVy93d3htYkFtc0NPTGk5dmJkdz09" width="620" height="640"></iframe></p>
**Appliction 2:** Increasing the grid's cell density improves the fluid's realism. Click and drag to induce flow.

