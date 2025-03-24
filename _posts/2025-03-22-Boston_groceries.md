---
layout: posts
title:  "Boston on a budget"
date:   2025-03-22 8:05:54 -0500
classes: wide

graph_1:
  - url: /assets/images/boston_data/country_overview.png
    image_path: /assets/images/boston_data/country_overview.png
    alt: "graph"
    title: "US cost of living overview"

graph_2:
  - url: /assets/images/boston_data/spreadsheet_overview.png
    image_path: /assets/images/boston_data/spreadsheet_overview.png
    alt: "graph"
    title: "Spreadsheet overview"

graph_3:
  - url: /assets/images/boston_data/grocery_day_examples.png
    image_path: /assets/images/boston_data/grocery_day_examples.png
    alt: "graph"
    title: "Grocery day examples"

graph_4:
  - url: /assets/images/boston_data/market_map.png
    image_path: /assets/images/boston_data/market_map.png
    alt: "graph"
    title: "Boston market map"

graph_5:
  - url: /assets/images/boston_data/expenses_weekly.png
    image_path: /assets/images/boston_data/expenses_weekly.png
    alt: "graph"
    title: "Weekly expenses analysis"

graph_6:
  - url: /assets/images/boston_data/categorized_expenses.png
    image_path: /assets/images/boston_data/categorized_expenses.png
    alt: "graph"
    title: "Categorized expenses"

graph_6:
  - url: /assets/images/boston_data/categorized_expenses.png
    image_path: /assets/images/boston_data/categorized_expenses.png
    alt: "graph"
    title: "Categorized expenses"

graphs_7_8:
  - url: /assets/images/boston_data/milk_per_galon.png
    image_path: /assets/images/boston_data/milk_per_galon.png
    alt: "milk"
    title: "milk per galon"
  - url: /assets/images/boston_data/eggs_per_dozen.png
    image_path: /assets/images/boston_data/eggs_per_dozen.png
    alt: "eggs"
    title: "eggs per dozen"

graph_9:
  - url: /assets/images/boston_data/fruit_seasonality.png
    image_path: /assets/images/boston_data/fruit_seasonality.png
    alt: "graph"
    title: "Fruit seasonality"

graph_10:
  - url: /assets/images/boston_data/price_quantity_correlations.png
    image_path: /assets/images/boston_data/price_quantity_correlations.png
    alt: "graph"
    title: "Price-quantity correlation"

graphs_11_12:
  - url: /assets/images/boston_data/final_outcome.png
    image_path: /assets/images/boston_data/final_outcome.png
    alt: "end game"
    title: "Final outcome"
  - url: /assets/images/boston_data/close-up_message.png
    image_path: /assets/images/boston_data/close-up_message.png
    alt: "close-up"
    title: "Close-up message"
---
This post is a long one in the making. I should dedicate it to my wife, as this has been a family project running for years. We will divert from science management for this issue, and talk about grocery management! So a post on data science for everyone!

Here is a short prelude to a longer story: back in the covid years, my wife and I were living in Vancouver, and dealing with the steep prices of the city on academic salaries. Given we love cooking, for fun (and maybe out of spite as well), we started hacking the city for grocery bargains. We were very successful and, by the time we were about to leave to Boston (our current residence), I told a friend - whose identity I will spare, to not gloat too much! - that we seemed to be spending about $20 bucks a week in groceries for two people. He called me a liar (or just plain wrong). He underestimated my scientific spirit; he didn't know what he was starting.

### *NERD-sniping strikes back*

Boston, like Vancouver, is one of the worst cities in the world (and in particular in the US) for cost of living. Here goes an illustrative chart on that:
{% include gallery id="graph_1" %}{: .align-center style="width: 70%;"}

The motivation to hack Boston groceries was there for me and my wife, just like in Vancouver, and I was determined to get revanche on my friend who doubted me. So we decided to go quantitative. Since our first week in Boston, we started a spreadsheet where we have registered every single grocery purchase we ever made (focused on foodstuffs only). Fast-forward 3.5 years and we have over 1000 entries of data! 

{% include gallery id="graph_2" %}{: .align-right style="width: 40%;"}
Plenty for our scientific minds to have fun with.

_A small disclaimer: Boston scientific culture is cramed with opportunities for free food (both in academia and industry settings). Given that, we are very mindful about cooking most of what we eat, not having more than one free meal per week, on average, and not going to restaurants mode than once a month (not a challenge; Boston's restaurant's scene is surprisingly not that exciting). These free meals and restaurant food expenses are not accounted for. What we account is just what is spent in pure grocery shopping, which by far and large accounts for most of our monthly expenses other than bills/rent._

The database accounts for names of the items, quantity purchased, price and price per quantity ("specific price" or "Sprice"), date, place, and category. We also included a details column for any noteworthy comments we felt like making. Keeping format and units through quantities is not always easy, and every now and then we have to review the database for drifts in patterns. That introduces a degree of uncertainty in the data which, since our dataset is so large and mostly coherently populated, is likely to be inconsequent to the truthfulness of broad conclusions on our patterns. 

So let's look at interesting general insights that we believe can be quite meaningful to the typical Bostonian. And also some personal insights we learned about our on consumer patterns.

### *Good grocery deals and where do we find them*

