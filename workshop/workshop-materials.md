---
title: Workshop Materials
nav_title: Materials
---

### Slides

PDF versions of the slides we present in this workshop can be found in the [slides directory]({{site.repository_url}}/tree/main/slides) of the `{{site.repository}}` repository, and are also linked to directly from the [schedule](SCHEDULE.md).

### Module Structure

In the `training-modules` repository, each individual module is found in a subfolder of the main page, along with folders containing cheat sheets and setup instructions.

In this training workshop, we will be using the following modules:

{% case site.workshop_content  %}
{% when "intro-r" %}
  - [Intro to R and the Tidyverse](https://github.com/AlexsLemonade/training-modules/tree/{{site.release_tag}}/intro-to-R-tidyverse)
{% when "intro-single-cell" %}
  - [Intro to R and the Tidyverse](https://github.com/AlexsLemonade/training-modules/tree/{{site.release_tag}}/intro-to-R-tidyverse)
  - [Intro to single-cell RNA-seq](https://github.com/AlexsLemonade/training-modules/tree/{{site.release_tag}}/scRNA-seq)
{% when "intro-bulk" %}
  - [Intro to R and the Tidyverse](https://github.com/AlexsLemonade/training-modules/tree/{{site.release_tag}}/intro-to-R-tidyverse)
  - [Intro to Bulk RNA-seq](https://github.com/AlexsLemonade/training-modules/tree/{{site.release_tag}}/RNA-seq)
{% when "advanced-single-cell" %}
  - [Advanced single-cell RNA-seq](https://github.com/AlexsLemonade/training-modules/tree/{{site.release_tag}}/scRNA-seq-advanced)
{% endcase %}

The link(s) above will take you to our `training-modules` GitHub repository where all materials are stored, but we will also directly provide you will all of these materials as part of the workshop.


The layout of the `training-modules` folders follow a common general structure.

<img src="https://github.com/AlexsLemonade/training-modules/raw/{{site.release_tag}}/module_structure_detail.png" alt="Module Structure" width="600">

In these folders, you will notice that there may be two or three versions of some notebook files.
For example, there may be a `01-intro_to_base_R-live.Rmd`, a `01-intro_to_base_R.Rmd`, and a `01-intro_to_base_R.nb.html`.

- The version with `-live.Rmd` at the end is an incomplete version of the notebook, missing some code that will be filled in during the workshop.
- The `.Rmd` file (with no `-live`) is a fully completed version of the notebook, useful for reference in case you might have missed any steps during the workshop.
- The `.nb.html` version of the file is a rendered web page of the notebook.
This file can be downloaded or viewed via the links in the README file that you will see at the bottom of the file listing for each module.

Cheatsheets that review key functions and concepts are found in the [`module-cheatsheets` folder](https://github.com/AlexsLemonade/training-modules/tree/{{site.release_tag}}/module-cheatsheets).
These are formatted both as markdown files and PDFs, with the latter likely most useful for reference.

### RStudio Server

Notebooks and data files required for participation in the workshop will be pre-loaded for each user on the RStudio server.
See [this page](../software-setup/rstudio-login.md) for more information about logging into your RStudio Server account for the first time.