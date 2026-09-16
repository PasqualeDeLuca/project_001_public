# Greed World

A data-driven naval sandbox RPG developed in Unity.

## Overview

**Greed World** is a 2D sandbox video game that combines exploration, trading, diplomacy, crew management, and tactical naval combat.

The player navigates a dynamic world influenced by economic systems, diplomatic relationships, weather conditions, reputation, character behavior, and world events.

Player decisions affect how the world reacts, creating emergent gameplay experiences driven by interconnected simulation systems rather than exclusively scripted events.

The project has been developed entirely by me over **three years**, and represents both a video game and a large-scale software engineering project, with a strong focus on **software architecture, system design, UI engineering, data-driven development, and code maintainability**.

> Developed independently for over 3 years, with a strong focus on UI Engineering, Data-Driven Architecture, System Design, and scalable software patterns.

---

## Features

- Open-ended 2D naval sandbox gameplay
- Exploration and dynamic world simulation
- Dynamic economy and trading
- Tactical turn-based naval combat
- Crew management and morale
- Character personalities and behavioral traits
- Diplomatic relationships between characters and kingdoms
- Reputation-driven interactions
- Data-driven quest and dialogue systems
- Dynamic weather simulation
- Global crisis events
- Autonomous AI activities
- Runtime entity database
- JSON-based content database
- Custom save/load and persistence system
- Custom UI framework and reusable UI components
- Custom development and debugging tools

---

## Technology Stack

### Core Technologies

- **Unity**
- **C#**
- **JSON**
- **Newtonsoft.Json**
- **Odin Serializer**

### Architecture & Design

- Data-Driven Architecture
- Repository Pattern
- Dependency Injection
- Event-Driven Architecture
- Runtime Entity Database
- Serializable Domain Models
- MVC
- MVVM
- ECS
- State Machines
- Separation of Concerns

---

## Software Architecture

The project follows a layered architecture designed to separate responsibilities, business logic, data access, and persistence.

```text
UI
↓
Managers
↓
Systems
↓
Repositories
↓
Data
```

The codebase consists of **hundreds of C# scripts, tens of thousands of lines of code, and dozens of interconnected systems**.

### Architectural Principles

- Data-Driven Architecture
- Repository-Based Architecture
- Runtime Entity Database
- JSON-Based Content Database
- Serializable Domain Models
- Event-Driven Communication
- Dependency Injection
- Separation of Concerns

The architecture is designed to minimize coupling between systems and make individual components easier to maintain, test, and extend.

---

## Core Systems

### Data Management System

A custom persistence system based on serializable domain models.

Key features:

- Save and load system
- Save versioning
- JSON serialization
- Optional data encryption
- Modular file management
- Runtime state persistence

---

### Entity Repository

A centralized runtime entity database used to index and retrieve game entities through unique identifiers.

Key features:

- Generic entity lookup
- Strongly typed data retrieval
- Runtime caching
- Decoupled communication between systems
- Repository Pattern implementation

Systems communicate through entity identifiers rather than direct object references, significantly reducing coupling between modules.

---

### Economy & Trading System

A dynamic economic system that determines the value of goods based on the current state of the game world.

Features include:

- Dynamic pricing
- Trading routes
- Cargo management
- Trading interactions
- Market fluctuations

---

### Diplomatic System

Manages relationships between different entities:

- Character → Character
- Character → Kingdom
- Kingdom → Kingdom

Diplomatic relationships can influence quests, trading opportunities, conflicts, and world events.

---

### Personality System

Characters develop behavioral traits based on actions and events occurring throughout the game.

Examples include:

- Greed
- Honor
- Cruelty
- Courage
- Ambition

These traits influence AI decisions, diplomacy, and character reactions to the world.

---

### Knowledge System

A knowledge-management system that distinguishes between different types of information:

- Direct experience
- Rumors
- Shared information

Information can deteriorate over time, introducing uncertainty and encouraging exploration and information gathering.

---

### Crew Management System

Simulates life aboard a ship.

Features include:

- Food and supply consumption
- Morale management
- Crew requirements
- Sailor loyalty
- Mutinies

