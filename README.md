# Multi-Window iOS Browser

A high-performance, native iOS application built with **Swift** that enables true multitasking. This browser allows users to manage multiple concurrent window instances to view PDFs and photos side-by-side, overcoming the "single-task" limitations of standard mobile browsers.

## 🚀 Key Features
*   **Multi-Window Architecture:** Full implementation of Scene-based architecture, allowing multiple independent app instances on iPadOS and iOS.
*   **Integrated Document Viewer:** Native rendering of PDFs using **PDFKit** with support for zooming, scrolling, and thumbnail navigation.
*   **High-Resolution Media Handling:** Leverages the **QuickLook** framework for high-fidelity image rendering and seamless document interaction.
*   **Productivity UI:** Optimized for split-view and slide-over functionality to enhance user workflow.

## 🛠️ Technical Stack
*   **Language:** Swift 5.0+
*   **Frameworks:** UIKit, PDFKit, QuickLook, Foundation
*   **Architecture:** SceneDelegate (Multitasking support)
*   **Tools:** Xcode 15+

## 🧠 Technical Challenges & Learnings
*   **Scene Lifecycle Management:** One of the primary challenges was ensuring independent state persistence across multiple windows. I implemented unique session identifiers to prevent data leakage between concurrent scenes.
*   **Memory Optimization:** Rendering multiple high-resolution PDFs and photos simultaneously requires careful memory management. I utilized background threading and lazy loading to ensure the UI remains responsive at 60 FPS.
*   **Framework Mastery:** Deep-dived into `PDFView` and `QLPreviewController` to provide a "desktop-class" document interaction experience on mobile.

## 📂 Project Structure
* `SceneDelegate.swift`: Manages the multi-window lifecycle and configuration.
* `BrowserViewController.swift`: Core logic for URL handling and multi-window instantiation.
* `DocumentPreviewManager.swift`: Handles the rendering of PDF and Image assets via PDFKit and QuickLook.

## 📖 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git](https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git)
