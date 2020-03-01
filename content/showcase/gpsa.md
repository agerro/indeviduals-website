---
title: "GPSA"
date: 2020-03-01T22:26:44+01:00
draft: false
---

## Description

When I moved to Gothenburg (which is a bigger city than the one I was born in and lived most of mu life) I had some trouble getting around using the buses and trams. The problem lied in knowing when to get of the bus/tram in a city where I didn't know where anything were. 
Sure, I could easily just google stuff and figure it out, but when I thought about the problem I realised that I could just automate it away.

My backgroud is Java development. When I moved into programming applicaitions for my Android phone, that knowledge came in handy.

`GPSA` was a project where I set out to get my self an application that would sound an alarm (just like the one you have when you wake up in the morning). But, instead of being based on time, I wanted it to be based on my location.

So, I built just that.

The application works just as you would set an alarm for you to wake up in the morning. But instead, you set a geografical location, to which the application (a service running in the background) would check to see if you have reached. The "reached" part about it was just basically a radius at a set distance from the target, and once you're inside of the cirle; the alarm would sound.

So, sleeping on the tram/train would now not only be dependant on time (and trains can be late here in Sweden), it would actually tell you when you are close to your destination.

## Problems I had to face

One issue was working with longitud and latitud. The issue was related to the curvature of the earth, and calculating the distance between two point on a (in an optimal situation) spherical globe. The problem relates to the sides and angles of spherical triangles.
Luckily there is a way to estimate the location, using the [Haversine formula](https://en.wikipedia.org/wiki/Haversine_formula)

## What is it?

`GPSA` is (currently only) an Android application that keep track and alarms you about your location in relation to a set target (users pick).
An geolocation based alarm application.

## Where can I get it myself?

Head on over to: [GPSA](https://github.com/agerro/gpsa)