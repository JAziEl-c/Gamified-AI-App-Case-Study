# Gamification AI Voice Training Web Application Simulation
**Confidentiality Notice:** This repository serves purely as an architectural case study and technical design overview. Government data schemas and proprietary source code will **not** be provided adhering to non-disclosure and project confidentiality guidelines

## 1. Overview
The prototype is a web application for realistic mock simulation practice through social service conversations in a Singapore context. Trainees work through various scenarios in response to a simulated client and receive feedback against a structured behavioural rubric. The app also includes progress tracking and supporting features for managing scenarios and reviewing practice history.

## 2. Problem Statement
Social service officers often go through difficult scenarios where there is a need in handling sensitive and emotionally intense conversations through clients while simultaneously treating them with care and following through strict service policies. Often at times, opportunities to practice these skills in realistic situations can be limiting, and requires scheduling between colleagues on top of handling clients.

The prototype aims to explore in this sector on whether an online guided simulation can give officers a way to practice conversations and receive structured feedback in a lower-risk environment.

## 3. System Architecture
At a high level, the application is organized in 3 different layers:
1. **Presentation Layer** - Web application
2. **Business Layer** - RESTful API, Conversational AI Service, Scenario Dialogue Service, Gamification Service, Assessment Engine
3. **Persistence Layer** - Cloud Data Storage, Physical Data Storage, Temporary Data Storage <br>
<img width="588" height="677" alt="image" src="https://github.com/user-attachments/assets/97e0c7ea-9e17-4f13-ba53-a1be5ae64be3" />

The browser interface uses HTML, CSS and JavaScript. A Flask application handles the web pages and main application workflow which connects to AI speech services and stores scenarios/sessions/user information. Redis is used as temporarily cache management.

## 4. Key Features
- Simulated conversations based on social service scenarios
- AI-supported assessment against a behavioural rubric
- Speech-To-Text (STT) and Text-To-Speech (TTS) support
- Scenario history, reflections, scores and analytics
- User profiles, badges, leaderboards, and peer features
- Admin tools and dashboard for managing scenarios, users and settings
- Local JSON storage for demos, with PostgreSQL support in configured deployments

## 5. Outcome
A working prototype that brings scenario practice alive, fully captured conversations through STT/TTS, structured feedback and progress tracking in one web application. It provides a foundation in exploring how AI-supported simulations are able to fit into officer training. 

## 6. Challenges
- **Making conversations feel realistic:** Emotions in speech from the AI simulated client had to be conveyed strongly
- **Confidential data:** User authentication data has to be carefully handled before overwriting any source code
- **Fair feedback:** Feedback had to comply strictly with the rubrics and ensuring every officer has a similar scoring assessment if similarities in conversations are shared.
- **Cross-device support:** Certain web browsers blocked microphone access depending on hardware device
- **Session data:** Ensuring state synchronization occurs across multiple data sources

