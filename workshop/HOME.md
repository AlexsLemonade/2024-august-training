---
nav_title: Home
permalink: /
---


<img style = "padding: 0px 15px; float: right;" img src = "workshop/screenshots/CCDL_2021_Logo-x-ALSF_RGB.png" width = "300">
The **[Childhood Cancer Data Lab (Data Lab)](https://www.ccdatalab.org/)** develops tools and training programs to empower childhood cancer researchers to utilize  data to make more robust discoveries.
The Childhood Cancer Data Lab is an initiative of **[Alex's Lemonade Stand Foundation](https://www.alexslemonade.org/)**.

# {{site.training_title}}

Dates: {{site.start_date}} through {{site.end_date}}

## Getting Started


### Pre-workshop Prep

* Please review the [Code of Conduct](../code-of-conduct.md).
* If you are new to using R, we've [assembled some resources for getting starting with R](../additional-resources/R-resources.md#pre-workshop-prep-for-r-programming) that can optionally help prepare you for the workshop.
* Please review the **[software platforms](../software-setup/software-setup-instructions.md)** we will be using to familiarize yourself with our procedures.
  * You will also need to install
{%- case site.workshop_type -%}
{% when "remote" %}
`Slack` and `Zoom`
{% when "in-person" %}
`Slack`
{%- endcase -%}, as described in the link above.

* Sign up for the **Cancer Data Science** Slack workspace at <http://ccdatalab.org/slack>. Please use your full name in your profile, so we can find you easily and add you to the private meeting channel.
* Once you have been given your username and temporary password, follow [these instructions](../software-setup/rstudio-login.md) to log in to our RStudio server and change your password.

## Schedule

<!-- Introduce general schedule here -->

**For more details on the schedule for each day, [click here](SCHEDULE.md).**

## Workshop Structure

A description of our plans and goals for the workshop can be found on the [Workshop Logistics page](workshop-logistics.md). Please also refer to the [schedule](SCHEDULE.md) for information about timing and links relevant to each day.
An overview of the modules we will cover and associated links can be found on the [Workshop Materials page](workshop-materials.md).

During instruction sessions, Data Lab staff will lead you through course material using [Slack](../software-setup/slack-procedures.md) and [RStudio Server](../software-setup/rstudio-login.md).
{%- if site.workshop_type == "remote" %}
All instruction will take place over [Zoom](../software-setup/zoom-procedures.md), as described.
We will record instruction and provide it to workshop attendees so they can revisit it outside of workshop hours or in case they experience disruptions during live instruction.
{%- endif %}

During consultation sessions, Data Lab staff will be available to answer questions and provide 1:1 assistance as you work through exercise notebooks we provide or work with your own transcriptomic data.
We recommend you follow these [guidelines for posting errors](posting-errors-guidelines.md) so you can maximize others' abilities to help you resolve any errors you encounter.
