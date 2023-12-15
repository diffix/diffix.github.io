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

Click [here](/syndiffix-mostlyai-ctgan) for a comparison of SynDiffix with Mostly AI and CTGAN.

<a href="/syndiffix-mostlyai-ctgan"> <img src="/assets/img/compare-link.png"> </a>

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

Obtaining this accuracy improvement, however, requires a different usage style compared to other products. The intended usage style of other products is "*one size fits all*": a single monolithic synthetic dataset serves all use cases. It's like expecting a vehicle to be good at city maneuverability, highway cruising, and hauling lumber.

By contrast, with **SynDiffix**, a different *tailored* synthetic dataset can be produced for each use case: like having a Smart car for the city, a Mercedes S-class for the highway, and a Ford F-150 for hauling stuff.

{% include image.html src="/assets/img/usage.png" alt="SynDiffix usage style" max_width="550px" %}

For instance, suppose the analyst is interested in a heatmap with columns C and E. With other synthetic data products, one would synthesize the complete table, and then make the heatmap with only columns C and E. With **SynDiffix**, one would create a synthetic table consisting of only those two columns and obtain much better results.

**SynDiffix** has anonymization mechanisms that allow for literally thousands of column combinations without compromising anonymity. This is not the case with other products, where anonymity is weakened with each new data synthesis.

## Accuracy

Here are three scatter plots showing the synthetic and real points for a 2-column dataset for **SynDiffix**, the commercial product MostlyAI, and the open-source implementation of CTGAN by SDV.

{% include image.html src="/assets/img/scatter.png" alt="SynDiffix accuracy" max_width="600px" %}

The black dots are the original data and the blue dots are the synthetic overlaid on the original data. SynDiffix is far more accurate. More examples can be found in the [arXiv paper](https://arxiv.org/abs/2311.09628).

## Anonymity

We measured the anonymity of **SynDiffix** and a number of other products using the [Anonymeter](https://github.com/statice/anonymeter) tool developed by Statice. The following figure shows the results of measuring the effectiveness of 100s of attacks over multiple different tables (again, see the [arXiv paper](https://arxiv.org/abs/2311.09628) for details). Any score below 0.5 can be regarded as having strong anonymity, and scores below 0.2 are very strong. The "noAnon" plot measures attacks against the original data, and is there for calibration.

{% include image.html src="/assets/img/privacy.png" alt="SynDiffix privacy" max_width="400px" %}

As these results show, **SynDiffix** and most of the other products have very strong anonymization with respect to the attack used by Anonymeter.