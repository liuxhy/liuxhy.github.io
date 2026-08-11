---
title: "Real-Time Cat vs. Dog Classifier"
excerpt: "Webcam image classifier serving a TensorFlow Lite model behind a Flask API, with SQLite prediction logging."
collection: portfolio
---

A small web app that classifies webcam frames in real time. Frames are captured in the
browser, posted to a Flask backend, classified by a quantized TensorFlow Lite model, and
logged to SQLite so predictions can be reviewed later.

**Stack:** Python, Flask, TensorFlow Lite, SQLite, JavaScript

**Source:** [github.com/liuxhy/catdog_webcam](https://github.com/liuxhy/catdog_webcam)
