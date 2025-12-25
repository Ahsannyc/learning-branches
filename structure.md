# Physical AI & Humanoid Robotics Textbook Project

## Vision & Scope

The Project Overview of this project involves creating a comprehensive textbook for teaching Physical AI & Humanoid Robotics, focusing on the intersection of AI systems and the physical world. The course aims to bridge the gap between digital AI and physical robotics, enabling students to apply their AI knowledge to control Humanoid Robots in simulated and real-world environments.

The project follows a structured approach with 8 distinct phases, divided into mandatory functionality (Phases 1-5) and extra features for bonus points (Phases 6-8). The textbook will be built using Docusaurus and deployed to GitHub Pages, with an integrated RAG chatbot and various advanced features.


## Core Requirements in Phases (Foundational Development)

## Phase 0: Setting Up Environment Foundation (main)
- Git Branch: main
- Installed speckitplus and initialized its project using `specifyplus init .`
- Create the frontend directory using `npx create-docusaurus@latest frontend classic` command which has the default setup of docusarus project 
- Create the backend directory using `uv init backend --package` command which has the default setup of uv
- Create the contitution.md file of the entire project using `/sp.constitution <prompt>` in claude code

### Phase 1: Book Curriculum (001-book-curriculum)
- Git Branch: `001-book-curriculum`
- Create comprehensive textbook content using Docusaurus
- Structure content around the four core modules:
  - Module 1: The Robotic Nervous System (ROS 2)
  - Module 2: The Digital Twin (Gazebo & Unity)
  - Module 3: The AI-Robot Brain (NVIDIA Isaac™)
  - Module 4: Vision-Language-Action (VLA)

### Phase 2: Minimal FastAPI Backend (002-minimal-fastapi-chat)
- Git Branch: `002-minimal-fastapi-chat`
- Develop a FastAPI backend with OpenAI Agents SDK
- Create a single endpoint `/chat` for chat functionality
- Configured with Gemini LLM (gemini-2.0-flash) by using OpenAI Agent SDK's OpenAIChatCompletionsModel.

### Phase 3: Chatbot Integration (003-chatbot-integration)
- Git Branch: `003-chatbot-integration`
- Integrate OpenAI ChatKit UI into the Docusaurus frontend
- Connect the frontend chatbot with the FastAPI backend
- Ensure seamless communication between UI and backend services

### Phase 4: UI Design (004-ui-design)
- Git Branch: `004-ui-design`
- Apply a professional robotics theme to the UI
- Ensure consistency and visual appeal throughout the application
- Implement design elements that reflect the robotics/physical AI theme

### Phase 5: RAG Implementation (005-rag-qdrant-integration)
- Git Branch: `005-rag-qdrant-integration``
- Integrate Qdrant Cloud for vector storage
- Use Gemini embedding model instead of OpenAI
- Sync book content into the vector database for intelligent question answering using fastapi endpoint /ingest
- Create a tool that OpenAI Agent uses for RAG (Retrieval-Augmented Generation) purposes

## Bonus Phases

### Phase 6:Identity Authentication & Database (006-identity-authentication-neondb)
- Git Branch: `006-identity-authentication-neondb`
- Implement Better Auth backend for user authentication
- Use NeonDB for storing user credentials and data
- Likely implemented in Node.js or Express
- Handle secure user registration and login flows

### Phase 7: Multiple Language Support (007-multiple-language-support)
- Git Branch: `007-multiple-language-support`
- Add multilingual options to the UI
- Implement translation capabilities for textbook content
- Enable content translation features for international accessibility

### Phase 8: Content Customization (008-content-Customization)
- Git Branch: `008-content-customization`
- Add a personalization button on every page of content
- Allow users to customize content based on their preferences
- Implement dynamic content adaptation based on user settings