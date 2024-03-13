---
layout: default
title: GuitarLSTM
parent: Examples
nav_order: 9
has_children: false
has_toc: false
---

## GuitarLSTM

This example demonstrates Cmajor being used for machine learning inference.

The code to generate this patch can be found in https://github.com/cmajor-lang/GuitarLSTM, which is a fork of the github project provided by https://guitarml.com


### Recreating the patch

To recreate this patch yourself, check out the above repo like this:

    git clone git@github.com:cmajor-lang/GuitarLSTM.git
    cd GuitarLSTM
    git submodule init
    git submodule update

The model can then be trained with:

    ./train.py data/ts9_test1_in_FP32.wav data/ts9_test1_out_FP32.wav test

This will generate the output in models/test, and the generated Cmajor will be in `models/test/patch`


### How this works

The model and inference is unchanged from the GuitarLSTM script, so this uses TensorFlow to build the model and run the training.

After training, we export the TF model to an RTNeural `.json` file, using the scripts included in the RTNeural package.

The script then executes the python script in `cmajor/tools/rtneural` to generate a Cmajor file based on the generated RTNeural json file.


<a href="https://github.com/cmajor-lang/cmajor/tree/main/examples/patches/GuitarLSTM" target="_blank">Click here to view the source code.</a>

<iframe style="display: inline-block; width: 100%; height: 32rem; border:none; padding-top: 1rem;"
        src="../../../assets/example_patches/GuitarLSTM/index.html">
</iframe>

