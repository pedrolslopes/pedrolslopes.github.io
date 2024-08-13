---
layout: posts
title:  "Cash Flower"
date:   2024-08-12 8:05:54 -0500
classes: wide

graph:
  - url: /assets/images/cash_flower_analysis_example.png
    image_path: /assets/images/cash_flower_analysis_example.png
    alt: "graph"
    title: "Cash Flower Data Analysis"

---
Recently I have written posts on the challenges and subtleties of keeping a healthy funding stream for a scientific team. We have also covered some creative practices and opportunities to mitigate some of the risks involved and challenges identified.

This is my own attempt at contributing something to this cause. Keeping track of a group's finances can be tricky; being able to forecast one's funding capacity, measuring opportunities against burning rates, can be the difference between being caught unprepared or stably honoring the trust other researchers put on the team manager. Thus, I introduce the "Cash Flower", a simple Monte Carlo program to provide financial forecasts for an organization funded by typical means a researcher may encounter. Find the source and installation insructions on [this repo](https://github.com/pedrolslopes/Cash_Flower).

Financial data can be input in four different types of categories:

  - **Stable**: Constant sources of income or expense (e.g., salaries, bills, IP licenses), characterized by monthly average values and variances.
  - **Singles**: One-time revenue or expense events (e.g., rare large sales, purchases).
  - **Recurrent**: Repeated cash flows triggered after an initial event (e.g., long-term deals, scholarships, sales or purchase of established products).
  - **Project**: Milestone-based cash flows tied to project success and timing (e.g. grants).

Users may flexibly encode data from their different funding streams in the categories above, with pre-determined probabilities of realizing each event, according to preferences, convenience, or mindset. No single right way of doing it.

Given a set of financial data, Cash Flower outputs some traditional data analytics upon estimating several scenarios of success or failure at achieving revenue or expenses. These analytics include, for the moment, monthly revenue/expense reports, an analysis of the accumulated funding in the organization as function of time, and the risk of going negative. Here goes what the generated plots can look like for some example data:

{% include gallery id="graph" %}

This program is open source and all are welcome to contribute to the project. Some of my current ideas for improvement include:

- Better visuals for histogram of monthly expenses and gains.
- Change data gathering and reading scheme so users can take resources from Excel spreadsheets or Pandas dataframes.
- Plot categorized data according to the different types of cashflow events, evaluating how important each is at a given time.

Bug reports are also welcome, particularly identifying situations where the program fails!

I hope Cash Flower will help scientific managers and individual contributors alike to better monitor the financial health of their endeavours!

_Disclaimer: as of the writing of this post, these resources have not yet been tested on realistic scenarios._

_For this one I owe a big thanks to my wife, Marianne, for the support, helping with debugging, and feature suggestions. Hope this will be useful to her one day! I also owe the idea for creating this program to Yuval Boger, "The Superposition Guy"._
