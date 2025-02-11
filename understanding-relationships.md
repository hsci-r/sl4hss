# Understanding relationships

Sometimes, we are not interested in either describing groups or validating their differences. Instead, we may be interested in relationships between variables. For example, we might want to [know](https://ourworldindata.org/life-expectancy#what-drives-improvements-in-life-expectancy) how much income level affects life expectancy, and even compare that to the effect of sex and healthcare expenditure. This is an area of statistics that quickly grows in complexity (see e.g. [Bayesian probabilistic modeling](https://doi.org/10.1038/s43586-020-00001-2)). For this short introduction, we will thus only limit ourselves to the most simple of methods, intended to just convey the general gist of what these are about.

When wanting to evaluate the relationship between two numerical variables (e.g. life expectancy and healthcare spending), the simplest approach is to look at their correlation. Correlation measures the extent to which the variables are linearly related, i.e. have a relationship where if one variable grows a certain amount, the second variable either grows or diminishes a proportional amount (e.g. that for every 100 million spent into healthcare, life expectancy would increase by a year - note also that as stated, correlation only accounts for linear relationships, so, for example, would not be able to model diminishing returns in healthcare spending, etc).

{% hint style="info" %}
Assignment

* To get a better idea of how correlation works, play around with this [visualization](https://rpsychologist.com/correlation/). For example, think of X as the size of ones' hand, and Y as their height. If the two are correlated, and you measure both the height as well as hand size of people, a large hand size (large X value) should also lead to a large Y value (= tall height).
* Once you understand how correlation works, ponder what it means by looking at [spurious correlations](https://www.tylervigen.com/spurious-correlations) found in real-world data. The take-home message here is that [correlation does not imply causation](https://en.wikipedia.org/wiki/Correlation_does_not_imply_causation). Instead, there are multiple ways through which a correlation can appear, including for example a common external cause for both, or again merely due to random chance.
{% endhint %}

Stepping on from correlation, one may want to start building a formal model of the data, through which one could posit and verify laws about the world that gave rise to it. While such models can grow increasingly complex (again see e.g. [Bayesian probabilistic modeling](https://doi.org/10.1038/s43586-020-00001-2)), it is good again to start with the simplest of such models: a linear regression model. Here, the idea is to formally code the linear relationships sought for through correlation. For example, to come up with a formula that the height of a person is 50cm+8times their hand size in cm (height=50+8\*hand size).

{% hint style="info" %}
Assignment

* To get a better idea about linear regression, go look at [regression explained visually](https://setosa.io/ev/ordinary-least-squares-regression/) and play around with it.
* Finally, as a bridge toward computational data analysis approaches, look at [principal component analysis explained visually](https://setosa.io/ev/principal-component-analysis/). In this approach, the viewpoint switches from describing, comparing or modelling data on given axes into instead using statistical computation to 1) figure out what axes in the data are important in the first place and 2) to automatically discover the most important patterns (or more precisely, most important by a certain precise definition concerning axes of maximal variance) in the data overall.
{% endhint %}
