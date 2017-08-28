---
layout: post
title: Replicate Distribution on Perfherder
subtitle: And GSoC has come to an end
tags: [mozilla, gsoc, perfherder]
---

I would have put up this post a tad early had the Game of Thrones season finale not consumed my entire afternoon today. What an episode! It’s saddening that the final season of the show requires a two-year long wait.

All the code which I have written for GSoC has been merged!

After squashing [Bug 1273513](https://bugzilla.mozilla.org/show_bug.cgi?id=1273513) and [Bug 1164891](https://bugzilla.mozilla.org/show_bug.cgi?id=1164891), I started working on [Bug 1350384](https://bugzilla.mozilla.org/show_bug.cgi?id=1350384) which constituted a major portion of my GSoC project.

Up till now, [Perfherder](https://wiki.mozilla.org/EngineeringProductivity/Projects/Perfherder) provided aggregated results and graphical visualization of various [test suites](https://wiki.mozilla.org/Buildbot/Talos/Tests) in its comparison view, but not for the individual replicates that are used to generate them. For tests where there is a large natural variation in these individual numbers, it can be difficult to determine if there is regression when the summarised values change because there could be many different underlying reasons for that. For these cases, a detailed view of the individual test results could be extremely helpful.

These individual test results can now be analysed using the new replicate view.This can be accessed from the subtest comparison:


<figure>
	<img src="/images/ReplicatePost/subtest.png" >
	<figcaption align="center">Link to the replicate distribution view from subtest comparison.</figcaption>
</figure>

In this view, bar charts are used to compare the replicate results. The values for  the base and original projects run-side by-side in the order in which they were obtained.

<figure>
	<img src="/images/ReplicatePost/replicateView.png" >
	<figcaption align="center">The new replicate view.</figcaption>
</figure>

This feature is currently available for Talos framework when two specific revisions are compared.

With this bug comes an end to Google Summer of Code. It was a truly amazing experience. Over this summer, I have developed a better understanding of how Perfherder works and my front-end development skills have improved a lot. I got a chance to fly to San Francisco and attend the All hands meeting. The best part about GSoC was the fact that the code which I have written would make an impact on how performance testing is done in Mozilla.

In other news, my seventh semester in the college has begun. There's so much to explore. This semester, I'll try my hand on Artificial Intelligence and Cryptography. And probably a new Mozilla project too.

I hope you find the features which I have added to Perfherder useful. :)
