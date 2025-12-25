# Data Model: Physical AI & Humanoid Robotics Hackathon Phase-1 Frontend Content

**Feature**: Physical AI & Humanoid Robotics Hackathon Phase-1 Frontend Content
**Date**: 2025-12-25

## Overview

This document defines the conceptual data model for the Phase-1 frontend content of the Physical AI & Humanoid Robotics Hackathon textbook. Since this is frontend-only content with no backend implementation, the data model focuses on the content structure and organization rather than traditional data entities.

## Content Entities

### 1. Textbook Page
**Description**: A single page of the Physical AI textbook containing educational content

**Attributes**:
- `id`: Unique identifier for the page (string, required)
- `title`: Display title of the page (string, required)
- `description`: Brief description for SEO and navigation (string, optional)
- `content`: Main educational content in Markdown format (string, required)
- `keywords`: SEO keywords for the page (array of strings, optional)
- `navigationTitle`: Title used in navigation menus (string, optional)
- `sidebar`: Sidebar configuration for the page (object, optional)

**Validation Rules**:
- Title must be 5-100 characters
- Content must be in valid Markdown format
- ID must be unique across all pages

### 2. Physical AI Concept
**Description**: A core concept within Physical AI and embodied intelligence

**Attributes**:
- `name`: Name of the concept (string, required)
- `definition`: Clear definition of the concept (string, required)
- `examples`: Practical examples illustrating the concept (array of strings, optional)
- `relatedConcepts`: Other concepts that relate to this one (array of strings, optional)
- `difficultyLevel`: Beginner, Intermediate, or Advanced (enum, required)

**Validation Rules**:
- Name must be unique within the textbook
- Definition must be 20-200 characters
- Difficulty level must be one of the defined values

### 3. Course Structure Element
**Description**: An element of the course structure (learning outcome, weekly journey item, etc.)

**Attributes**:
- `type`: Type of structure element (string, required)
- `title`: Title of the element (string, required)
- `description`: Detailed description (string, required)
- `order`: Order in which this appears in the sequence (integer, required)
- `prerequisites`: Other elements that should be understood first (array of strings, optional)

**Validation Rules**:
- Order must be unique within the same type
- Type must be one of: learningOutcome, weeklyJourney, assessment, goal

## Content Relationships

### Textbook Page Relationships
- A Textbook Page MAY contain multiple Physical AI Concepts
- A Textbook Page MAY reference other Textbook Pages as related content
- A Textbook Page SHOULD align with one or more Course Structure Elements

### Physical AI Concept Relationships
- A Physical AI Concept MAY be related to other Physical AI Concepts
- A Physical AI Concept SHOULD be explained in at least one Textbook Page
- A Physical AI Concept MAY have prerequisite concepts

## Content State Transitions

### Page States
- **Draft**: Content is being created
- **Review**: Content is ready for review
- **Approved**: Content has been approved for publication
- **Published**: Content is live in the textbook

## Content Validation Rules

### General Content Rules
- All content must maintain academic textbook tone
- No implementation details or code examples
- All content must be appropriate for beginner-to-intermediate learners
- Content must align with Physical AI and embodied intelligence focus

### Phase-1 Specific Rules
- Content must be limited to Phase-1 scope
- No references to future phases or features
- No backend, API, or technical implementation details
- Content must synthesize material from Hackathon PDF pages 3-9
- All pages must be Docusaurus-compatible Markdown/MDX format

## Navigation Model

### Sidebar Structure
The sidebar will be organized in a hierarchical structure:
- Main category (Physical AI & Humanoid Robotics)
- Subcategories (Introduction, Concepts, Architecture, etc.)
- Individual pages within each category

### Breadcrumb Trail
Each page will include a breadcrumb trail showing the navigation path from the main textbook page to the current page.