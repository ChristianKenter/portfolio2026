---
title: "Project Structure and Data Modelling"
date: 2026-09-18T09:00:00+02:00
draft: false
weight: 3
---

This week I worked on organising the codebase and planning the data models used throughout MyOllama.

I focused on separating the different responsibilities into packages for routes, controllers, services, data access, entities and DTOs. This makes the code easier to maintain and helps prevent individual classes from becoming responsible for too many things.

I also worked through the main entities. The Client represents a registered user, while the video workflow uses objects such as Video, VideoFile, VideoInstruction and VideoRequest.

These objects are important because generating a video requires several different resources. The application needs to handle images, audio files, text overlays and instructions before sending everything to the rendering service.

I also considered how information should move between the different layers of the application.

Next week I will focus on connecting the database and implementing the first parts of the user registration system.
