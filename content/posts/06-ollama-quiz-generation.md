---
title: "Connecting Ollama and Generating Quiz Questions"
date: 2026-10-09T09:00:00+02:00
draft: false
weight: 6
---

This week I focused on the quiz-generation functionality.

MyOllama uses the Ollama API together with the Qwen 2.5 3B model to generate multiple-choice questions based on a category provided by the user.

I worked on the prompt structure to make the generated responses more predictable. The model needs to return one question, four possible answers labelled A to D and one correct answer.

The OllamaService handles communication with the external API. It uses Java's HttpClient to send the request and Jackson to process the JSON response into a structured DTO.

This is important because the rest of the application needs to work with the generated question and answers in a consistent format.

I also realised that prompt design has a direct effect on the reliability of the application. If the response format changes unexpectedly, the later stages of the video workflow can become more difficult.

Next week I will focus on converting the generated text into audio and collecting the media resources needed for the video.
