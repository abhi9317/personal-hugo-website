---
summary: Building a Bayesian updater app to help with updating beliefs about the world.
draft: false
authors: []
lastmod: 2020-12-13T00:00:00.000Z
title: Updating beliefs
subtitle: How to make Bayesian updates to your beliefs about simple events in a
  (slightly) more accurate manner
date: 2020-12-13T00:00:00.000Z
featured: false
tags: []
categories: []
projects: []
image:
  caption: ""
  focal_point: ""
  placement: 2
  preview_only: false
---
I first came across the concept of Bayesian statistics a couple of years ago and thought it was a bit strange that I'd never actually been exposed to it in any depth during my academic life through the 2010s (which involved a fair bit of statistics and psychometrics). 

In simple terms, Bayesian thinking (as opposed to frequentist thinking) relies on codifying your beliefs about the world (often in some kind of probability estimate) and then "updating" or changing your probability estimate in response to new data. This approach is quite different from the more conservative frequentist approach where there is a "default state" that isn't really defined by any prior beliefs about the world (it is just a conservative guess of what the world is like that varies by context. Also known as the null hypothesis). 

For instance, let's say we wanted to understand whether smoking 10 packs a day is likely to cause lung cancer. In a Bayesian world, we might have some "prior" (belief) about the probability of this relationship being true. I would then observe some relevant data (say lung cancer occurence in people who smoked and didn't smoke) and then update my belief (or probability that the smoking-cancer relationship is true). Let's ignore the math of how the update happens to the prior for the moment. 

By contrast, In a frequentist world, we would assume that smoking does NOT cause cancer (this is a conservative belief) and essentially check if the data we've collected is what we'd expect if that statement was true. If it doesn't, there is probably something else going on (an alternative hypothesis). Of course, it is worth noting that this example is a gross simplification that ignores essentially all aspects of causal inference that we'd think about if we were actually trying to establish a causal relationship between smoking and cancer, but for now, it will do. 

In summary, frequentist and Bayesian approaches can be thought of as cousins that have different strengths and weaknesses that are appropriate for different contexts. To illustrate, I sometimes like frequentist approaches because they're conservative and make it easy to avoid the issues that come with having a "bad" or inaccurate prior (belief). On the other hand, Bayesian approaches are just easier to think about practically for everyday questions and for events that aren't repeated much. Furthermore, I generally find it more intuitive and useful to interpret Bayesian methods of quantifying uncertainty (credible intervals) as opposed to frequentist methods (confidence intervals). 

That being said, one thing I have struggled with is understanding exactly *h*owto update priors in response to new data. The related math can range from straightforward to quite challenging, especially when there are no analytic solutions. However, over time, I have found that most things I use Bayesian thinking for can be boiled down to a simple model of where there is an event X and I'm principally concerned with the probability of event X happening or not happening. In response, I built a simple Bayesian updater helper app that helps me update my beliefs about these types of events in an appropriate manner. Of course, this won't save anyone from "bad" priors but I hope it makes the exact updating process a little less of a black box (even if I haven't fleshed out the math here). 

\