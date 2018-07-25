---
layout:     post
title:      Pose Estimation
date:       2018-07-07 13:45:13
summary:    second intern project
categories: intern
---

Just because the computer started understanding the text data present all over the internet, it gave rise to one of the biggest tech giants, Google. Imagine how cool would it be if computer started understanding human actions! It would make computers so easy to interface with, and also to open another dimension of human-computer coordination.
With an aim to make computer understand human actions, we were asked to determine poses by extracting joints of human body, in any image provided. Luckily, this is already being done by various research groups all over the globe. One such very popular group is [Openpose](https://github.com/CMU-Perceptual-Computing-Lab/openpose), of Carnegie Mellon University.

The project was specifically aimed at detection of poses in sports. This will give us an extra edge to analyse performance and micro-recommendation which is priceless. We set off to do something like this - 

![Image](https://mohitsinha.in/img/img4)


### Concept:

The behind-the-curtain hero of this project is Convolutional Neural Network which does the most difficult part for us. I will assume you know basics of Machine Learning if you have made it so far reading this blog. Openpose uses a CNN with 17 layer architecture on well-annotated COCO dataset images. The accuracy of the final model depeds hugely on the kind of annotation that has been done. This is how we can represent the CNN architecture - 

![Image](https://mohitsinha.in/img/img5)

The CNN model, which is trained on these millions of images, gives us two things on forward propagation on new images -
1. Heatmaps
2. PAFs (Part Affinity fields) associated to heatmaps.

Take a look at how they look like when you plot them - 

![Image](https://mohitsinha.in/img/img6)

The pipeline of pose detection can be explained by the following diagram - 

![Image](https://mohitsinha.in/img/img3)

The two important parts of this project are - generating heatmaps and connecting them appropriately. The first part is done by CNN, which returns an array of 19 joints and 57 PAFs. While the heatmaps denote the joints in the image, PAFs are nothing but a quantity representing degree of association to another joint. So, obviously, PAFs will be less for forearm to knee, and more for forearm to elbow. By solving Bipartite graphs of PAFs, we can establish which two heatmaps will actually be connected in the final output. One more salient feature of this method is its ability to detect multi-person poses. Earlier model used a top-down approach, in which they detected a person first, and then determined its joint. Here, it doesn't matter if the person is present wholly. If only a fairly visible body part is in the frame, it will be detected.


### What we did:
My job was to build an algorithm which can compare poses between two humans posing. One will be a model, another will be player. I read about an awesome geometric algorithm named Procrustes. What is does is, translate whole of the datapoints of the player to model datapoints, perform affine transformation and scaling, and give you a measure of disparity by root mean squared error. I wrote this using Openpose C++ API. It was working fine as you can see - 

![Image](https://mohitsinha.in/img/img7-1) ![Image](https://mohitsinha.in/img/img7-2)

Apart from that, we also worked on posed detection on thermal images. The aim was to obtain joint fatigue of sportsman. It looked something like this - 

![Image](https://mohitsinha.in/img/img8)

Finally, the whole work was done and we presented our work in front of the Co-founders and they seem to be impressed. It was a wonderful experience to work at such a startup. I will miss Bangalore a lot. This is a picture from the last day of intern.

![Image](https://mohitsinha.in/img/img2)


Signing off.
