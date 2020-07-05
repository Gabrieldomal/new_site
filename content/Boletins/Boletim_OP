---
title: "Music order - Random forest"
date: 2020-04-16T00:18:58-03:00
draft: false
toc: false
images:
tags: 
  - untagged

---

Here is a model that my friend Filipe Côgo and I built. Our idea was to take the features of each track, and use it to predict what the feature of the next track of each album would be.

An awesome idea that Filipe gave was to compute the cumulated tempo, energy and valence from track $1$ to track $n$. This would give us a 'historical overview' of the tempi, energy, and valence that had been used in each album. 

The theoretical implication of this is still in debate, but we could argue that, by looking at the past cumulated tempo of each track, we would have a better idea of what is to come next.

Well, one thing that should be noted before we jump into the results is that we categorized every single variable of ours. Tempo, loudness, energy, valence and danceability were therefore labeled after employing a Jenks Natural Break optimization algorithm.

Here is what we found:

![](/auc.png)

Seems like we are doing a reasonable job ad finding out what the next song is, based only on the features of the past songs. Let us continue our work and see what comes next.

