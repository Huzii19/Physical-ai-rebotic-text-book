<!--
Sync Impact Report:
- Version change: 1.0.0 -> 1.1.0
- List of modified principles: None
- Added sections:
  - Added "Quality Validation" to Key Standards
- Removed sections: None
- Templates requiring updates: None
- Follow-up TODOs: None
-->
# AI-Native Textbook + RAG Chatbot for “Physical AI & Humanoid Robotics” Constitution

## Core Principles

### I. Specification-Driven Development
Specification-driven development is the source of truth. All work must be grounded in a specification, and Spec-Kit Plus is the tool to enforce this.

### II. Modular, Reproducible Workflows
Workflows across the book, code, and chatbot must be modular and reproducible. This ensures consistency and allows for independent development and testing of components.

### III. Technical Accuracy
Technical accuracy must be validated against robotics standards. All claims and procedures related to robotics must be verifiable against ROS 2, Gazebo, and Isaac Sim documentation.

### IV. Clarity for Students
The primary audience is students from CS/AI engineering backgrounds. All content must be clear, concise, and aimed at an undergraduate-to-advanced level.

### V. Multi-Agent Consistency
The book content, RAG corpus, and chatbot behavior must align. This ensures a consistent experience for the user and prevents conflicting information.

### VI. Verification Through Prototypes
All features must be verified through runnable prototypes. This includes the book build, API tests, and chatbot inference.

## Key Standards

- **Book Format**: Docusaurus v3, deployed to GitHub Pages.
- **Code Quality**: Code must be Claude Code-compatible, type-safe, and well-documented.
- **RAG Architecture**: The RAG system will use a FastAPI backend, OpenAI Agents/ChatKit, Qdrant Cloud for vector storage, and Neon Serverless Postgres for metadata.
- **Knowledge Ingestion**: The RAG system will ingest book chapters and user-selected text chunks.
- **Citation Standard**: Factual robotics and AI claims must follow the IEEE citation style.
- **Physical AI Concepts**: Concepts must adhere to ROS 2, Gazebo, URDF, and NVIDIA Isaac documentation.
- **Quality Validation**: All content and code must pass explicit validation steps for:
    - **Accuracy**: Claims and procedures are checked against source documentation (e.g., ROS 2, Gazebo docs).
    - **Clarity**: Content is reviewed for understandability by the target student audience.
    - **Reproducibility**: All code examples, simulations, and exercises are tested to ensure they run as described.
- **No Hallucination**: All robotics procedures must be verifiable via documentation or simulation. The RAG chatbot must not invent information.

## Constraints

- **Book Length**: The book will be between 120 and 200 pages, structured into modules.
- **Curriculum Structure**: There will be a minimum of 4 modules, each including theory, simulation, code, exercises, and an assessment.
- **RAG Chatbot Functionality**:
    - Must answer questions *only* from indexed book content.
    - Must support an "answer from selected text only" mode.
    - Must log interactions in the NeonDB database.
    - Must be served via a FastAPI backend in a local or cloud environment.
- **Deployment**: The book and any associated applications must build and deploy automatically via GitHub Actions.

## Success Criteria

- Docusaurus site builds cleanly with no broken links or MDX errors.
- GitHub Pages deployment is successful on the main branch.
- RAG pipeline returns accurate answers from the book text.
- Qdrant vectors match all chapters without empty embeddings.
- FastAPI backend passes all end-to-end API tests (health, search, answer).
- Book content covers:
    - ROS 2 core concepts (Nodes, Topics, Services, URDF)
    - Gazebo & Unity digital twins
    - NVIDIA Isaac Sim, Isaac ROS, navigation, VSLAM
    - Vision-Language-Action robotics workflows
- A capstone project is defined: “Autonomous Humanoid Robot with Voice-to-Action Pipeline”.
- No hallucinated or unverifiable robotics claims are present in any output.
- All deliverables are hackathon-ready and can be demonstrated in a final presentation.

## Governance

This constitution is the supreme governing document for this project. All development, documentation, and operational practices must comply with its principles and standards. Amendments to this constitution require a documented proposal, review, and approval from the project lead.

**Version**: 1.1.0 | **Ratified**: 2025-12-07 | **Last Amended**: 2025-12-09