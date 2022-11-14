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
- To offer enough power and flexibility to satify professional audio tech industry users
- To speed-up commercial product cycles by enabling sound-designers to be more independent from the instrument platforms
- To attract students and beginners by being vastly easier to learn than C/C++

If you're keen to learn the nitty-gritty of the language itself, the [language guide](docs/LanguageReference) offers a deep dive. To see some examples of the code, try the [examples](https://github.com/SoundStacks/cmajor/tree/main/examples/patches) folder.

## How can Cmajor be used?

There are lots of different workflows in the world of audio development, and we want Cmajor to fit into as many of them as possible. Some of the ways you can use it are:

### Stand-alone development

It's trivially easy to get started writing and playing Cmajor patches on your local machine. (See the [quick-start guide](docs/GettingStarted)).

If you don't fancy using our command-line tools, we have a VScode extension which provides a 1-click install process, giving you everything you need to edit and run Cmajor patches inside VScode, without going near a terminal or knowing what a compiler is.

As well as being able to test patches using a MIDI keyboard and your computer's audio input/output, you can also use our Cmajor VST/AU plugin to load your patches inside any regular DAW. This loader plugin uses a JIT engine, so you can edit your patches while running, and they'll automatically rebuild and update themselves without needing to restart.

### Turning a Cmajor patch into a native VST/AU/AAX plugin

When you have a finished Cmajor patch, you can use our tools to convert it to a native C++ JUCE project, which you can compile into whatever audio plugin format you like, and distributed like any other audio plugin.

### Using Cmajor code in C++ projects

Our tools can also export a raw, dependency-free C++ version of any Cmajor code. This means that you could design and test a DSP algorithm using our JIT engine and hot-reloader, and then export the finished code as C++ for use in any kind of app or even a bare-metal project.

### Embedding the Cmajor JIT engine in your app

For developers who want to embed the Cmajor JIT engine into their own native apps, there's a C++ API to do that - see the documentation [here](docs/C++API).

As well as an API, we supply a whole range of utility C++ classes that make it easy to use Cmajor in various common audio software patterns.

### (Coming soon!) Develop and run Cmajor in your browser

Cmajor has been designed from the outset to fit into a WASM/WebAssembly stack, and we'll soon be offering a full online playground at [cmajor.dev](https://cmajor.dev). This will let people dabble with the language without needing to install anything on their local machine.

### (Coming soon!) Native support for Cmajor patches in DAWs

Tracktion Waveform will be the first DAW to support native loading of patches, but we hope others will follow soon!

A DAW with native support for Cmajor will offer a better experience of scanning for patches, and can do a better job of presenting and hot-reloading them. Our Cmajor JIT plugin can load patches into a DAW, but thanks to the VST/AU formats being designed for static plugins, there are some things it can't do, such as allowing dynamic changes to parameter lists or i/o buses.

---------------------------------------------------------------------------------

### Contacting us

To chat about Cmajor, you can join our [discord channel](https://discord.gg/Abtc5xabcT) at [theaudioprogrammer.com](https://www.theaudioprogrammer.com/)

For bugs and feature requests, you can use our [github issue tracker](https://github.com/SoundStacks/cmajor/issues).

To find out about any upcoming job openings, follow us on [LinkedIn](https://www.linkedin.com/company/sound-stacks-ltd/).

For business-related enquiries, email us at info@soundstacks.co.uk

---------------------------------------------------------------------------------

<img src="assets/images/SoundStacks-logo.png" width="190pt">

Cmajor is developed by [Sound Stacks Ltd.](https://soundstacks.co.uk)
