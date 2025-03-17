---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Isospin-breaking in light-meson leptonic decays"
subtitle: ""
summary: Summary of recent work on the effects of photons in decays of mesons to leptons
#"(**Image credit: Matteo Di Carlo**) This is a summary of our recent work on including the effects of photons, and the mass difference of up and down quarks, in decays of mesons to leptons and neutrinos."
authors: []
tags: []
categories: []
date: 2023-01-12T12:00:00Z
lastmod: 2023-01-12T12:00:00Z
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  placement: 1
  caption: ""
  focal_point: "Center"
  preview_only: false

links:
  - name: Preprint
    url: https://arxiv.org/pdf/2211.12865.pdf

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

This is a summary of the article [_Isospin-breaking corrections to light-meson leptonic decays from lattice simulations at physical quark masses_]({{< ref "/publication/boyle-2022-lsi" >}}). In this paper, we investigate effects that have been neglected in numerical lattice calculations in the past, but are now becoming important due to increased precision. In particular, we calculate the correction to a ratio of leptonic decay rates of mesons from two closely related effects. The first is electromagnetism (the effect of photons on the decays) and the second is the mass difference of the two light quarks (the effect of the up and down quarks having different masses, $m_u \neq m_d$).

A precise determination of the ratio of leptonic decay rates of kaons and pions (the mesons) into muons and neutrinos (the leptons) is useful for precision tests of the Standard Model. In particular, combining such results with experimental inputs allows one to extract the ratio of Cabibbo-Kobayashi-Maskawa (CKM) matrix elements $|V_{us}|$ and $|V_{ud}|$.

One of the main focuses of the publication is the role of the finite volume in the calculation, which is very important because the finite-volume effects are enhanced when photons are included. This is because a photon can be emitted from the incoming meson (the mother particle), can then travel a long distance, and can then finally interact with the lepton (a decay product). This travel between the interactions implies that the photon can "feel" the finite volume more than the meson itself.

This particular work employs lattice QCD simulations with 2+1 flavors of dynamical quarks with near-physical masses, utilizing Möbius domain wall fermions. Electromagnetic interactions are incorporated using the QED${}_L$ prescription. The study highlights the significant impact of the finite spatial volume on electromagnetic corrections of such decay rates, identifying this as the leading source of uncertainty in the study.