Let's start with some exemplary photographs of what a grocery day can look like. 
{% include gallery id="graph_3" %}{: .align-center style="width: 70%;"}
As can be seen, good deals can include vegetables and fruits, as much as meats and packaged ingredients. The secret here is that this city (as perhaps many in the USA) deal with too much abundance, and the surplus market can lead to unbelievable deals (like 30+ lemons for $1).

Our data allows us to carefully consider where do we go most for purchases and draw some geographic correlations. We live in the North End neighborhood, which is fairly central and well connected. 4-5 different stores concentrate the majority of our expenses. We found out that _we are lazy, but not that much_. We certainly visit markets and stores closer to us more often than far, but we actually put the effort to reach some farther destinations because their deals are special to us. Quantitatively (data not shown), we do groceries within a couple km from our home about 85% of the time, but out of the remaining 15%, almost its totality brings us to about full 5km away from where we live (and we got no cars).

{% include gallery id="graph_4" %}{: .align-center style="width: 70%;"}

On the graph above we show some of our favorite items for each place. Some may be unexpected: Whole Foods, generally the most expensive market short of gourmet markets, is the place where we can get "natural" peanut - no sugar or oils added, unfortunately it is hard to also avoid salt here in the US - for the best price. It is a special item that we care for just like that, so we suffer Whole Foods every now and then. An interesting finding is also that large chain stores may not have standardized prices even within a single city. A small corner Target store at Beacon Hill, my wife realized, used to sell full 12-egg cartons for $1! Well, that was back in 2022. Regulations on granaries made that go away, but we enjoyed the deal while it lasted! They still sell milk for the best prices.

Other favorite places for us include the traditional Haymarket and Jia Ho market - the latter in China Town - for surplus fruits and veggies, as well as the hispanic market Tropical Foods in Roxbury, for flours and meat (particularly chicken) and some other specialty items.

### *Expense records*

Dear friend that doubted me, this one is for you! You know who you are! ;-)

{% include gallery id="graph_5" %}{: .align-right style="width: 50%;"}

Knowing the right places for the right items, eating mostly home prepped food, and putting the energy to pursue the right deals, we have hit our mark! Averaging through our whole time in Boston, we have spent, on average, close to $25 per week! In fact, averaging our weekly expenses per year, we found that we considerably lowered our expenses as time passed (and despite significant inflation). In recent years (data not shown), we are spending around $19/week on groceries. (for the purists that may not be satisfied with the $25 above, given my original claim while in Vancouver)

{% include gallery id="graph_6" %}{: .align-right style="width: 50%;"}

The data suggests all kinds of other interesting patterns, including some degree of periodicity (which we associate with our consuming rate of more industrialized products like condiments and seasonings). Looking at our categorized expenses, it seems like we do pretty well; grains, dairy, vegetables and fruits make bulk expenses, with meat - which is considerably more expensive - matching values, suggesting we don't buy much meat (even when we do, we tend to go for items usually ignored/discarded by most, like chicken gizzards and beef/pork bones).

### *Seasonal and other chronological patterns*

With our data, we can also track how inflation and public policies have affected the prices of different items. A couple favorites are milk and eggs, the former because it is such a staple item for us, and the latter because of having shown a fourfold increase in price through our years of monitoring. 
{% include gallery id="graphs_7_8" %}

A curious one involves looking at the seasonality of our consumption of fruits. Comparing 4 sub-categories showcases that our purchase pattern (which, take me for my word, follows the best deals we find) is strongly correlated with the seasons for each of these major fruit categories. Surprisingly pears appear to fall out of the line, with peak in our purchases in April. Some explanations for this could include that good deals for pears in that time of the year may involve importing them from the southern hemisphere. Another option would be that, given that pears are generally available throughout the whole year, and late fall in the northern hemisphere is not a good season for any of our major purchase sub-categories, we may default to pears which we like so much!

### *The economy of scale*

A commonly shared intuition is that buying foodstuffs in larger quantities result in economy. But is that the case? If so, what is the scaling law?

Scatter plotting all our purchases with respect to the corresponding quantities bought (normalized to unitless) gives us direct access to exactly that knowledge!

{% include gallery id="graph_9" %}{: .align-right style="width: 50%;"}

Indeed, a descending trend is verified on price as function of quantity. A fit showcases that the corresponding scaling law shown for our dataset is $price \sim quantity^{-1.0 \pm 0.1}$! This is an awesome result but bittersweet result. Some of us (me!) were really hoping for a non-linear inverse scaling that favored even lower prices for ever larger quantities. We just got inverse proportionality. Still, it is awesome to see common knowledge verified and quantified!

{% include gallery id="graph_10" %}{: .align-right style="width: 50%;"}

### *Final words*

Given how expensive central cities are becoming, and given how short student stipends can be, I hope this knowledge can come in handy for many folks, including scientists in the making. The ideas can be replicated in other cities or, if you live in Boston, you may want to deploy them according to your own needs and preferences!

Often I see professional chefs saying that good food depends on quality ingredients. My experience is that cooking is a forgiving science and a multi-sensorial art. If your tomato is not perfectly round, you can still make good pizza sauce, salad, or whatnot. You can make it look good, smell good, and be very appealing. So let it not be said that the use of economy of scale, surplus markets, and undervalued ingredients will limit the quality of what we eat. I will leave you with some photos of what we have cooked, to make our final point, and some words of excitement!

{% include gallery id="graphs_11_12" %}
