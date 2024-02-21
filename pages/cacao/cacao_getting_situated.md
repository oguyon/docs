---
title: cacao - Getting Situated
keywords: documentation theme, jekyll, technical writers, help authoring tools, hat replacements
last_updated: Feb 20, 2024
tags: [getting_started]
summary: "cacao - Getting Situated"
sidebar: cacao_sidebar
permalink: cacao_getting_situated.html
folder: cacao
---


CACAO is a plugin of the milk package, which provides the building blocks for deploying realtime processes with low-latency interprocess communication, and also provides the user interfaces and controls to configure and operate the AO control loop.


# cacao Loops


CACAO can run multiple AO loops, which may or may not interact. Each loop has a unique number, name, and root directory. To see which loop(s) are currently installed on a system, run:

```bash
cacao-loops
```

An example output is:


<pre>
cacao loops on system :

LOOP  2 using DM 00 ( 336 x 1 )  NAME: maps
rootdir     : /mnt/data0/WORK/AOloop-cacao/maps-rootdir
Last access script : /usr/local/milk/bin/cacao-fpsctrl-logprocess
Last access time   : 2023-09-29 18:17:24.566123595 -1000

SCRIPT /usr/local/milk/bin/cacao-loops  Success
</pre>

<span class="label label-default">Default</span>
<span class="label label-primary">Primary</span>
<span class="label label-success">Success</span>
<span class="label label-info">Info</span>
<span class="label label-warning">Warning</span>
<span class="label label-danger">Danger</span>


{% include note.html content="This is a Note
" %}


{% include tip.html content="This is a Note
" %}

{% include warning.html content="This is a Note
" %}

{% include important.html content="This is a Note
" %}




# Running Commands


Most operations are done by running cacao scripts within the loop root directory (shown as rootdir in the example above). To get a list of all cacao scripts, run:

```bash
cacao-commands
```

Each command can be safely run with the -h option to print help.
Most cacao commands start by scanning the local directory for required files and environment variables, and will exit if requirements are not satisfied. To run this check alone, run:

```bash
cacao-check-cacaovars
```

The command will fail if not run in a loop's rootdir. Running the command is a good way to check what type of AO loop is configured.

{% include image.html file="cacao-check-cacaovars.png" alt="Jekyll" caption="This is a sample caption" %}



# Deploying an AO loop



CACAO comes with a few example AO loops, used on actual AO systems and maintained by the corresponding AO groups. To deploy one of the examples, run cacao-loop-deploy. Run with the -h option for help and brief description of the examples.








{% include links.html %}