---

### Weather System

A dynamic weather system that affects navigation, trading, encounters, and exploration.

---

### Crisis System

Manages global events capable of changing the economic, political, and social conditions of the game world.

---

### Quest System

A data-driven architecture for managing quests and missions.

Supports:

- Objectives
- Prerequisites
- Rewards
- Event-driven progression

---

### Dialogue System

A dialogue system integrated with reputation, diplomacy, and the current state of the world.

---

### AI System

A behavioral simulation system for autonomous characters and factions.

AI systems can handle:

- Trading
- Patrolling
- Target searching
- Threat avoidance
- Strategic navigation
- Autonomous world activities

This allows parts of the game world to continue operating independently of direct player interaction.

---

### Battle System

A turn-based naval combat system based on a **hexagonal grid**.

Features include:

- Tactical positioning
- Cannon range management
- Movement planning
- Ship orientation
- Ship-to-ship combat

Positioning and attack angles are fundamental elements of the combat strategy.

---

## Front-End & UI Engineering

The entire user interface has been designed and implemented by me.

The UI includes:

- Data Binding
- Dynamic tooltips
- Modal windows
- Drag & Drop interactions
- Dynamic lists
- Sorting
- Filtering
- Context menus
- Complex UI flows

The UI architecture follows **MVC and MVVM principles** to maintain a clear separation between presentation logic and application logic.

---

## Data Management

Greed World uses a two-level data architecture that separates static game content from dynamic runtime state.

### Static JSON Repository

Static game content is stored in JSON files and loaded into strongly typed serializable models.

Examples include:

- Items
- Ships
- Cities
- Kingdoms
- Classes
- Quests
- Effects

This approach allows game content to be modified independently from the core gameplay systems.

### Runtime Entity Database

Dynamic game state is managed through dedicated runtime repositories.

Advantages include:

- Scalability
- Maintainability
- Efficient data retrieval
- Separation between content and runtime state
- Reduced coupling between systems

---

## Design Patterns

Several software design patterns and architectural approaches have been used throughout development:

- Singleton
- Observer / Event Bus
- Factory
- Fluent Builder
- Strategy
- State Machine
- Repository
- Dependency Injection
- Command
- MVC
- MVVM
- ECS
- Data-Driven Design

The patterns are used according to the responsibilities of individual systems rather than as a rigid framework, with the goal of keeping the codebase modular and maintainable.

---

## Development Tools

Custom internal tools have been developed to improve development speed, debugging, testing, and data management.

These include:

- Custom Unity Editor windows
- Runtime debugging and visualization tools
- Automated data generators
- Inspection utilities
- Testing utilities

---

## Screenshots

<p align="center">
  <img width="450" alt="Screenshot #1" src="https://github.com/user-attachments/assets/e98a0dad-4fc9-4773-8747-82ceaae00930" />
  <img width="450" alt="Screenshot #2" src="https://github.com/user-attachments/assets/1f3fac4c-dc72-4591-8e02-9aa68db04560" />
  <img width="450" alt="Screenshot #3" src="https://github.com/user-attachments/assets/5c4dbfdb-8b63-4c93-a3e1-7423541172c6" />
  <img width="450" alt="Screenshot #4" src="https://github.com/user-attachments/assets/7146bae4-6ca9-4aac-bb92-a6ad85e68684" />
  <img width="450" alt="Screenshot #5" src="https://github.com/user-attachments/assets/83b37799-0ccc-45ca-99bb-889b120a39a3" />
</p>

---

## Project Status

The project is currently under active development.

The current version includes a playable prototype and continues to serve as a platform for experimenting with:

- Software architecture
- UI engineering
- Data-driven systems
- System design
- Game AI
- Simulation systems
- Scalable software patterns

---

## Source Code

The source code is maintained in a private repository.

This public repository serves as a **project showcase and technical documentation** of the architecture, systems, development practices, and software engineering concepts explored throughout the development of Greed World.

The repository focuses on documenting the technical challenges and architectural solutions rather than exposing the complete source code.
