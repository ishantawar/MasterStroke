# System Design Document

## Overview
AI-powered web application that helps Indians discover government schemes. The system uses rule-based AI to analyze user profiles and match them with eligible government schemes. It's a static web application with no backend server required for MVP.

## Architecture

### System Architecture Diagram
```
┌─────────────────────────────────────────────────────────────┐
│                    User Browser                             │
│  ┌──────────────────────────────────────────────────────┐  │
│  │  HTML/CSS/JavaScript (Client-side)                  │  │
│  │  - UI Components                                    │  │
│  │  - AI Logic                                         │  │
│  │  - Search & Filter                                 │  │
│  └──────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────┘
                           ↓
┌─────────────────────────────────────────────────────────────┐
│              Static File Server (HTTP)                      │
│  - HTML files                                               │
│  - CSS files                                                │
│  - JavaScript files                                         │
│  - JSON database                                            │
└─────────────────────────────────────────────────────────────┘
```

### Components Overview
- **Frontend UI**: HTML/CSS/JavaScript interface
- **AI Engine**: Rule-based eligibility matching logic
- **Search Module**: Real-time search and filtering
- **Data Layer**: JSON database of schemes
- **Web Speech API**: Voice search capability

## Design Principles

### Core Principles
- **Simplicity**: No backend complexity for MVP
- **Performance**: < 1 second response time
- **Accessibility**: WCAG 2.1 compliant
- **Maintainability**: Clean, modular code
- **Scalability**: Can add more schemes easily

### Design Patterns
- **Module Pattern**: Separate concerns (search, filter, AI)
- **Observer Pattern**: Event listeners for user interactions
- **Factory Pattern**: Create recommendation objects
- **Singleton Pattern**: Single instance of data store
