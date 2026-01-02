---
layout: project
title: "Sentiment Detector"
icon: sentiment.png
github: "https://github.com/mylogon341/SentimentDetector"
tag: "A Swift library for providing basic text sentiment."
stack:
  - Swift
  - CoreML
  - NaturalLanguage
  - SwiftTesting
  - SPM
---

I created this as a learning experience. I trained a CoreML model under a Text Classification project via the Apple 'Create ML' software. To train the model, I produced a training data set of around 800 labeled phrases in a CSV file. The classifications that I have started with are:
- Threat
- Insult
- Sexual
- Positive
- Neutral
- Negative
- Profanity

This is a very lightweight library that runs on-device. 