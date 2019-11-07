---
title: "gig"
date: 2019-11-04T23:46:44+01:00
draft: false
---

## Description

My take on learning GoLang a bit more.

I needed a goal to build towards, and setting the goal to build the most un-necessary tool ever (since it basically can be replaced with and alias in your shell of choice) was perfect.

And so, *gig* was born.

## What is it?

*gig* (Git IGnore) is a tool built in Go, which works based on the fantastic website gitignore.io

The concept was to have a tool that you could query the websites "api" and get a .gitignore file downloaded based on the languages you gave it as input.

It also comes with a **configure** command which would get the latest version of the language definitions in gitignore.io

The command **list** would list all available languages (and input parameters for searching/greping).

And lastly, **generate** would generate a .gitignore file based on languages passed as input parameters.

## Where can I get it myself?

Head on over to: [gig](https://github.com/agerro/gig)