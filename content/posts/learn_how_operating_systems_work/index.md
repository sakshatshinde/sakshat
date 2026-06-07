+++
title="Learn how Operating Systems work"
description="Learn how Operating Systems work"
date=2020-04-28

[taxonomies]
tags = ["tech"]
categories = ["os", "kernel",]
+++

Operating Systems are a major part of our lives. Mobile phones, computers and the cloud — which serves as a backbone of the entire internet — utilize them every single day. However Operating Systems are not limited to these complex machines, for example `MiniOS` which is developed for Arduino. This post aims to provide a better understanding of how Operating Systems are developed in a very simplistic manner. Furthermore how various components work together to make a computer do things that we expect from it. Developing a fully fledged Operating Systems from scratch is a lot of work and a huge commitment.

We will be diving into the details of components such as Bootloaders, Kernels and Drivers which play a key role to make use of the hardware. These `low level programs`, bunched together, working in harmony is what enables us to use our computers and other devices every day

> An operating system is usually described as a piece of software which enables users to interact with a hunk of metal.

Traditionally one would say it is essentially a program which runs other programs. So that makes it the first program. In other words, everything you do on your computer is totally dependent on the Operating System, directly or indirectly. A few key components of an Operating System are:

- the Kernel
- the Bootloader
- the Drivers

These three components and many others work together to create an abstracted layer for the user by which they can interact with the machine easily. Essentially these programs are the ones who interact with the bare metal. Example when you press a key on your keyboard, the computer knows which key was pressed and does the job accordingly. Your monitor displays certain stuff depending on the given input so on and so forth. It also interacts with your RAM, CPU and other components in different ways.

If you wish to know more about the individual components, checkout my paper linked below which explains those components in detail.
It's relatively easy to understand, I promise :p

Research paper : [Piecing together a basic Operating System](https://www.researchgate.net/publication/341001566_Piecing_together_a_basic_Operating_System)

If you want to see how things are implemented in code look no further. It's also a tutorial :D

[github/os-tutorial](https://github.com/cfenollosa/os-tutorial)
