---
title: "Simulating Cosmic Structure"
layout: single-portfolio
excerpt: "<img src='/images/research/LSS_icon.png' alt=''>"
collection: research
order_number: 10
header: 
  og_image: "research/LSS_icon.png"
---


# Section 0: Introduction

What follows is a visual guide for anyone curious about the Large Scale Structure of the Cosmos, what we can learn by mapping it, and how we can simulate its formation on a computer.

The Large Scale Structure (LSS) of the universe is a fascinating subject of study for astrophysicists and cosmologists. It refers to the distribution of galaxies and matter on a larger scale than individual galaxies or galaxy groups, with patterns extending up to billions of light years. These structures are formed and shaped by gravity, which pulls galaxies and matter together to create rich and complex patterns, resembling a cosmic web. Studying LSS provides astronomers with important insights into the formation and evolution of the universe as a whole.

![LSS](/images/research/LSS.png)
**Figure 0:** Filamentary structures of intergalactic gas spanning tens of Megaparsecs, produced by the [Nyx Simulation Suite](https://amrex-astro.github.io/Nyx/).

Studying LSS allows cosmologists to measure the strength of gravity in the universe, as they can measure galaxies at different distances and times in the universe's history, revealing that gravity has been attracting more matter together over time. Furthermore, LSS provides information about dark energy, the mysterious pressure driving the expansion of the universe, which is known to slow down the process of gravity creating large structures. As the universe accelerates in its expansion, matter takes more time to come together due to the increased distance. By studying the growth of LSS over time, astronomers can gain knowledge about how the relative strengths of gravity and dark energy may themselves be changing as the universe evolves. 

In this article, we will explore the methods used to map the composition of the nearby universe and the techniques used to simulate the formation of the large scale structure of the cosmos as a whole. 


# Section 1: Cosmic Cartography

![Sloan Digital Sky Survey](/images/research/SDSS.svg)
**Figure 1:** A 3D map of galaxies in the local universe (z<0.15), reconstructed using galaxy spectra by the [Sloan Digital Sky Survey](https://classic.sdss.org/).

The simplest way to see this cosmic structure for real is to make a map of the local universe. Figure 1 shows a map of galaxies in the nearby universe up to a distance of about two billion light years away. Each point is a galaxy and the Milky Way (which contains Earth) is at the center. The web-like distribution of galaxies on large scales can be easily seen by eye. 

As the universe expands, light traveling through the universe expands as well. As light expands, its wavelength gets longer and consequently looks redder. Galaxies at large redshifts are further away from Earth which means that the light from those galaxies has taken longer to reach our telescopes and thus has spent more time expanding and getting redder. Astronomers have precisely studied the colors of nearby galaxies so they can use this cosmological reddening information to estimate the distance to galaxies based on the color of light they observe.

The variable z is used to quantify this “redshift”, it describes the scalar factor by which the wavelength has expanded by. For example a galaxy at redshift 0.15 is observed at a wavelength 15% longer than when it was emitted.

Nearby galaxy maps like this are extremely useful for understanding the physics of our universe.

![Deep](/images/research/Deep_Survey.png)
**Figure 2:** A deeper map of galaxies in the more distant universe (z<5), reconstructed using galaxy and quasar spectra by the [Sloan Digital Sky Survey](https://classic.sdss.org/), adapted from a figure made by [mapoftheuniverse.net](https://mapoftheuniverse.net/) showing the cosmic microwave background in the distance.

Two billion lightyears may sound like a lot (and it is!), but the universe is much bigger. As we look further away and further back in time, it becomes more and more difficult to find visible galaxies. As you can see in figure 2, the density of observable galaxies falls off for distances further than z=5 (ie. 500% redder)  To map the universe beyond here, astronomers will need to be creative. 

It may be hard to see distant galaxies, but a handful of quasars are still visible. Quasars are supermassive black holes at the centers of galaxies. Unlike the dark supermassive black hole in the center of the Milky Way, quasars are some of the brightest objects in the universe. They consume infalling matter so fast that the disk of gas and plasma orbiting around them heats up and glows with the light of a trillion stars. Some of these extreme quasars are so powerful that they can shine 10 or even 100 times brighter than their host galaxies.

![Absorb](/images/research/Absorb.svg)
**Figure 3:** Light from a distant quasar is absorbed by intergalactic gas clouds on its way to earth.

Knowing the location of these quasars is interesting, but there are not enough of them to form a complete enough map. Fortunately, the light which reaches us from these distant quasars encodes a lot more information. 

As this ancient quasar light travels through the universe, it frequently encounters clouds of intergalactic gas (like that shown in figure 0). As the light enters these gas clouds, certain wavelengths are absorbed and others pass through freely. 

![QSO](/images/research/QSO_Spectra.png)
**Figure 4:** High resolution (FWHM ~ 6.6 km/s) spectrum of a quasar at z = 3.62, taken with the Keck High Resolution Echelle Spectrometer (HIRES). Data from [Womble et al (1996)](https://arxiv.org/pdf/astro-ph/9511035.pdf).

The absorbed wavelengths of light are well known, they are associated with the energy transitions of the element hydrogen, which makes up the majority of these clouds. When the light from a quasar passes through one of these clouds, this wavelength is effectively subtracted from the quasars spectra. You might think of this like a piece of colored glass where if you shine light of all colors (ie. white light) through the glass, orange light might be absorbed but red, yellow, green, blue, purple light pass through the glass freely. 

As the remaining light travels through space, the universe continues to expand and stretch the light with it. Every color/wavelength in the quasar’s spectra is stretched individually, so some light which passed through a cloud before may now be absorbed. This is like if the yellow light passes through a first piece of glass but is then stretched out to look orange (i.e. redder than yellow) and is then absorbed by a second piece of glass.

So as the quasar light travels through the universe, the history of all the gas clouds it has encountered along the way is imprinted in the spectra. With nothing in the way, a quasar’s spectra should be relatively smooth, so astronomers can use the sections that appear to be missing to infer the location of the gas clouds it passed through. 

![Skewer](/images/research/Skewers.svg)
**Figure 5:** Surveying many distant quasars and Lyman-break galaxies allows us to reconstuct an approximate map of the gas ocacity in the distant universe which we can use for statistical analysis.

Modern telescopes can probe the ancient universe with unprecedented precision and depth. Specifically built facilities survey the sky year-round and have mapped millions of these distant quasars and captured their spectra. Using the combination of these spectra, we can construct a map of gas clouds in the distant universe. Figure 5 shows how a set of spectra from distant galaxies and quasars can be used to reconstruct a map of the shadow cast by these web-like gas clouds.


# Section 2: Analysis Pipeline

These maps of the cosmos can be used to study the evolution and underlying physics of our universe. The current large-scale structure of the universe is shaped by the parameters of a given cosmological model, as well as initial conditions. By comparing accurate observed galaxy/cluster maps with high-fidelity simulated model universes we can thus constrain the parameters of our cosmological model, for example: the nature of dark matter and dark energy, the history of inflation and reionization in the early universe, and the mass of neutrino particles.

![Pipeline](/images/research/LSS_Pipeline.png)
**Figure 5:** Data analysis pipeline for obtaining constraints on cosmological parameters from observations of cosmic structure.

These constraints are found by comparing the statistics of the observed, real universe with a large set of simulated universes. Researchers can change physical properties of the universe when running simulations to see how varying parameters like the density of matter or the strength of dark energy affect the structures that emerge. Finding the parameters of the actual universe then becomes a matter of finding which of these simulated universes is most similar to what researchers observe in reality. 

This is not a matter of getting a universe which *exactly* matches our own, where you could point out some recognisable feature like the Milky Way or Andro (or even yourself). Rather, it is an issue of getting the virtual universe to match the real one *statistically*. Certain measurable statistical properties of the universe depend on these underlying physical parameters .

In practice, researchers do not need to get these parameters to exactly match the real universe either. With enough sample, simulated universes, researchers can extrapolate the true values based on the correlation between the statistics and the physical parameters. Even so, this analysis will require producing an astronomical number of these simulated universes. 


# Section 3: Digital Universes

To be able to derive the cosmological constraints discussed above, we need fast and accurate techniques for simulating model universes. Hydrodynamic cosmological simulations are remarkably powerful tools for studying the formation of structure in the universe but require extreme computational resources. Full-physics cosmological simulations are among the most expensive simulations run at supercomputing centers, requiring tens of millions of CPU-hours. 

To get an understanding of how these simulations work, we will break down the basic components of the algorithm: gravity and fluid mechanics. 

### Dark Matter and Gravity Simulation

The overwhelming majority of matter in the universe is what’s called ‘dark matter’. The influence of dark matter has been observed in many different contexts, from the orbital speeds of stars within galaxies to gravitational lensing around galaxy clusters. While Physicists may be unsure what exactly dark matter *is*Astronomers agree about its presence and influence.

Extensive research has suggested that dark matter is cold and pressureless. Unlike ordinary, visible matter which often collides with itself, dark matter seems to be collision-less. The only influence dark matter has on the universe seems to be via gravity. 
 
<p align="center"><video width="640" height="480" autoplay loop muted>
  <source src="/images/research/NBody.mp4" type="video/mp4">
</video></p>
**Video 1:** Simulation of self-gravitating dark matter particles forming structure. 

The classic way to model dark matter is using what’s known as an N-Body simulation. This involves some number, N, of particles which can move about a region of space. These particles interact with one another via gravity, attracting towards each other with a force proportional to the inverse square of their distance.  

![Expand](/images/research/Expand.svg)
**Figure 6:** Dark matter structure can be simulated using an N-Body simulation in an expanding spacetime. Many particles gravitationally attract eachother while the frame they inhabit is slowly stretched out.

To model the expansion of the universe, we can include some parameter, a, which defines the scale at a given time. This scale factor increase with time and is used to calculate the effective distance between two points from their comoving (ie. non-expanding) distance. Effectively this means the force of gravity between points gets weaker over time as their effective distance becomes greater.

<p align="center"><iframe src="https://openprocessing.org/sketch/1900476/embed/?plusEmbedHash=NGUxNzEzNTI3NDhkZTRhOTUyZmRhNzQ0ZDhlYzFmYjFmZGE4N2Y1MDc4ZTUzZTAzYmE5OGM1OTUzM2ZhODgwZDFmZDAzNTg3Nzg2NDdkZTE3YzZhOWVlYjlmYjQ5NDA4ZTQwOGIzZDliYmZkOGMwMDk3YThhYjcxNDQ1YWQwNGJXcy8zc0pkeUxVMWFvTUNkeEdYTGxnS2FUanh6STU2aFhJU3ZhZE5JSFBkN3pIYUZuNzlHY0p2WURPZUtzODlQdUsrcEFzMzNTM2VuVnpidVhJRUMxZz09" width="620" height="640"></iframe></p>
**Appliction 1:** Self-gravitating dark matter particles in an expanding spacetime. (You must hold your mouse in the center of the frame for it to animate)

Modeling the universe using this N-Body approach reproduces the web-like filament structures that astronomers have observed. 


### Visible Matter and Fluid Simulation

There is over five times as much dark matter in the universe as ordinary matter, but (as its name suggests) astronomers have no way to see it. So while dark matter represents the overwhelming majority of the attractive drive behind structure formation, simulations of dark matter alone *do not* contain all of the information relevant to what can actually be seen. 

To simulate the kinds of structure that *can* be observed by our telescopes, we must also simulate the ordinary (non-dark) matter. Unlike dark matter, ordinary matter is collisional (for instance, you cannot pass your hand through the table). This means that we have to add some new features to our simulation technique to capture the properties of ordinary matter. 

The ordinary matter which inhabits the space between galaxies forms a gas. Much like the gasses you’re familiar with here on earth, this intergalactic has some pressure and temperature which affects how it moves. Such a gas will behave like a fluid (note there is a difference between ‘fluid’ and ‘liquid’), it flows much like wind and can even produce turbulence.

<iframe width="560" height="315" src="https://www.youtube.com/embed/4IIEJlSwuXo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
**Video 2:** Evolution of cosmic structure including baryon hydrodynamics. View is 10 Mpc wide, taken from the [TNG100 simulation](https://www.tng-project.org/).

As shown in Video 2, this fluid-like behavior of gas produces a much more diverse and interesting structure than the dark matter-only filaments shown in Video 1. You can see the formation of turbulent, spiral clouds which will seed the formation of galaxies and eventually stars. But also between these newborn galaxies are nebulous tendrils of diffuse gas, these are the structures that can be seen with our telescopes. 

Simulating this fluid behavior presents a unique challenge, so we will break down the key components of the common methods. In principle it would be possible to use a similar N-body scheme, only modifying the code such that these gas particles could collide and bounce off one another. However to accurately capture the pressure and density of such an N-Body gas, an enormous number of particles would be needed and it would be incredibly inefficient to run on any computer.

![Euler](/images/research/Euler.png)
**Figure 8:** The density of intergalactic gas modeled using a grid for the density and velocity fields.

Instead, the gas can be modeled using what’s called a cellular automata. Figure 0 shows a grid of density values where brighter regions are denser. If you are accustomed to thinking of gasses in terms of gas particles, you might think of this density field as encoding the average number of particles per unit volume inside each grid cell.

![Advect](/images/research/Advection.png)
**Figure 8:** Fluid transport (ie. Advection) on an Eulerian Grid is done by distributing the density in given cell to the cells nearest the tip of the velocity vector extending from the start cell.

![Diffuse](/images/research/Diffusion.png)
**Figure 9:** Density Diffusion and Fluid Viscosity on an Eulerian Grid are modeled similarly by diffusing a each field slightly each timestep using convolution with some discrete gaussian kernel.

<p align="center"><iframe src="https://openprocessing.org/sketch/1052845/embed/?plusEmbedHash=YmEzYTllYTJjMDI0MmM1NmM3YThkNWM5NWVmZGVhYjcyZjUyMzI3MTdjZTliMTAwZDFiNTY0MWQyNTM2NjdjY2ViMmMyMGRmMmFhNWI5Yjk4MTM5NjY4NzMxNjJlZGNlZWU4MWUxOWY5YjY3YTAzYmFkMTgzMmNjNTAxMWU5ZTlhYWJscXNmZk1Vd2ZoUTVQV1BJWFlubmMrR0Q4dGtsUzVISW90MTBQTFBKalg4YUI1K29qYW1mN2ZNblp6cGF1c0FqVkphYXNuTTZkVVlWK2RaSUtOZz09" width="620" height="640"></iframe></p>
**Appliction 2:** Combining the above concepts yields a visually striking fluid model. Click and drag to induce flow.


<p align="center"><iframe src="https://openprocessing.org/sketch/1052684/embed/?plusEmbedHash=YTE5OWVlOTRmZWUxMzk2ZjAzYjFjNzQ0NmNjOGY1YmQ2ODliYzU5N2U0NTkxMjZkZDQ2Y2U4YmYyNWExODVjOTRlODcwMDBiYWI4NGI1NGExM2MwMjFkMDdlM2FkYzBhNjI1MTk2ZGRkMDIyMzVkYjlmNjgxNWQ1OTU0ZmUzZTRiWUt4ZVo3ak9Zai9vWXl3YlJmYlljU1RPbm9nUHppYXROd2hBVCtkdWNWUjJzai9hT1kvYkorVEhNVHFvb0pYcmQvVy93d3htYkFtc0NPTGk5dmJkdz09" width="620" height="640"></iframe></p>
**Appliction 3:** Increasing the grid's cell density improves the fluid's realism. Click and drag to induce flow.

![Evolve](/images/research/Evolution.png)
**Figure 6:** Simulation of gravity in an expanding Universe. As time goes on (left to right) the universe itself is expanding so any given box within the universe gets bigger. In reality this effect is *much* more exaggerated. Adapted from an figure by the National Center for Supercomputer Applications (NCSA).

### Initial Conditions

![CMB](/images/research/CMB_PS.svg)
**Figure 7:** Observations of the CMB provide constraints on the initial conditions of the overdensity fluctuations as modeled by a guassian random field.

