---
id: 001
title: Establish Project Constitution for AI Textbook
stage: constitution
date: 2025-12-07
surface: agent
model: google/gemini-pro
feature: none
branch: main
user: user
command: /sp.constitution /sp.constitution

Project: AI-Native Textbook + RAG Chatbot for “Physical AI & Humanoid Robotics”

Core principles:
- Specification-driven development (Spec-Kit Plus as source of truth)
- Modular, reproducible workflows across book, code, and chatbot
- Technical accuracy validated against robotics standards (ROS 2, Gazebo, Isaac Sim)
- Clarity for students (CS/AI engineering background, undergraduate-to-advanced)
- Multi-agent consistency: book content, RAG corpus, and chatbot behavior must align
- Verification through runnable prototypes (book build, API tests, chatbot inference)

Key standards:
- Book format: Docusaurus v3, deployed to GitHub Pages
- Code quality: Claude Code-compatible, type-safe, documented
- RAG architecture: FastAPI backend, OpenAI Agents/ChatKit, Qdrant Cloud, Neon Serverless Postgres
- Knowledge ingestion: Book chapters + user-selected text chunks
- Citation standard (for factual robotics/AI claims): IEEE style
- Physical AI concepts must follow ROS 2, Gazebo, URDF, Isaac documentation
- No hallucination: All robotics procedures must be verifiable via docs or simulation

Constraints:
- Book length: 120–200 pages across modules
- Minimum 4 modules aligned to the quarter curriculum
- Each module must include: theory → simulation → code → exercises → assessment
- RAG chatbot must:
  - Answer questions *only* from indexed book content
  - Support "answer from selected text only" mode
  - Log interactions in NeonDB
  - Serve via FastAPI on local or cloud environment
- Deployment: Must build and deploy automatically via GitHub Actions

Success criteria:
- Docusaurus site builds cleanly with no broken links or MDX errors
- GitHub Pages deployment successful on main branch
- RAG pipeline returns accurate answers from book text
- Qdrant vectors match all chapters without empty embeddings
- FastAPI passes end-to-end API testing (health, search, answer)
- Book content covers:
  - ROS 2 core concepts (Nodes, Topics, Services, URDF)
  - Gazebo & Unity digital twins
  - NVIDIA Isaac Sim, Isaac ROS, navigation, VSLAM
  - Vision-Language-Action robotics workflows
- Capstone defined: “Autonomous Humanoid Robot with Voice-to-Action Pipeline”
- No hallucination or unverifiable robotics claims
- Hackathon-ready: All deliverables demonstrable in a final presentation
labels: ["constitution", "setup"]
links:
  spec: null
  ticket: null
  adr: null
  pr: null
files:
 - .specify/memory/constitution.md
 - .specify/templates/plan-template.md
tests:
[]
---

## Prompt

/sp.constitution /sp.constitution

Project: AI-Native Textbook + RAG Chatbot for “Physical AI & Humanoid Robotics”

Core principles:
- Specification-driven development (Spec-Kit Plus as source of truth)
- Modular, reproducible workflows across book, code, and chatbot
- Technical accuracy validated against robotics standards (ROS 2, Gazebo, Isaac Sim)
- Clarity for students (CS/AI engineering background, undergraduate-to-advanced)
- Multi-agent consistency: book content, RAG corpus, and chatbot behavior must align
- Verification through runnable prototypes (book build, API tests, chatbot inference)

Key standards:
- Book format: Docusaurus v3, deployed to GitHub Pages
- Code quality: Claude Code-compatible, type-safe, documented
- RAG architecture: FastAPI backend, OpenAI Agents/ChatKit, Qdrant Cloud, Neon Serverless Postgres
- Knowledge ingestion: Book chapters + user-selected text chunks
- Citation standard (for factual robotics/AI claims): IEEE style
- Physical AI concepts must follow ROS 2, Gazebo, URDF, Isaac documentation
- No hallucination: All robotics procedures must be verifiable via docs or simulation

Constraints:
- Book length: 120–200 pages across modules
- Minimum 4 modules aligned to the quarter curriculum
- Each module must include: theory → simulation → code → exercises → assessment
- RAG chatbot must:
  - Answer questions *only* from indexed book content
  - Support "answer from selected text only" mode
  - Log interactions in NeonDB
  - Serve via FastAPI on local or cloud environment
- Deployment: Must build and deploy automatically via GitHub Actions

Success criteria:
- Docusaurus site builds cleanly with no broken links or MDX errors
- GitHub Pages deployment successful on main branch
- RAG pipeline returns accurate answers from book text
- Qdrant vectors match all chapters without empty embeddings
- FastAPI passes end-to-end API testing (health, search, answer)
- Book content covers:
  - ROS 2 core concepts (Nodes, Topics, Services, URDF)
  - Gazebo & Unity digital twins
  - NVIDIA Isaac Sim, Isaac ROS, navigation, VSLAM
  - Vision-Language-Action robotics workflows
- Capstone defined: “Autonomous Humanoid Robot with Voice-to-Action Pipeline”
- No hallucination or unverifiable robotics claims
- Hackathon-ready: All deliverables demonstrable in a final presentation

## Response snapshot

Established the project constitution and updated related templates.

- Created `.specify/memory/constitution.md` with version 1.0.0 based on user-provided principles, standards, and constraints.
- Updated `.specify/templates/plan-template.md` to include a "Constitution Check" section aligned with the new principles.
- Created this Prompt History Record.

## Outcome

- ✅ Impact: High. Established foundational governance for the project.
- 🧪 Tests: None. This was a documentation and configuration change.
- 📁 Files: 2 files modified/created: `.specify/memory/constitution.md`, `.specify/templates/plan-template.md`. 1 PHR file created.
- 🔁 Next prompts: User can now proceed with feature specification and planning using `/sp.specify` and `/sp.plan`.
- 🧠 Reflection: The process of creating a constitution from user input and propagating it to templates works well. The agent-native PHR creation fallback was necessary and successful.

## Evaluation notes (flywheel)

- Failure modes observed: The `create-phr.sh` script assumed in the instructions was not found.
- Graders run and results (PASS/FAIL): PASS
- Prompt variant (if applicable): null
- Next experiment (smallest change to try): Ensure PHR creation logic is robust to missing scripts and has a reliable fallback.
