---
layout: posts
title:  "Showcasing Emergence in Scientific Collaborations"
date:   2024-03-16 8:05:54 -0500
classes: wide

graph:
  - url: /assets/images/network_plot.png
    image_path: /assets/images/network_plot.png
    alt: "graph"
    title: "pub network"

reports:
  - url: /assets/images/Academic Network Current State.png
    image_path: /assets/images/Academic Network Current State.png
    alt: "report current"
    title: "report current"
  - url: /assets/images/Academic Network Target State.png
    image_path: /assets/images/Academic Network Target State.png
    alt: "report target"
    title: "report target"
---

*This post tells a bit of my own professional story as I left life as a pure researcher, and then moves toward introducing my first managerial tool for scientific collaborations. Hope you enjoy it!*

It was early 2020, before the surprising upheaval of life caused by Covid-19. I had found my first non-research job: to manage and pave the way for the success of the [Stewart Blusson Quantum Matter Institute Grand Challenges](https://qmi.ubc.ca/) research program. This program aimed to foster coherence in research among the institute's members, prioritizing and focusing research topics for greater impact and value for the community.

The origin of this Grand Challenges program can be traced back to discussions among the Institute's scientific advisory board. Simplifying a complex story, these advisers questioned why significant funds should be injected into a thematic institute if it merely resulted in already established research groups continuing to work independently. Essentially, there was a view that merely uniting independent researchers under a well-funded endeavor wasn't enough to drive transformative change and leadership. To make the institute an undisputed global leader in its field. Many of its groups were already adequately funded, so achieving such scientific leadership was seen to require a coherent, laser-focused approach on the most impactful work possible.

Echoing Phil Anderson's timeless ["more is different"](https://www.science.org/doi/10.1126/science.177.4047.393), widely influential across the quantum matter community, the sentiment was that to achieve scientific prominence and success, the "institute must be more than the sum of its parts." Primary Investigators were brought together, themes were selected, and charters of work and project proposals began to take shape. I was brought in to oversee the management of the program.

Program and project management in the physics community are not extensively documented, and tools and methodologies are not well developed. This is partly because deliverables tend to be uncertain, making it tricky to track progress and evaluate performance using formal approaches. When I began working on the Grand Challenges, I underwent professional training in project management. However, many concepts were not directly transferable. Moreover, attempting to impose standards developed by outsider communities on academic groups with different pressures and goals was likely to backfire and generate conflict. Nevertheless, I was enthusiastic about the opportunity to innovate how research could be conducted and managed.


As upper management pressured the Grand Challenges team to create deliverables and performance indicators, I decided to revisit the program's origin. The success of the work should indicate that the program was fostering coherence within the institute, ensuring it was more than the sum of its individual parts. Being a mathy guy and having a career centered around correlated matter, I embraced ambition. I conceived an academic social network for the Grand Challenges Principal Investigators. This tool, I believed, would be visually impactful for reporting - facilitating communication with donors and advisory boards - and enable precise course corrections and policy changes to achieve success. Moreover, its geeky appeal made it likely to be embraced by academics without resistance to managerial practices, which was a personal favorite aspect.

So what did this look like? Here goes an example:

{% include gallery id="graph" %}

I assigned professors in a given project academic names (Professor A, B, etc., in this example) and represented them as nodes in a graph (the blue disks). With the help of a colleague, I obtained a database containing all the papers of the institute's members. I then wrote a script to filter this database, creating a list of pairs of names whenever two professors co-authored a scientific publication. These pairs were represented as red edges on the graph, symbolizing collaboration—instances where individual members joined efforts to address a single problem. To depict the strength of collaboration, the thickness of the red connections was made proportional to the number of papers two researchers co-authored. The more papers they shared, the stronger their collaboration!

Now how could I create a sense of "where this program is going"? I decided to examine sub-projects proposed in the program. As these involved multiple groups, I created a list of "collaborations in development." If an edge didn't exist between two professors but collaboration was underway, I depicted it as a dashed line. The web of dashed lines indicated the program's capacity to foster a more robust collaborative network, paving a path to make the institute "more than the sum of its parts." For reporting and tracking, once a publication came together, boom! The list of publications could be updated, the dashed line would become red, and one could visualize the change in the network directly.

Of course, these are all qualitative ways of looking at the problem. But again, graph theory is a well-established branch of mathematics. There are several quantities one can use to obtain quantitative information on the state of one such network. Here go a few I like:

* Degree Distribution: the distribution of degrees (number of connections) can provide insights into the connectivity of the network. In our academic network, we would be looking at the number of collaborations each professor has.

* Centrality Measures: Centrality measures identify the most important nodes in the network. Some measures of centrality include:
    * Degree Centrality: the number of connections each node has.
    * Betweenness Centrality: the number of shortest paths that pass through a node. This indicates the node's importance as a bridge between different parts of the network.
    * Closeness Centrality: this measures how close a node is to all other nodes in the network, indicating its ability to quickly  spread information.
    * Clustering Coefficient: the degree to which nodes tend to cluster together. In our research network, this indicates the presence of tightly-knit research sub-groups.

* Path Length Distribution: the distribution of shortest path lengths between nodes, which provides insights into the overall structure and connectivity of the network.

Reports with these data could then be generated for analysis. I habitually provided reports on the "current state" of the network (i.e., without the dashed lines), and "target state" (including the dashed lines) for comparison. These can be plotted in bar charts and set up thes side-by-side for analysis. For example, for the mock data of the graph above, we would have


{% include gallery id="reports"  %}

Though there's room for improvement—for example, plotting both on the same axes for easier comparison—the tool proved effective. It not only structured early program reporting but also aided researchers in grant applications, helping secure nearly seven-figure funding. While the solidity of research programs was the main driver of such success, I am happy I could play a small part in this achievement.

Managerial teams are not always equipped to program tools like this, nor to determine suitable graph-based metrics. I've heard that reproducing what I initiated with these networks became challenging after my departure from the Stewart Blusson Quantum Matter Institute. Recently, with renewed energy, I revisited my code and polished it to make it easier to reuse and share. If you are interested in trying it, you can find what I hope is a straightforward codebase on [this Github repo](https://www.github.com/pedrolslopes/publishing_network). Once you've successfully generated your data, running

```
python research_network_analyzer.py
```

will generate figures of your network, plots with data analysis, and text files with numerical report data for both the current and target states of your network. As mentioned above, there is space for improvement, but I hope this can now be useful to more people!

And with that, the story—or perhaps this chapter—ends. The Grand Challenges program is ongoing, and research there continues to thrive. Many former researchers who participated in the program have moved on to prominent positions in academia and industry. Likewise, my journey to improve managerial practices in research environments continues to evolve.