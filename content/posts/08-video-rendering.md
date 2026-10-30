---
title: "Combining the Assets and Rendering the Video"
date: 2026-10-23T09:00:00+02:00
draft: false
weight: 8
---

This week I focused on bringing the different parts of the video-generation workflow together.

The QuizVideoRenderer coordinates the media required for the finished quiz video. This includes the background image, question audio, countdown audio, answer audio and background music.

The VideoInstruction object is used to prepare the instructions and visual overlays. The different resources are represented through VideoFile objects and grouped together in a VideoRequest.

The application then sends this request to the FFmpeg service, which is responsible for rendering the final video.

I also reviewed the VideoController and its POST /video/generate-video endpoint. The endpoint exposes the video-generation process and returns the resulting video with the video/mp4 content type.

This was an important stage because the individual services need to work together in the correct order. A problem with one resource or an incorrectly structured request could affect the complete workflow.

Next week I will focus on testing, documentation and evaluating what is finished and what still needs improvement.
