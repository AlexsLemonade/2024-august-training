---
title: Workshop Logistics
nav_title: Logistics
---

**Table of contents**

* TOC goes here
{:toc}

{% if site.workshop_type == "in-person" %}
    {% include_relative local-participant-information.md %}
{% endif %}

## Workshop Structure

Our goals for the workshop include the following:

* You will be introduced to
{% case site.workshop_content %}
{%- when "intro-r" -%}
 the R programming language
{%- when "intro-single-cell" -%}
  the R programming language and the fundamentals of scRNA-seq analysis
{%- when "intro-bulk" -%}
  the R programming language and the fundamentals of bulk RNA-seq analysis
{%- when "advanced-single-cell" -%}
  advanced scRNA-seq analyses
{%- endcase %}
through a series of hands-on, interactive lessons.
* You are able to ask questions and receive 1:1 assistance as needed during instruction. Because our instruction is almost entirely through hands-on lessons, we want to make sure we can help you through any difficulties or errors you may encounter.
* You have the opportunity to practice the skills you learn during instruction in consultation sessions with the support of your instructors, and/or using exercise notebooks we have provided.
* You receive consultation about the data you are working with to answer your research questions.
* You have opportunities to interact with other participants working on similar problems.

The next sections are designed to give you an idea of what your participation in the workshop will be like and outline the communication processes we have developed in service of these goals.

### Instruction sessions

