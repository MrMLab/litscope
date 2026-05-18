# 🔬 LitScope

> **Incredible Search for Credible Research.**

🔗 **Access the website [Here!](https://mrmlab.github.io/litscope)**

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg?style=flat-square)](#)
[![Version](https://img.shields.io/badge/version-1.0.0-blue.svg?style=flat-square)](#)
[![React](https://img.shields.io/badge/React-19.0-61dafb.svg?style=flat-square&logo=react)](#)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-v4.0-38b2ac.svg?style=flat-square&logo=tailwind-css)](#)
[![Security](https://img.shields.io/badge/Security-Hardened-red.svg?style=flat-square)](#)

---

## 📖 Executive Overview

**LitScope** is a high-performance, precision-driven academic search engine designed for researchers, academics, and professionals. It bridges the gap between global scientific literature and regional/international indexing standards. 

By seamlessly integrating real-time data from massive open-source bibliographic catalogs with a proprietary, cryptographically secured indexing database, LitScope instantly evaluates the credibility and tier of millions of academic papers. It automatically cross-references publications against **Scopus (Q1–Q4)** and **SINTA (S1–S6)** indices, providing users with a unified, lightning-fast dashboard to discover highly credible, peer-reviewed research.

## ✨ Key Features & Advantages

*   **🎯 Precision Search & Filtering:** Granular search capabilities allowing users to filter by specific SINTA tiers, Scopus quartiles, Open Access availability, publication years, and article limits.
*   **🧠 Intelligent Cross-Indexing Engine:** Automatically maps fetched academic papers to their respective journal indexing tiers using a proprietary, high-speed matching algorithm.
*   **🛡️ Enterprise-Grade Client Security:** Built with an active runtime shield. The application features robust anti-tampering mechanisms, domain-locking, and dynamic DevTools countermeasures to protect proprietary data and business logic.
*   **⚡ Edge-Optimized Cryptographic Pipeline:** Utilizes encrypted datasets delivered via edge networks, ensuring that proprietary indexing data is decrypted and processed entirely in-memory without leaving traces.
*   **🔐 Seamless Access Management:** Integrated deeply with the Finscope authentication ecosystem, offering fluid transitions between limited free-trial experiences and premium, unrestricted access.

---

## 🏗️ High-Level System Architecture

LitScope is designed with a modern, decoupled, and highly secure architecture. The system relies on a reactive frontend that orchestrates data from multiple external and internal endpoints through a secure data pipeline.

### 1. Data Flow & Processing Pipeline
1.  **Query Ingestion:** User inputs are sanitized and normalized within the React application.
2.  **Global Metadata Fetching:** The system communicates with global bibliographic APIs (e.g., OpenAlex) to retrieve massive sets of raw academic metadata (DOIs, abstracts, ISSNs, authorships).
3.  **Encrypted Data Delivery:** A highly compressed, AES-encrypted proprietary indexing database is fetched from an Edge network (Cloudflare Pages).
4.  **In-Memory Decryption & Matching:** 
    *   The proprietary database is decrypted *on-the-fly* directly in the client's memory.
    *   A heuristic matching engine correlates the raw academic metadata (via identifiers like ISSN) against the decrypted database to assign accurate SINTA and Scopus scoring.
5.  **UI Hydration:** The enriched, scored data is fed back into the React state, rendering interactive, color-coded cards highlighting journal credibility.

### 2. Operational Security (OPSEC) & Runtime Shield
To protect the proprietary matching engine and encrypted datasets, LitScope implements a multi-layered client-side security protocol:
*   **Environment Validation:** Continuous checks against allowed execution environments (e.g., domain whitelisting, viewport anomaly detection).
*   **Debugger & Inspection Traps:** Active DOM and memory monitoring that neutralizes attempts to open browser developer tools or inject malicious inspection scripts.
*   **Network Request Interception:** Native fetch and XHR prototypes are wrapped in a security layer that halts execution and isolates data if tampering is detected.

### 3. Authentication & Monetization Edge
Authentication operations are offloaded to secure Serverless Edge Workers. 
*   **Stateless Verification:** Verifies user credentials against the Finscope ecosystem without exposing backend databases to the client.
*   **Local State Management:** Manages trial limits and subscription states securely using encrypted local storage states, triggering premium upgrade flows seamlessly.

---

## 🛠️ Tech Stack

**Frontend & UI**
*   **React (v19):** Core library for reactive UI components and state management.
*   **Tailwind CSS (v4):** Utility-first framework for responsive, elegant, and modern styling.
*   **Lucide React:** Lightweight, customizable icon set.

**Security & Cryptography**
*   **CryptoJS:** Utilized for secure, in-memory AES decryption of proprietary databases.
*   **Custom Anti-Reversing Engine:** Proprietary JavaScript obfuscation and runtime environment checks.

**Data & Infrastructure**
*   **OpenAlex API:** Primary source for open academic metadata.
*   **Cloudflare Pages / Workers:** Distributed edge delivery for encrypted datasets and serverless authentication endpoints.

---

## ⚖️ Copyright & License

**© Mr. M. All rights reserved.**

*This software and its underlying architecture are proprietary. Unauthorized copying, reverse engineering, distributing, or modifying of the source code, via any medium, is strictly prohibited.*

**Interested in the source code or a custom implementation?**  
For business inquiries, collaborations, or source code requests, please reach out via the contact channels available directly on my **[Portfolio Website](https://mrmlab.github.io)**.
