---
title: "Getting Started"
sitemap: false
layout: single
classes: wide
permalink: /guides/
header:
  image: /assets/images/header.png
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

Prismatica is more than just another C2 tool it is meant to be an ecosystem. The project is focused around agnostic integration of information security toolsets to allow rapid prototyping, scripting, and automation of operator objectives. This goal grows out of the concept of Emergence where the collective intelligence of all tools and systems should be greater than the sum of their parts.

What does that mean exactly? Prismatica is dedicated to having your cake and eating it too. Prism applications can all be cross integrated and if a newer better way of performing an action is developed it can be integrated with the framework to automatically yield all of the capabilities of other apps within the ecosystem.

- Overview
- Using Prismatica
- Prism Implants
- Pismatica Marketplace
- Concepts and Terminology
- Emergence API

# Getting Started
To get started with Prismatica you will need to spin up an Emergence server to bind all subcomponents together across a shared data model. Emergence servers can be spun up quickly using Docker. Alternately, it can be executed manually using the `npm install` and `npm start` commands. To run Emergence within a Docker container the `docker` and `docker-compose` commands must be installed. Installing Docker:

**On Windows:** [Get Docker](https://docs.docker.com/docker-for-windows/install/)

**On Linux:**
```
apt install docker.io
apt install docker-compose
```

**Run Emergence:**
```
git clone https://github.com/Project-Prismatica/Emergence.git
cd Emergence
docker-compose up
```

Now that Emergence is running you are ready to start up Prism Apps! Diagon and Oculus are a good place to start.

**Installing Diagon:**

Diagon can be downloaded at the following link: [Diagon](https://github.com/Project-Prismatica/Diagon/releases)

![Screenshot](/assets/images/demo.gif)

You will need to configure the Diagon settings with the IP address of the system where Emergence is running. Then to setup listeners you will need to run Oculus.

**Installing Oculus:**

```
git clone https://github.com/Project-Prismatica/Oculus.git
cd Oculus
python oculus.py
```

Now you're all ready to rock and roll! Happy Hacking!

## Prismatica Application Marketplace

- [Diagon](https://github.com/Project-Prismatica/Diagon) The Diagon Attack Framework is a Prismatica application containing the Ravenclaw, Gryffindor, and Slytherin remote access tools (RATs).
- [Emergence](https://github.com/Project-Prismatica/Emergence) The Emergence fabric is an interface where interaction and integration of disparate information security subsystems gain combined intelligence.
- [Oculus](https://github.com/Project-Prismatica/Oculus) Oculus is a malleable python-based C2 system allowing for instantiation of listeners for the purpose of communication with remote access tools (RATs).
- [Prism Launcher]() The package manager for Prism Apps (Releasing at WWHF)
- [Prism Project Manager]() Project management, findigns, and reporting tool (Releasing at WWHF)
- [Acheron](https://github.com/Acheron-VAF/Acheron) Acheron is a RESTful vulnerability assessment and management framework built around search and dedicated to terminal extensibility.
- [Tiberium](https://github.com/0sm0s1z/Tiberium/releases) A Command and Control scanning tool


## Simple Python Beacon

```py
import requests
url = 'http://localhost:80/'
payload = "{\n\t\"type\": \"b\",\n\t\"agentid\": \"24464303\"\n}"
headers = {}
response = requests.request('POST', url, headers = headers, data = payload, allow_redirects=False, timeout=undefined, allow_redirects=false)
print(response.text)
```

<br />


{% include feature_row %}
