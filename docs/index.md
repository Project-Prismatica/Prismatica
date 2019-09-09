---
title: "Project Prismatica"
layout: splash
permalink: /
date: 2016-03-23T11:48:41-04:00
header:
  overlay_color: "#000"
  overlay_filter: "0.3"
  overlay_image: /assets/images/splash.jpg
  actions:
    - label: "Download"
      url: "https://github.com/Project-Prismatica/Diagon/releases"
  caption: "Image courtesy of [Open Security](https://opensecurity.com/)"
excerpt: "C2 - Modular, agnostic, and better than ever."
intro:
  - excerpt: 'Project Prismatica is a focused framework for Command and Control that is dedicated to extensibility. Our core objective is to provide a convenient platform with modular **Transports**, **Backends**, and **Implants** to enable rapid retooling opportunities and enhance Red Team operations.'

introimg:
  - image_path: /assets/images/demo.gif
    alt: "placeholder image 2"
    type: "center"
    title: "Having your cake and eating it too"
    excerpt: "Prismatica was designed from the ground up to be flexible, modular, and extensible. While the system does have core C2 components, extending and integrating 0-day capabilities has never been easier!
    Watch the Security Weekly episode below to learn how to make a python implant that takes advantage of all of Prismatica's capability in under 15 minutes."
    url: "https://youtu.be/SUu_VtJo19Y"
    btn_label: "See the Video"
    btn_class: "btn--primary"
introimg2:
  - image_path: /assets/images/demo2.png
    alt: "placeholder image 2"
    type: "center"
    title: "Cross-Platform, Multiuser, Scriptable"
    excerpt: 'Prismatica supports multiple users operating from Linux, Windows, and MacOS systems to enable red teams to maximize their efficency while on engagements.
    When handling large numbers of agents filtering numerous filtering options are available to enhance OnNet target interaction.'
introimg3:
  - image_path: /assets/images/demo3.png
    alt: "placeholder image 2"
    type: "center"
    title: "Prismatica Implants"
    excerpt: 'Prismatica includes a **Backdoor Factory** to enable the rapid development and deployment of implants.
    The default Prismatica implant, Gryffindor, is written in WSH JavaScript and leverages .NET Post-Exploitation libraries through DotNetToJScript.'
outro:
- image_path: /assets/images/demo4.png
  alt: "placeholder image 2"
  type: "center"
  title: "Open Source | Open API | Open Security"
  excerpt: 'Prismatica is fully open source and open API. The C2 UI (Diagon) and primary implant (Gryffindor) are not intended to be the ONLY way to interface with Prismatica, but simply one option. Checkout the **documentation** for developer information'
  url: "https://documenter.getpostman.com/view/1609493/7TT8UqJ?version=latest"
  btn_label: "Documentation"
  btn_class: "btn--primary"
---

{% include feature_row id="intro" type="center" %}
{% include feature_row id="introimg" type="left" %}
{% include feature_row id="introimg2" type="right" %}
{% include feature_row id="introimg3" type="left" %}
{% include feature_row id="outro" type="center" %}
