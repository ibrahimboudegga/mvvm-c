# MVVM-C Architecture Pattern

This repository introduces and demonstrates the **MVVM-C (Model-View-ViewModel-Coordinator)** architectural pattern, designed to enhance scalability, maintainability, and separation of concerns within complex user interfaces.

---

## Overview

### What is MVVM-C?
MVVM-C is a custom architectural pattern that extends the traditional **MVVM (Model-View-ViewModel)** approach by introducing a **Coordinator**. The **Coordinator** manages the flow of the parent screen and orchestrates communication between multiple subcomponents, each following its own **MVVM structure**. This approach prevents tight coupling and simplifies the handling of complex UI logic and navigation.

---

## Structure

- **Parent Screen (View)**: The primary screen, composed of multiple widget subviews.  
- **Coordinator**: Manages the lifecycle, interactions, and navigation logic of the parent screen and its subcomponents. It acts as the central controller for communication between sub-views.  
- **Sub-Views (View)**: Independent UI components within the parent screen, each represented by its own MVVM structure.  
- **ViewModel**: Contains the presentation logic for each corresponding sub-view.  
- **Model**: Represents the data layer, responsible for business logic and data handling.

---

## Why Use MVVM-C?

### Key Benefits
1. **Separation of Concerns**: Each sub-view is isolated with its own MVVM structure, making the codebase more modular and easier to maintain.
2. **Centralized Management**: The Coordinator simplifies handling complex UI flows by managing all interactions from a single point.
3. **Scalability**: Adding new views or modifying existing ones becomes straightforward without affecting other components.
4. **Improved Testability**: Isolated components following MVVM principles are easier to test independently.

---

## Example Workflow

1. **Demo Screen (DemoScreen)**:  
   A `DemoScreen` contains multiple subcomponents, such as `TokenView` and `ProductView` and `AddressSuggesstionsView`.  

2. **Coordinator (DemoCoordinator)**:  
   The `DemoCoordinator` manages the entire screen. It listens for events from `TokenView` or `ProductView` and orchestrates navigation or other actions.

3. **Sub-Views**:
   - **TokenView**: Consumes a Dummy JSON API that generates a random useless token.
   - **ProductView**: Consumes a Dummy JSON API that generates a random product.
   - **AddressSuggesstionsView**: Displays address suggesstions via a french API.

4. **Data Flow**:  
   The Coordinator handles events like button taps from `ProductView`, updates models if needed, and communicates changes back to the sub-views.

This architectural pattern was designed by my primary instructor, **Jewel CHERIAA**, a seasoned **Senior Mobile Application Developer** and **Software Architect** specializing in crafting robust architectural patterns for mobile frameworks, including **iOS**, **Android**, and **Flutter**. His expertise focuses on creating scalable, maintainable, and efficient solutions that enhance development practices and streamline application architecture.