**During instruction sessions**, an instructor may present some slides to introduce the material, and then they will instruct you to navigate to the RStudio Server (<https://rstudio.ccdatalab.org>), [enter your RStudio login credentials](../software-setup/rstudio-login.md#rstudio-server-set-up), and guide you through the interactive lesson.
Typically instructors will prompt you to navigate to a specific R Notebook file, and you will execute steps at the same time as your instructor.
You will have access to [a private training-specific Slack channel](../software-setup/slack-procedures.md#using-the-training-specific-channel) in [Cancer Data Science Slack](https://www.ccdatalab.org/slack) that you can use as a forum to post questions.
This channel will be monitored by instructors.

{% if site.workshop_type == "remote" %}

For remote workshops, instruction will occur over Zoom, and sessions will be [recorded and distributed to course participants](../software-setup/zoom-procedures.md#zoom-recording) (not posted publicly).

#### Your instructors' roles during instruction

**During instruction**, your instructors function in one of three roles:

* One person leads the hands-on exercise.
* One person is the host of the Zoom meeting and is responsible for administering that platform.
The host makes sure any time-sensitive questions or problems are addressed during instruction and is responsible for pairing anyone that needs 1:1 assistance with an available instructor.
The host may also group you into breakout rooms for exercises as needed.
* All other instructors are on-hand to monitor the training specific Slack channel, answer questions, provide 1:1 assistance, or help with technology or login issues.

We will clearly identify the role of each instructor at the beginning of instruction.

#### Using communication platforms during instruction

To make sure all your needs are addressed, we've put together a plan for how the communication platforms we use during instruction are intended to work together.

You can read more about how we use Zoom and Slack in the [Zoom procedures](../software-setup/zoom-procedures.md) and [Slack procedures](../software-setup/slack-procedures.md) documentation, but we've put together the table below to serve as a guide at a glance.

| If this happens | Use this platform |
|-----------------|-------------------|
| I need something clarified before we move on with instruction | Use Zoom chat to message the meeting host with your question or use the `Raise Hand` button on Zoom|
| I am stuck with an error message and am no longer able to follow the hands-on exercise | Use Zoom chat to message the meeting host to [ask for 1:1 assistance](../software-setup/zoom-procedures.md#using-zoom-during-instruction) - they will pair you with an available instructor in a [Zoom breakout room](../software-setup/zoom-procedures.md#using-breakout-rooms) |
| I have a general or conceptual question that can be addressed later in the lecture or asynchronously | Post in the [training-specific Slack channel](../software-setup/slack-procedures.md#using-the-training-specific-channel) |
| I am having trouble with my login credentials | [Use Slack to direct message a Data Lab staff member](../software-setup/slack-procedures.md#using-direct-messages-during-training) that is not leading instruction or the host of the Zoom meeting |
| I am having technical difficulties that preclude me from using Zoom and Slack | Email [training@ccdatalab.org](mailto:training@ccdatalab.org) |

{% endif %}
### Consultation sessions

During consultation sessions, you can work through exercise notebooks included as part of the course, with your own data, or with publicly available data related to your research.

The main method we use for communication during consultation sessions is Slack.
You can use the training-specific private channel to post errors, get help with debugging, and interact with other participants as they work through exercises.
We strongly recommend you follow these [**guidelines for posting errors**](./posting-errors-guidelines.md) so you can maximize others' abilities to help you resolve your error.

{% if site.workshop_type == "remote" %}

Zoom is the platform that we use to facilitate sharing your screen with an instructor, which may come in handy during consultation.
If you need assistance and would like to share your screen, an instructor will initiate a Zoom call in Slack.

{% endif %}


#### Using communication platforms during consultation sessions

Our goal during consultation days is to make sure you get the support you need from instructors, to facilitate peer-to-peer learning, and to maximize the information that is available to everyone in a form that is discoverable in the future.
For these reasons, the main process for communication on consultation days is the training-specific Slack channel.
Again, we recommend following these [guidelines for posting errors](posting-errors-guidelines.md) when requesting help for errors you encounter in your code.

_Remember – if you have a question, another person in the course almost certainly has the same question!_

{% if site.workshop_type == "remote" %}

Your instructors will be available via Slack during the consultation sessions listed in the [workshop schedule](SCHEDULE.md).
You may also remain in the Zoom meeting used for the day's instruction session, which will be used for breakout room functionality for grouping participants that want to work together.
If you need to share your screen with an instructor during a consultation day, the instructor will [start a Zoom meeting and you will be able to join from Slack](../software-setup/zoom-procedures.md#using-zoom-during-consultation).

You can read more about how we use Zoom and Slack in the [Zoom procedures](../software-setup/zoom-procedures.md) and [Slack procedures](../software-setup/slack-procedures.md) documentation. We've put together the table below to serve as a guide at a glance.

| If this happens | Use this platform |
|-----------------|-------------------|
| I have a question about yesterday's instruction | Post in [the training-specific Slack channel](../software-setup/slack-procedures.md#using-the-training-specific-channel) |
| I have a question about an exercise notebook | Please use the [guidelines for posting for help](posting-errors-guidelines.md) and post in the [training-specific Slack channel](../software-setup/slack-procedures.md#using-the-training-specific-channel)|
| I am having an issue that requires me to share my screen | Post in [the training-specific Slack channel](../software-setup/slack-procedures.md#using-the-training-specific-channel) - an instructor will initiate a Zoom meeting that you can [join from Slack](../software-setup/zoom-procedures.md#joining-a-zoom-call-from-slack) |
| I would like to be paired up with other participants | Post in [the training-specific Slack channel](../software-setup/slack-procedures.md#using-the-training-specific-channel) |
| I have a question that is **_highly specific_** to my data | [Use Slack to direct message a Data Lab staff member](..software-setup/slack-procedures.md#using-direct-messages-during-training) |
| I am having trouble with my login credentials | [Use Slack to direct message a Data Lab staff member](../software-setup/slack-procedures.md#using-direct-messages-during-training) |
| I am having technical difficulties that preclude me from using Zoom and Slack | Email [training@ccdatalab.org](mailto:training@ccdatalab.org) |

{% endif %}

### Participant presentations

On the last afternoon of the workshop, we will reconvene after the consultation session for participant presentations.
You will be invited to give a short (5 minutes or less) presentation on what you worked on during the week to the rest of the group.
This is meant to be a _low-pressure opportunity_ to reflect on what you've learned!
The content and format of the presentation is entirely up to you.
Here are some examples of what people have presented in the past at our workshops:

* Talked through part of an exercise notebook, highlighting where they ran into issues and how they figured it out
* Shown a visualization they made with their own data
* Walked through a set of slides that included tools they've used in the past and how they compare to what they learned during the workshop
* Identified some publicly available data sets relevant to their scientific questions and talked about next steps

{% if site.workshop_type == "remote" %}

These presentations will take place in the same Zoom meeting used for the rest of the workshop.
When it is your turn to present, you will [share your screen on Zoom](../software-setup/software-setup-instructions.md#enabling-screen-share) and unmute yourself.

{% endif %}
