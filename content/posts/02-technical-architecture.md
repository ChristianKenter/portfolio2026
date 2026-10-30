---
title: "Choosing the Architecture and Technologies"
date: 2026-09-11T09:00:00+02:00
draft: false
weight: 2
---

This week I focused on the technical architecture of MyOllama. I worked on deciding how the backend should be structured and which technologies would be suitable for the project.

I chose Java with Javalin for the backend because it provides a lightweight way to create HTTP endpoints without introducing an unnecessarily large framework.

I also planned a layered architecture. Routes define the available endpoints, controllers handle incoming requests, services communicate with external systems and DAO classes are responsible for database operations.

The project uses Maven for dependency management, PostgreSQL and Hibernate for persistence, and Java's HttpClient for communication with external APIs.

I also identified the main external services: Ollama for generating quiz content, Kokoro for text-to-speech and FFmpeg for video rendering.

This gave me a much clearer overview of how the application should work. Next week I will focus on the project structure and data models.
