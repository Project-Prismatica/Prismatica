---
title: "C2 Architecture"
sitemap: false
layout: single
classes: wide
permalink: /overview/
feature_row:
  - image_path: /assets/images/logo.png
    alt: "placeholder image 1"
    title: "C2 Architecture"
    excerpt: "Learn more about C2 architecture and concepts"
    url: "/overview/"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: /assets/images/term.png
    alt: "placeholder image 2"
    title: "Prismatica API"
    excerpt: "Project Prismatica is built around the concept of Emergence. Explore the Emergence API!"
    url: "https://documenter.getpostman.com/view/1609493/7TT8UqJ?version=latest"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: /assets/images/logo.png
    title: "UI and Implants"
    excerpt: "Everything you wanted to know about Gryffindor and Diagon"
    url: "/diagon/"
    btn_label: "Read More"
    btn_class: "btn--primary"
---

It is the golden age of C2! As a result of the major strides that have been recently accomplished by the information security community there are now more implant frameworks than ever! One downside of this incredible opportunity is the drift in terminology. This page discusses C2 concepts as they relate to the Prismatica Project.

- **Payload:** A self-encapsulated action that can be executed on a target in order to accomplish an exploitative objective. This could be used to establish an agent.
- **Agent:** A mechanism that provides interactive remote access to a target system. The default implant for Prismatica is Gryffindor.
- **Implant:** A mechanism that provides interactive remote access to a target system. The default implant for Prismatica is Gryffindor.
- **Transport:** A method or channel to enable communication between the C2 server and implant.
- **Listener:** A server that resides between the Emergence API and active implants.
- **Interface:** The control component providing operators with interactive access to the C2 system. The default interface for Prismatica is Diagon.
- **PostEx Language:** A language library supported by a given implant for modular post-exploitation tooling. i.e. SharpSploit (.NET), Impacket (Python)

<br />

{% include feature_row %}
