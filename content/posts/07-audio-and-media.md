---
title: "Text-to-Speech and Media Resources"
date: 2026-10-16T09:00:00+02:00
draft: false
weight: 7
---

This week I worked on the audio generation and media resource parts of MyOllama.

After Ollama generates a quiz question and its answers, the application needs spoken versions of the relevant text. I worked with the Kokoro text-to-speech service, which receives text through a JSON request and returns audio data in WAV format.

I also looked at how the application retrieves additional resources. These include the background image, countdown sound and background music.

The ResourceService is responsible for communicating with the resource server. This keeps the resource-related HTTP requests separate from the main controller logic.

At this stage, the workflow is becoming more complete. The application can generate quiz content, prepare speech and collect the media files that will eventually be combined into a video.

One challenge is making sure that the different types of data are handled consistently when they are passed between services.

Next week I will focus on combining the assets and sending the video instructions to the rendering service.
