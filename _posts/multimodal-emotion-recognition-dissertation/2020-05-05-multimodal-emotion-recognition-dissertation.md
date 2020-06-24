---
title: 'OceanNet: Multimodal Emotion Analysis on Social Media with Deep Learning'
collaborators: 'Angelo Cangelosi'
icon: fas fa-file-download
paper: /assets/papers/dissertation.pdf
date: 2020-05-05 18:00:00 +00:00
tags: [ML, DL, sentiment analysis, emotion recognition, NLP, computer vision, multimodal]
description: Research dissertation for the completion of B.Sc. (Hons) Computer Science at The University of Manchester.
---

<h5 class="paragraph-title">Abstract</h5>

<p class="abstract">"Massive amounts of multimodal information are available on social media platforms as people generally post images accompanied by textual descriptions and hashtags. The automatic extraction and analysis of affective knowledge from so much data can provide businesses, governments and individuals with insights into the market perception and audience feeling of their actions, products and services. Hence, we propose a Deep Learning approach to processing the visual and textual components of posts extracted from Tumblr in order to predict the emotions attached as hashtags by users. We perform transfer learning on the state-of-the-art InceptionV3 CNN for image classification to capture the highly abstract representations of emotions from pictures, while an LSTM network grasps complex temporal patterns of affects from the text sequences of these posts. Accuracy scores of up to 62.03% and 79.22% have been achieved on the problems of visual and textual emotion recognition, respectively, over the basic model of six emotions. Furthermore, we explore the fusion of these modalities in a multi-input network that combines the single-modality architectures and achieves 75.13% accuracy using this method. An in-depth discussion of the per-class performance of these models is provided as part of the evaluation. Finally, the research on these AI tools is integrated into the OceanNet framework. This incorporates a visualisation tool for market analytics platforms that produces real-time visualisations of affective statistics from social media information."</p>

<h5 class="paragraph-title">Motivation</h5>

<ul class="motivation">
    <li>Although the state-of-the-art in sentiment analysis exceeds human-level performance standing at about 90% accuracy, its binary classification mechanism only captures <b>how</b> an entity perceived rather than <b>why</b> it is perceived in a certain manner.
    <br/>
    <center><i class="fas fa-arrow-down"></i></center>
     <center><b>This motivates the need to identify the nuances of feeling portrayed by human emotions, which would provide explicit, actionable.</b></center>
    </li>
    <li> In human interactions, only part of the message is transmitted verbally as the vocal and visual elements often hold more weight.
    <br/>
    <center><i class="fas fa-arrow-down"></i></center>
     <center><b>We account for the textual and visual modalities using a multi-input network.</b></center>
    </li>
    <li> The proliferation of social media has fueled recent progress in sentiment analysis as the massive
streams of subjective textual and visual information encouraged the automatic collection of affective corpora.
    <br/>
    <center><i class="fas fa-arrow-down"></i></center>
     <center><b>We compile a multimodal dataset of Tumblr posts comprising text and pictures and aim to predict emotion hashtags attached by users.</b></center>
    </li>
</ul>

<h5 class="paragraph-title">Summary</h5>

<ul>
    <li> <b>We collect a multimodal dataset using the Tumblr API,</b> fetching those text posts accompanied by images that contain an <b>emotion hashtag e.g. #amazed.</b> </li>
    <li>We explore the relevance of the textual and visual modalities in expressing emotions by training a set of DL models to perform single- and multi-modal emotion classification:
        <ul>
            <li> For <b>textual emotion analysis</b>, we compose a module comprising single LSTM layer of 1024 units, followed by a softmax layer producing a probability distribution over the set of emotions. This topology is the result of a hyperparameter grid search over the number of layers and neurons per layer.
            </li>
            <li>For <b>visual emotion analysis</b>, we perform transfer learning on InceptionV3, motivated by its ability to discover intricate structures in training data as our problem requires learning representations at a high level of abstraction.
            </li>
            <li>For <b>multimodal emotion analysis</b>, we concatenate the outputs of the single-modality networks, on top of which a Softmax function produces a probability distribution over the emotion spectrum.
            </li>
        </ul>
    </li>
    <li>The accuracy scores achieved by these networks are <b>68%</b>, <b>41%</b>, and <b>62%</b> for <b>textual</b>, <b>visual</b> and <b>multimodal emotion recognition</b>, respectively. The multimodal accuracy comes in contradiction with the findings of DeepSentiment, the state-of-the-art in Tumblr emotion recognition, which noted an improvement when using images alongside text.</li>
</ul>