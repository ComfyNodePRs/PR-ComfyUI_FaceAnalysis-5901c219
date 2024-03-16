# Face Analysis for ComfyUI

This extension uses [DLib](http://dlib.net/) to calculate the Euclidean and Cosine *distance* between two faces.

The best way to evaluate generated faces is to first send a batch of 3 reference images to the node and compare them to a forth reference (all actual pictures of the person). That will give you a baseline number that you can use to compare to generated images.

## Installation

Please download the DLIB [Shape Predictor](https://huggingface.co/matt3ounstable/dlib_predictor_recognition/resolve/main/shape_predictor_68_face_landmarks.dat?download=true) and the [Face Recognition](https://huggingface.co/matt3ounstable/dlib_predictor_recognition/resolve/main/dlib_face_recognition_resnet_model_v1.dat?download=true) models and place them into the `dlib` directory.

Precompiled Dlib for windows can be found [here](https://github.com/z-mahmud22/Dlib_Windows_Python3.x).

In this repository you also find a workflow that uses IPAdapter to generate a few images and return the distance to the reference face.

![face analysis](./face_analysis.jpg)

The extension of course requires `dlib` that has to be installed into the ComfyUI environment.

## Important notes

There are many ways to do this. At the moment I'm using DLib as it's fast and easy to use, if there's an actual interest I will release more options (insightface?).

Also, I'm not an engineer and I don't know what I'm doing, hopefully someone more experienced can chime in.