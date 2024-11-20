---
title: 'IAMReX: A Multiphase Incompressible Flow Solver Based on the Immersed Boundary Method'
tags:
  - C++
  - Computational Fluid Dynamics
  - Immersed Boundary Method
  - Multiphase Flow
  - Adaptive Mesh
authors:
  - name: Adrian M. Price-Whelan
    orcid: 0000-0000-0000-0000
    equal-contrib: true
    affiliation: "1, 2" # (Multiple affiliations must be quoted)
  - name: Author Without ORCID
    equal-contrib: true # (This is how you can denote equal contributions between multiple authors)
    affiliation: 2
  - name: Author with no affiliation
    corresponding: true # (This is how to denote the corresponding author)
    affiliation: 3
  - given-names: Ludwig
    dropping-particle: van
    surname: Beethoven
    affiliation: 3
affiliations:
 - name: Lyman Spitzer, Jr. Fellow, Princeton University, USA
   index: 1
   ror: 00hx57361
 - name: Institution Name, Country
   index: 2
 - name: Independent Researcher, Country
   index: 3
date: 13 August 2017
bibliography: paper.bib

# Optional fields if submitting to a AAS journal too, see this blog post:
# https://blog.joss.theoj.org/2018/12/a-new-collaboration-with-aas-publishing
aas-doi: 10.3847/xxxxx <- update this with the DOI from AAS once you know it.
aas-journal: Astrophysical Journal <- The name of the AAS journal.
---

# Summary

The IAMReX repository is constructed based on the IAMR code, 
dedicated to solving the equations of multiphase incompressible flows. 
It utilizes the projection method to solve the Navier-Stokes equations 
on a semi-staggered grid, an approach that effectively manages the dynamics of 
incompressible fluids. Regarding the capture of gas-liquid interfaces, IAMReX 
offers both the Level Set (LS) method and the Conservative Level Set (CLS) method; 
these two techniques can accurately capture the dynamic changes of gas-liquid 
interfaces, making them particularly suitable for problems involving free surface 
flows or multiphase flows. For fluid-solid interface issues, IAMReX employs the 
Multi-Direction Forcing Immersed Boundary Method (IBM), a powerful tool for 
simulating the interaction between fluids and complex solid boundaries without 
the need for grid matching on the solid boundaries, thereby reducing computational 
costs and increasing flexibility. Additionally, IAMReX captures collisions between 
particles and walls as well as between particles themselves through the Adaptive 
Collision Time Model (ACTM), which is crucial for the simulation of particulate flows, 
providing a more realistic representation of particulate dynamics. This code is designed 
to simulate multiphase flow and fluid-structure interaction (FSI) problems, 
capable of running on both CPUs and GPUs with or without subcycling, meaning 
it can operate efficiently on different hardware platforms, leveraging the 
parallel processing capabilities of modern computational architectures to 
accelerate simulation processes. Code-level optimizations, such as loop unrolling (pragma unroll), 
further enhance computational efficiency. IAMReX can handle complex multiphase 
flow physical models, including the behavior of ideal gases and non-ideal fluids, 
and employs models like the Wallis speed of sound to calculate the speed of sound 
in multiphase mixtures, which is crucial for simulating the propagation of pressure 
waves and similar issues. As a powerful tool, IAMReX is suitable for researchers and 
engineers who require high precision and efficiency in solving multiphase flow and 
fluid-structure interaction problems, and it is adaptable to the ever-changing 
computational demands and challenges..

# Statement of need

`Gala` is an Astropy-affiliated Python package for galactic dynamics. Python
enables wrapping low-level languages (e.g., C) for speed without losing
flexibility or ease-of-use in the user-interface. The API for `Gala` was
designed to provide a class-based and user-friendly interface to fast (C or
Cython-optimized) implementations of common operations such as gravitational
potential and force evaluation, orbit integration, dynamical transformations,
and chaos indicators for nonlinear dynamics. `Gala` also relies heavily on and
interfaces well with the implementations of physical units and astronomical
coordinate systems in the `Astropy` package [@astropy] (`astropy.units` and
`astropy.coordinates`).

`Gala` was designed to be used by both astronomical researchers and by
students in courses on gravitational dynamics or astronomy. It has already been
used in a number of scientific publications [@Pearson:2017] and has also been
used in graduate courses on Galactic dynamics to, e.g., provide interactive
visualizations of textbook material [@Binney:2008]. The combination of speed,
design, and support for Astropy functionality in `Gala` will enable exciting
scientific explorations of forthcoming data releases from the *Gaia* mission
[@gaia] by students and experts alike.

# Mathematics

Single dollars ($) are required for inline mathematics e.g. $f(x) = e^{\pi/x}$

Double dollars make self-standing equations:

$$\Theta(x) = \left\{\begin{array}{l}
0\textrm{ if } x < 0\cr
1\textrm{ else}
\end{array}\right.$$

You can also use plain \LaTeX for equations
\begin{equation}\label{eq:fourier}
\hat f(\omega) = \int_{-\infty}^{\infty} f(x) e^{i\omega x} dx
\end{equation}
and refer to \autoref{eq:fourier} from text.

# Citations

Citations to entries in paper.bib should be in
[rMarkdown](http://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html)
format.

If you want to cite a software repository URL (e.g. something on GitHub without a preferred
citation) then you can do it with the example BibTeX entry below for @fidgit.

For a quick reference, the following citation commands can be used:
- `@author:2001`  ->  "Author et al. (2001)"
- `[@author:2001]` -> "(Author et al., 2001)"
- `[@author1:2001; @author2:2001]` -> "(Author1 et al., 2001; Author2 et al., 2002)"

# Figures

Figures can be included like this:
![Caption for example figure.\label{fig:example}](figure.png)
and referenced from text using \autoref{fig:example}.

Figure sizes can be customized by adding an optional second parameter:
![Caption for example figure.](figure.png){ width=20% }

# Acknowledgements

We acknowledge contributions from Brigitta Sipocz, Syrtis Major, and Semyeong
Oh, and support from Kathryn Johnston during the genesis of this project.

# References