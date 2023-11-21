---
layout: page
title: SynDiffix
permalink: /syndiffix
nav: true
---

**SynDiffix** is an open-source Python package for generating statistically-accurate and strongly anonymous synthetic data from structured data. Compared to existing open-source and proprietary commercial approaches, **SynDiffix** is

- many times more accurate,
- has comparable or better ML efficacy,
- runs as fast or faster,
- has stronger anonymization.

A complete description of **SynDiffix**, including its operation, performance, and anonymity, can be found on [arXiv](https://arxiv.org/abs/2311.09628). See [github.com/diffix/syndiffix](https://github.com/diffix/syndiffix).

Programming with **SynDiffix** can be as easy as:

```py
from syndiffix import Synthesizer

df_synthetic = Synthesizer(df_original).sample()
```

## Use Cases

Synthetic data has two primary use cases:

1. Descriptive analytics (histograms, heatmaps, column correlations, basic statistics like counting, averages, standard deviations, and so on).
2. Machine learning (building models, extending datasets, etc.)

While **SynDiffix** serves both use cases, it is especially good at descriptive analytics. The quality of descriptive analytics is many times that of other synthetic data products.

## Usage

Obtaining this accuracy improvement, however, requires a different usage style compared to other products. The intended usage style of other products is "*one size fits all*": a single synthetic dataset serves all use cases. By contrast, with **SynDiffix**, a different *tailored* synthetic dataset should be produced for each use case.

For instance, suppose the analyst is interested in the correlation between columns A and B. With other synthetic data products, one would synthesize the complete table, and then measure the correlation between columns A and B. With **SynDiffix**, one would create a synthetic table consisting of only those two columns and obtain much better results.

**SynDiffix** has anonymization mechanisms that allow for literally thousands of column combinations without compromising anonymity. This is not the case with other products, where anonymity is weakened with each new data synthesis.