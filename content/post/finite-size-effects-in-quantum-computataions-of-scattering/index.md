---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Finite-size effects in quantum computations of scattering"
subtitle: ""
summary: Summary of recent work on finite-size effects in real-time quantities
authors: []
tags: []
categories: []
date: 2020-12-10T17:52:21+01:00
lastmod: 2020-12-10T17:52:21+01:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: "Right"
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
This is an informal summary of: [_The role of boundary conditions in quantum computations of scattering observables_]({{< ref "/publication/briceno-2020-rar" >}}).
There has recently been a major push, worldwide, to accelerate the development of quantum technologies and especially quantum computing. One future application of this might be real-time simulations of quantum field theories, potentially including quantum chromodynamics (QCD), the mathematical description of the strong nuclear force. The idea of "real-time" here is in contrast to the current numerical state-of-the-art, the method of lattice QCD, which relies on imaginary times (replacing real $t$ with $t = - i \tau$ where $i = \sqrt{-1}$ and $\tau$ is made real so that $t$ is an imaginary number). This is a mathematical trick that makes the calculation work, but it can severly limit the physical predictions that we can extract.


One class of observables where this plays an important role is that of scattering amplitudes. Consider, for example, the scattering amplitude describing
$$p \pi^- \to n \pi^+ \pi^- .$$
This is naturally a real-time process; at early times a proton and a negative pion collide and at late times a neutron and a charged pion pair emerge. So, three natural questions arise:

1. Can we somehow calculate such processes using current methods (i.e. numerical lattice QCD)?

2. Can we envision calculating such processes using future quantum computers?

3. In which cases, and to what extent, will quantum devices give a significant advantage in extracting this information?

As I have already strongly hinted, the answer to the first question is absolutely yes! The most useful method so far is to use the finite system size in the numerical calculation (often called the finite volume) as a way of probing the interactions. In particular, in the finite-volume set-up, a particular set of discrete energies are allowed to exist, and the values of these energies can be used to determine the scattering amplitude.

The answer to number two is also yes, but in this case the finite volume can only be seen as an unwanted artifact. This turns out to be a very important issue when assessing number three and is exactly the motivation for our work: To compare the extraction of scattering information from imaginary-time calculations (where the finite volume is a useful tool) to the extraction from real-time calculations (where the finite volume becomes an unwanted artifact).

The logic is potentially confusing, as one needs a strategy to predict how real-time scattering information will be distorted by the finite system size. To achieve this, we actually use the standard methods from lattice QCD but run them backwards. So instead of using finite-volume energies and matrix elements to predict amplitudes
$$E_n(L), \langle n, L \vert \mathcal J \vert m, L \rangle \ \longrightarrow \ \mathcal M_{\pi \pi \to \pi \pi}, \ \mathcal T_{\pi \gamma \to \pi \pi} , $$
we use models of the infinite-volume amplitudes to predict the finite-volume information
$$\mathcal M_{\pi \pi \to \pi \pi}, \ \mathcal T_{\pi \gamma \to \pi \pi}  \ \longrightarrow \  E_n(L), \langle n, L \vert \mathcal J \vert m, L \rangle , $$
and this, in turn, to predict the finite-volume amplitudes that one might extract
$$ E_n(L), \langle n, L \vert \mathcal J \vert m, L \rangle \to \mathcal M_{\pi \pi \to \pi \pi}(L) .$$
From here we can compare the finite- and infinite-volume versions of $\mathcal M_{\pi \pi \to \pi \pi}$ directly.

The punchline of this article is that finite-volume effects can be so significant that it is not always clear whether real time provides a clear advantage. This is especially true for systems with interesting types of interactions including short-lived particles (resonances) that form and then immediately decay in the scattering process. The biggest advantage will be for scattering at higher energies and for amplitudes where many particles are involved. Finally, in this article we describe some strategies for reducing the volume effects and illustrate how well these work. Above all, I would stress this is only the first step towards answering these questions and the work has some clear limitations. So far, we have focused on systems with only one spatial dimension (instead of three) and on scattering amplitudes where only one type of particle is involved. Work is already underway to lift these restrictions and investigate the situation for more complicated systems.
