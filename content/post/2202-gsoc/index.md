---
title: GSoC 2022 call
date: 2022-02-09
summary: "List of Suggested Projects for GSoC 2022."

---

<!-- https://stackoverflow.com/a/63790068 -->
<style>body {text-align: justify}</style>


### List of Suggested Projects for GSoC 2022

This is a list of projects suggested by Catalyst-Team for GSoC 2022. 
GSoC has focused on 2 types of projects this year: ~175 hours or ~350 hours to complete, the list below contains project suggestions that should meet these criteria depending also on the skill level of the participant. 
These are only suggestions, and if you have your own ideas, please discuss them on the [Catalyst Team Slack](https://join.slack.com/t/catalyst-team-devs/shared_invite/zt-d9miirnn-z86oKDzFMKlMG4fgFdZafw). 
We have a lot of talented ML practitioners in the Catalyst Team who would love to mentor good students for GSoC 2022.

- Meta tracks: examples, documentation, tests
- LR Finder API
- Poetry
- Metric Learning metrics and benchmark
- Self-Supervised Learning benchmark extension
- RecSys sequential recommenders
- Off-policy RL
- On-policy RL


See lower down on this page for more details for some of the projects listed above.


### Timeline
The timeline for GSoC 2022 is [here](https://developers.google.com/open-source/gsoc/timeline).


### How to improve your chances of being accepted
When making the difficult decision about which students to accept, we look for:

- Clear and detailed application explaining how you think the project could be done
- Relevant prior experience - machine learning, deep learning, pytorch
- Experience contributing to Catalyst or other open source ML/DL projects
- Understanding of Git and/or GitHub

----

#### Meta tracks: examples, documentation, tests

Like every open-source framework, Catalyst is actively interested in examples and documentation improvements to improve its adoption. In such a case during any listed projects below you are welcome to extend our documentation site with FAQ of your own, or [Keras-like examples](https://keras.io/examples/).


#### LR Finder API

[LR finder](https://blog.dataiku.com/the-learning-rate-finder-technique-how-reliable-is-it) is a well-known technique in the ML community to tune your initial learning rate for maximal performance. 
While Catalyst already has [its implementation with some extensions](https://github.com/catalyst-team/catalyst/blob/master/catalyst/callbacks/scheduler.py#L262) there is a place for improvement in terms of user API.

The goal of the project
- revisit LR finder implementation and add additional documentation if required
- extend [Runner](https://catalyst-team.github.io/catalyst/api/runners.html#runner) API with `find_lr` method (like `runner.train` or `runner.predict_loader` ones)
- benchmark LR finder on available examples
- write a blog post with your findings for the community


#### Poetry

The main idea of this project is to transfer Catalyst from `pip` to a `poetry`-based development environment. It includes working with installations scripts, tests, and contributions guides.
See [RP#1358](https://github.com/catalyst-team/catalyst/pull/1358) for more information.


#### Metric Learning metrics and benchmark

Catalyst Team was always inspired with the Metric Learning. For such a reason, we also have a wide variety of ML-based metrics: [CMCMetric](https://catalyst-team.github.io/catalyst/api/metrics.html#cmcmetric), [ReidCMCMetric](https://catalyst-team.github.io/catalyst/api/metrics.html#reidcmcmetric).

The goal of this project
- extend the available metrics with Normalized Mutual Information (NMI)
- implement and benchmark Mean Average Precision at R
- write a blog post with your findings for the community


#### Self-Supervised Learning benchmark extension

In addition to Metric Learning, Catalyst also has a [Self-Supervised Learning benchmark](https://github.com/catalyst-team/catalyst/tree/master/examples/self_supervised). Nevertheless, it could be improved a bit.


The goal of this project
- extend the `catalyst.contrib.datasets` with the `ImageNet1k`
- add `ImageNet1k` support to the current SSL benchmark
- add video-based dataset support to the SSL benchmark
- revisit the final results
- write a blog post with your findings for the community


#### RecSys sequential recommenders

There are [many RecSys-based examples in the Catalyst](https://github.com/catalyst-team/catalyst/tree/master/examples/recsys) already. One thing to mention - they are mainly AutoEncoders-based. For such a reason we are interested in its adoption for a wide variety of sequential recommenders also.

The goal of this project
- implement a synthetic data generator for sequential RecSys recommenders
- add RecSysDataset support to the `catalyst.contrib.data`
- implement SAS4Rec recommender
- implement BERT4Rec recommender
- implement RepeatNet recommender
- compare available Catalyst recommenders
- write a blog post with your findings for the community


#### Off-policy RL

While Catalyst already has [a few off-policy RL examples](https://github.com/catalyst-team/catalyst/tree/master/examples/reinforcement_learning), several improvements can be made.

The goal of this project
- extend available RL examples with n-step returns and categorical/quantile loss
- implement TD3 algorithm
- implement SAC algorithm
- write a blog post with your findings for the community


#### On-policy RL

While Catalyst already has [a few on-policy RL examples](https://github.com/catalyst-team/catalyst/tree/master/examples/reinforcement_learning), several improvements can be made.

The goal of this project
- improve current implementation with BatchEnv wrapper
- implement TRPO algorithm
- implement PPO algorithm
- write a blog post with your findings for the community
