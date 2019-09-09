---
title: "Prismatica Core C2 Components"
sitemap: false
layout: posts
classes: wide
permalink: /diagon/
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

Diagon is the default C2 toolset of Prismatica Project. The primary implant for Diagon is Gryffindor a JavaScript-based implant that leverages Windows Scripting Host (WSH) for execution. Gryffindor also has the capability to load and execute arbitrary .NET assemblies through the DotNetToJScript project.

![Screenshot](/assets/images/demo3.png)

## Base Gryffindor Commands

Gryffindor includes custom WSH, COM, and .NET post-exploitation capabilities however the implant also supports the ability to `InvokeAssembly` for futher post exploitation capability. Gryffindor includes two core .NET assembly frameworks actualized through DotNetToJScript:

- Mimikatz
- SharpSploit

```
===========================
Gryffindor Commands:
===========================
help - Show this information
cat - Show file contents
type - Show file contents
cd - Change directory
ls - Show directory contents
dir - Show directory contents
die - Exit session
kill - Exit session
set - Modify payload settings
 - interval <ms>
 - sleep <ms>
 - jitter <percent>
show - Display payload information
 - settings <ms>
upload - Upload a file to the target system
download - Download a remote file from the target system
spawn - Instantiate a new session on the target system
   - Example Usage: spawn <target-ip> <user> <password>
WMIExecute - Instantiate a new session on the target system
   - Example Usage: WMIExecute <target-ip> <cmd> <user> <password>
hashdump - Use Mimikatz to dump SAM hashes
InvokeAssembly - Run an payload from within a loaded .NET assembly (Defaults:SharpSploit)
   - Example Usage: InvokeAssembly -Entry SharpSploit.Execution.Shell -Module ShellExecute -Args ('calc.exe','','','')
LoadAssembly - Load an arbitrary .NET assembly payload
type -
Other commands sent to Gryffindor are executed in the Windows cmd.exe shell.
===========================
```

## Starting a Listener
Before establishing remote access to a target system it is important to instantiate a listener for the implant to connect into. Click on the *headphones* icon to access the listeners panel. Next, click start listener to instantiate a basic http listener in Oculus.

![Screenshot](/assets/images/listeners.png)

As seen above Diagon provides a direct staging command; however, standalone .js payloads can be generated as seen below.

## Generating a Payload
Click on the *factory* icon to open the backdoor factory modal window. Generated payloads will appear in the current user's home/.prismatica directory on both Windows and Linux operating systems.

![Screenshot](/assets/images/demo3.png)

<br />


{% include feature_row %}
