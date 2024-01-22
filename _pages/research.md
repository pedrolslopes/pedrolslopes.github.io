---
title: "Research"
layout: splash
permalink: /research/
collection: publications
author_profile: false
classes: wide
sort_order: reverse

intro: 
  - excerpt: <br> The bulk of my scientific production revolves around two main topics of quantum physics that I approach via quantum-field theoretical and algebraic numerical approaches.

interest1:
  - image_path: assets/images/QP-Fractionalization.png
    alt: "placeholder image 2"
    image_size: 100%
    title: "Quasiparticle fractionalization"
    excerpt: "Through strong interactions, quantum matter can undergo quasiparticle fractionalization, effectively separating intrinsic degrees of freedom like the spin and charge of an electron. This phenomenon, often intertwined with topological effects, manifests in limited dimensions or in the presence of material defects such as boundaries, or atomic disclinations and dislocations. The resulting particles, known as anyons, exhibit properties that span a continuum between familiar fermions and bosons. This departure from nature's conventional elementary particles not only serves as a fascinating deviation but also holds practical value for fault-tolerant quantum computation. Check out my research on qubit architectures with Fibonacci anyons in Kondo systems for more on that!"

interest2:
  - image_path: /assets/images/Symmetry-Emergence.png
    alt: "placeholder image 2"
    image_size: 100%
    title: "Symmetry emergence"
    excerpt: "In the realm of phase transitions, systems at low energies are expected to emmergently exhibit reduced symmetries, as when fluids freeze into crystalline structures. When topology is at play, the classification of certain phases with no difference in symmetries is also possible. A less explored possibility is the emergence of higher symmetries in systems at low energies. While this phenomenon is sporadically discussed in the literature on a case-by-case basis, my research delves into systematically analyzing mechanisms that broadly induce 'symmetry emergence' across physical systems. I design these mechanisms from the bottom-up via structures that combine degrees of freedom and restrict perturbations, or uncover them from the top-down scrutinizing cases of unexpected symmetry emergence."

---
 

{% include feature_row id="intro" type="center" %}

{% include feature_row id="interest1" type="left" %}

{% include feature_row id="interest2" type="left" %}

<h1><b> Publications: </b></h1>
<div class="archive__item-excerpt">
  {% include publications-collection.html collection=page.collection sort_by=page.sort_by sort_order=page.sort_order type=entries_layout %}
</div>

