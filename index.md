# 📘 **Software Requirement Specification (SRS)**

### Visual Novel Game (React + Canvas + Electron)

---

## **1. Introduction**

### 1.1 Purpose

The purpose of this document is to outline the requirements for a modular, visually expressive story game developed using **React** and **Canvas API**, and deployed for **desktop platforms** (Windows/macOS/Linux) using **Electron**. The game emphasizes **dynamic animations**, **player choices**, **state persistence**, and **cross-platform support**.

### 1.2 Scope

The game will feature:
- Dynamic character sprites with various poses and facial expressions.
- Multiple background scenes that change as the story progresses.
- Multiple music tracks and sound effects to enrich the experience.
- A flexible dialog system with branching choices.
- Save and load progress functionality.
- Multilingual support for a global audience.
- Cross-platform compatibility (Windows, macOS, Linux).
- A modular architecture supporting future scalability.
- GitHub CI/CD integration for builds, tests, and deployment.

### 1.3 Definitions, Acronyms, Abbreviations

|Term|Description|
|---|---|
|UI|User Interface|
|UX|User Experience|
|SFX|Sound Effect|
|CI/CD|Continuous Integration / Continuous Deployment|
|SRS|Software Requirements Specification|

### 1.4 References

- [GeeksforGeeks SRS Format](https://www.geeksforgeeks.org/software-requirement-specification-srs-format/)
- React Documentation: [https://reactjs.org/](https://reactjs.org/)
- Electron Documentation: [https://www.electronjs.org/](https://www.electronjs.org/)
- Canvas API: [https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)

---

## **2. Overall Description**

### 2.1 Product Perspective

This project is a standalone desktop application using Electron. It will render scenes and characters using the Canvas API and handle UI logic with React. The game will be easily expandable to support additional storylines, characters, and languages.

### 2.2 Product Functions

- Display characters with multiple poses and facial expressions.
- Change backgrounds dynamically as the story progresses.
- Play multiple music tracks and sound effects, enhancing the atmosphere.
- Provide dialog choices and branch storylines.
- Save and load progress.
- Support multiple languages.
- Deploy across desktop platforms.

### 2.3 User Classes and Characteristics

- **Players**: A global audience, no restrictions on languages or regions.
- **Developers**: Developers or modders interested in extending the story, characters, or translations.

### 2.4 Operating Environment

- OS: Windows 10+, macOS 12+, Linux Ubuntu 20.04+
- Node.js (for build tools)
- Electron Runtime
- Browsers supporting Canvas (for development/testing)

### 2.5 Design and Implementation Constraints

- The game will feature dynamic background changes.
- Characters will have multiple poses and facial expressions.
- Multiple music and sound effect tracks will be included.
- UI optimized for desktop platforms.

### 2.6 User Documentation

- In-game tutorial dialog.
- README with installation and usage instructions.
- Contribution guide for story/mod developers.

---

## **3. Specific Requirements**

### 3.1 External Interface Requirements

#### 3.1.1 User Interfaces

- React UI with minimalist layout: character view, dialog box, choice options.
- Language selector toggle.
- Save/load interface (simple buttons).

#### 3.1.2 Hardware Interfaces

- Standard keyboard and mouse support.

#### 3.1.3 Software Interfaces

- Canvas API for graphics.
- Web Audio API for music and sound.
- LocalStorage or filesystem-based saving via Electron.

#### 3.1.4 Communications Interfaces

- N/A (offline standalone application)

---

### 3.2 Functional Requirements

#### 3.2.1 Modular Architecture

- Components:
    
    - Dialog System
        
    - Character Renderer
        
    - Scene Manager
        
    - Audio Manager
        
    - Save/Load System
        
    - Localization Engine
        

#### 3.2.2 Dialog System

- Dynamic branching logic.
- JSON or similar format for dialog files.
- Dialog choices with consequences (affect future lines or endings).

#### 3.2.3 Character Management

- Character object with emotion state.
- Update facial expressions and poses based on dialog context.
- Dynamic animation: breathing, blinking, lip movement (CSS or Canvas).

#### 3.2.4 Save System

- JSON-based save file.
- Auto-save and manual save support.

#### 3.2.5 Scene Management

- Change background images dynamically depending on the progress of the story.
- Simple or complex transitions between scenes (fade, slide, etc.).

#### 3.2.6 Audio System

- Support for multiple music tracks.
- Support for multiple sound effects.
- Audio should transition smoothly during scene changes or dialogue events.

#### 3.2.7 Localization

- Game supports multilingual content.
- Language files managed as JSON or i18n library.
- In-game switch toggles language instantly.

#### 3.2.8 Cross-Platform Desktop Deployment

- Packaged using Electron for Windows, macOS, and Linux.
- Platform-specific settings like notifications and save directories.

#### 3.2.9 CI/CD Integration

- GitHub Actions workflows for:
    
    - Build on every push.
        
    - Run tests.
        
    - Create installers for each platform.
        
    - Auto-tag and release versions.
        

---

### 3.3 Performance Requirements

- Load game within 3 seconds on mid-range hardware.
- Maintain 60 FPS in UI and Canvas rendering.
- Audio playback without lag or noticeable delay.

---

### 3.4 Logical Database Requirements

- No external database.
- Use local file storage or localStorage for game saves and settings.

---

### 3.5 Design Constraints

- The game will feature **dynamic backgrounds**.
- **Multiple character poses** will be available.
- **Multiple music tracks** and **sound effects** will be implemented to enhance the atmosphere.

---

### 3.6 Software System Attributes

#### 3.6.1 Reliability

- Autosave and manual save reduce risk of data loss.
- Thorough error handling in dialog system and asset loading.

#### 3.6.2 Availability

- Always available locally once installed.
- No need for internet connection.

#### 3.6.3 Security

- Save files readable only by the user (handled via Electron's file system).

#### 3.6.4 Maintainability

- Clear modular structure.
- External story and localization files for easy editing.

#### 3.6.5 Portability

- Electron ensures compatibility across platforms.
- Configuration via environment variables or settings file.

---

### 3.7 Other Requirements

- The game will feature **multiple languages** for accessibility and audience reach.
- Dynamic and varied animations to engage players.
- Multiple music and sound effect tracks to complement the mood and tone of the story.
