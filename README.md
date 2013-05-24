# buzzArxiv

### Identify trends and spot interesting new physics results

For those who don’t know, arxiv.org is an online repository of scientific papers, categorized by field (experimental particle physics, astrophysics, condensed matter, etc…). Most of the pre-print articles posted to the arxiv eventually also get submitted to journals, but it’s usually on the arxiv that the word about new work gets disseminated in the community. The thing is, there’s just gobs of new material on there every day. The experimental, pheonomonolgy, and theory particle physics mailings can each have a dozen or so articles per day.

The number of submissions has been steadily increasing over the years. I organize the experimental particle physics seminar at SLAC, and I try to stay on top of new developments in the field, but it’s very hard to cull the wheat from the chaff. Most big news ends up spreading by word of mouth, or by blog, but the coverage can be spotty. **So, I started pulling the article metadata (author list, abstract, etc…) regularly in the hopes of partially automating the task of picking out results of interest by looking for outliers in the distribution of word frequencies**.

I build the arxiv corpus using a bare-bones OAI-PMH client in python which runs weekly. The text is cleaned (I use some regexes to drop the plurals, convert meta-characters, drop capitalization, etc…). The cleaned articles are stored on my laptop in a mysql database for frequency analysis (outlier detection, trend identification, plotting, etc...)
