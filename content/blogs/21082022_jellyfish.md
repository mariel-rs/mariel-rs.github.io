---
title: "Hello Jammy Jellyfish"
date: 2022-08-21
draft: false
author: "Mariel"
tags:
  - ubuntu
  - linux
  - en
image: false
description: "Hi there Jellyfish"
toc: true
---

This was the weekend for the so much awaited upgrade to Ubuntu 22.04.1. I 
installed Ubuntu 20.04 because it was the LTS version available and I didn't 
want to be messing around upgrades. After seeing first-hand how Windows upgrades
could be nasty, horrible or fatal, I wanted to avoid a bittersweet experience
with Ubuntu.

<!--more-->

To start with, the upgrade manager started prompting me to accept the upgrade 
for about 2 weeks now, but I didn't do it until I got confident that this major
change would not break my computer. I read many blog posts where this upgrade
is praised as one of the smoothest upgrade processes. So I gave it a go.

## Transparent upgrade
The upgrade manager showed me the amount of stuff it would do, including the
details of the packages that would install/upgrade/remove. Comparing this
against Windows upgrades, it is a transparent process. It's my first time doing
an Ubuntu upgrade, so I suppose this is the norm? 

Anyhow, back to the upgrade. Considering my home internet speed is not that 
fast, the download took around 25 minutes for _circa_ 466 packages. Installing 
them was not so fast, it was about one hour. Finally, the manager required one
reboot. 

And here we are! The upgrade was completed without any issues. The upgrade 
didn't change much of the desktop, aside for some new themes and icons added.

## Upgrade "goodies"

Despite that the upgrade went well and I didn't lose anything major, I did 
notice a couple of things that didn't work as before :grinning:

### Rhythmbox
I noticed that Rhythmbox started to misbehave after the upgrade. Rhythmbox would
play but it wouldn't "sound". It wasn't the sound drivers either, as VLC 
was playing files and radio stations fine. 

The way I fixed this, was to mute Rhythmbox on the Sound settings / Applications
section, and then unmute it. Restart Rhythmbox and voilà :raised_eyebrow:

### Launcher panel
The launcher panel on the left-hand side changed its behaviour. It used to 
show the existing instances and allow the user to launch a new application 
instance. Now the panel is simply launching new instances but you cannot see if 
you have any prior instance opened before. The way I accessed them was with the 
keyboard shortcut `Alt` + `Tab`.

The way around it was to remove the panel and use Plank instead. Plank retains
the existing functionality that I got used to on 20.04. 

## Final thoughts
It's been only a day with 22.04.1, so I haven't found much as of now. So far, it
feels faster and more stable. The upgrade was quite smooth and I am pleased that
I don't have to fix major issues because of messy upgrades. Python, Java, git,
Hugo and all my development environment tools are working as expected. It's as
if I have only rebooted the machine. 

I'll update this entry with the latest surprises I unveil :smirk: