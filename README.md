---
title: "tongueDetection"
authors: "Javad Rahimipour Anaraki, Silvia Orlandi and Tom Chau"
date: '22/09/20'
---

## Notice
The code `mainCNN.m` is available now, and a link to the paper on arXiv is provided down below. If you need more details and explanation about the algorithm, please contact [Javad Rahimipour Anaraki](http://individual.utoronto.ca/jrahimipour/).

## Use case
To decide if tongue is out based on a CNN trained against pediatric population data as described in "A Deep Learning Approach to Tongue Detection for Pediatric Population" by Javad Rahimipour Anaraki, Silvia Orlandi and Tom Chau. Here is the arXiv link to the paper: [arXiv](https://arxiv.org/abs/2009.02397)

## Requirements
This code is implemented in MATLAB® 9.8.0.1323502 (R2020a), and the recommended spec for running the code is Intel®Core™i7, 16 GB of RAM, and NVIDIA®Quadro® Graphic card

## Run
In the data folder, store neutral face images in *neutral* folder, and tongue-out images in *tongue* folder for each participant. The structure of *data* folder is as follows:

- data
  - P1
    - tongue
      - neutral
      - tongue
  - P2
    - tongue
      - neutral
      - tongue
  - ...

To run the code, open `mainCNN.m` and run the code as-is. The current setting uses MATLAB® implemented augmentation to resize all the input images to 32 x 32. If otherwise, modify the `imageSize` variable. The current network setting is as follows:

- `MiniBatchSize` is 128
- `MaxEpochs` is 50

And to change the running environment from GPU to CPU, change the value of variable `ExecutionEnvironment` from 'gpu' to 'cpu'.


## Note
 - The training process might take longer if `ExecutionEnvironment` is set to 'cpu'
 - Failure in organizing the *data* folder would prevent the code from running
