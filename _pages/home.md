---
layout: about
title: Home
subtitle:
permalink: /
news: true  # includes a list of news items
social: true  # includes social icons at the bottom of the page
---

## Open source tools for anonymizing structured data

Open Diffix is an open source project developing tools for anonymizing structured data.

### SynDiffix

Our flagship tool is [**SynDiffix**](/syndiffix), a Python package for generating statistically accurate and strongly anonymous synthetic data from structured data. **SynDiffix** is:
* **one to two orders of magnitude more accurate** than other open-source tools, and
* **five to ten times more accurate** than the best commercial products. 

SynDiffix is particularly well suited to **descriptive analytics use cases**. Nevertheless, it works for ML use cases as well.

The current release is the first release. We are planning many new features. If you would like to request features, or need help or advice, you may contact us at [hello@open-diffix.org](mailto:hello@open-diffix.org). You may also post bug reports or feature requests as GitHub issues at [github.com/diffix/syndiffix](https://github.com/diffix/syndiffix).

### pg_diffix

**pg_diffix** is a PostgreSQL extension that gives aggregate anonymized answers to SQL queries. Advantages over **SynDiffix** include:

* Faster and more scalable
* Supports untrusted users
* Supports back-end data for applications

**pg_diffix** only returns aggregate answers (column values and associated counts) to a very limited subset of SQL. It is far less flexible than **SynDiffix**. See [github.com/diffix/pg_diffix](https://github.com/diffix/pg_diffix).

Development on **pg_diffix** is currently paused. If you are interested in a project using **pg_diffix**, please contact us at [hello@open-diffix.org](mailto:hello@open-diffix.org).