---
layout: default
title: Home
nav_order: 1
description: "C major documentation."
permalink: /
---

# Welcome to Cmajor!

The programming language for writing fast, portable audio software.

You've heard of C, C++, C#, objective-C... well, C*major* is a C-family language designed specifically for writing DSP signal processing code.

## About

Our goal is to improve on the current status-quo for audio development in quite a few ways:

- To match (and often beat) the performance of traditional C/C++
- To make the same code portable across diverse processor architectures (CPU, DSP, GPU, TPU etc)
- To offer enough power and flexibility to satisfy professional audio tech industry users
- To speed-up commercial product cycles by enabling sound-designers to be more independent from the instrument platforms
- To attract students and beginners by being vastly easier to learn than C/C++

If you're keen to learn the nitty-gritty of the language itself, the [language guide](docs/LanguageReference) offers a deep dive. To see some examples of the code, try the [examples](https://github.com/cmajor-lang/cmajor/tree/main/examples/patches) folder.

## How can Cmajor be used?

There are lots of different workflows in the world of audio development, and we want Cmajor to fit into as many of them as possible. Some of the ways you can use it are:

### Stand-alone development

It's trivially easy to get started writing and playing Cmajor patches on your local machine. (See the [quick-start guide](docs/GettingStarted)).

If you don't fancy using our command-line tools, we have a VScode extension which provides a 1-click install process, giving you everything you need to edit and run Cmajor patches inside VScode, without going near a terminal or knowing what a compiler is.

As well as being able to test patches using a MIDI keyboard and your computer's audio input/output, you can also use our Cmajor VST/AU plugin to load your patches inside any regular DAW. This loader plugin uses a JIT engine, so you can edit your patches while running, and they'll automatically rebuild and update themselves without needing to restart.

### Exporting a Cmajor patch as a native VST/AU/AAX plugin

When you have a finished Cmajor patch, you can use our tools to convert it to a native C++ JUCE project, which you can compile into whatever audio plugin format you like, and distributed like any other audio plugin.

### Exporting a Cmajor patch as Javascript/WebAssembly/HTML

The Cmajor command-line tools and VScode extension can instantly export a folder of dependency-free HTML/Javascript which you can view with a webserver to play your patch using WebAudio/WebMIDI.

Internally, we use the latest LLVM backend to convert the DSP to optimised WebAssembly, so it'll run about as fast as you can get inside a browser. The export process also bundles any custom GUI code.

Our tools can either emit an `index.html` that gets you up-and-running, or you can just export the javascript classes and write your own glue code to plumb them into your website.

### Exporting a Cmajor patch for use in legacy C++ projects

Our tools can also export a raw, dependency-free C++ version of any Cmajor code. This means that you could design and test a DSP algorithm using our JIT engine and hot-reloader, and then export the finished code as C++ for integration into any kind of app or even a bare-metal project.

### Embedding the Cmajor JIT engine in your app

For developers who want to embed the Cmajor JIT engine into their own native apps, there's a C++ API to do that - see the documentation [here](docs/Tools/C++API).

As well as an API, we supply a whole range of utility C++ classes that make it easy to use Cmajor in various common audio software patterns.

### (Coming soon!) Native support for Cmajor patches in DAWs

Tracktion Waveform will be the first DAW to support native loading of patches, but we hope others will follow soon!

A DAW with native support for Cmajor will offer a better experience of scanning for patches, and can do a better job of presenting and hot-reloading them. Our Cmajor JIT plugin can load patches into a DAW, but thanks to the VST/AU formats being designed for static plugins, there are some things it can't do, such as allowing dynamic changes to parameter lists or i/o buses.

---------------------------------------------------------------------------------

### Contacting us

To chat about Cmajor, you can join our [discord channel](https://discord.gg/Abtc5xabcT) at [theaudioprogrammer.com](https://www.theaudioprogrammer.com/)

For bugs and feature requests, you can use our [github issue tracker](https://github.com/cmajor-lang/cmajor/issues).

To find out about any upcoming job openings, follow us on [LinkedIn](https://www.linkedin.com/company/cmajor-software-ltd/).

For business-related enquiries, email us at info@cmajor.dev

---------------------------------------------------------------------------------

<img src="assets/images/Cmajor-Logo.png" width="190pt">

Cmajor is developed by [Cmajor Software Ltd.](https://cmajor.dev)
