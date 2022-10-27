---
title: Emoji-Predictor 🐍
summary: School project using machine learning to guess the emoji used in a tweet based on its content..
tags:
  - ds
date: '2022-01-27'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: 
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: source
    url: https://github.com/SaadNeverSad/Emoji-Prediction
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.

---
# Emoji predictor
School project using machine learning to guess the emoji used in a tweet based on its content.

## Model

![Model](model.png)

### Word2Vec
The first layer of our model is an embedding layer. We used *word2vec* as it yields good results. We used the *cbow* version with a window of size 5 and an embedding size of 500.

### LSTM
For classification, we used an LSTM as it is the most suited for handling textual data. The last layer is a fully connected layer of size 20.

## Results

### Scores

![Scores](scores.png)

### Confusion matrix

![Confusion matrix](confusion_matrix.png)


{{< youtube taVOEMFuwUA >}}









