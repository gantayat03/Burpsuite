# Burp Suite Basics – A Beginner's Walkthrough

## Introduction

Burp Suite is a powerful and widely-used framework for **web application security testing**. Built in **Java**, it serves as a comprehensive solution for penetration testers, bug bounty hunters, and cybersecurity professionals aiming to identify and exploit vulnerabilities in web applications.

Over time, it has become the **industry standard** for ethical hacking and vulnerability assessment due to its flexibility, modular design, and extensive feature set.

---

## How It Works

At its core, Burp Suite operates as an **intercepting proxy**. It captures, inspects, and modifies all **HTTP and HTTPS traffic** flowing between your browser and the target server. This ability forms the **backbone of the entire framework**.

By sitting in the middle of this communication channel, Burp allows you to:
- Modify requests *before* they reach the server
- Tamper with responses *before* they are rendered in the browser
- Log, analyze, and replay traffic to uncover hidden security flaws

This kind of control makes it invaluable for testing input validation, session handling, authorization, and much more.

---

## Editions of Burp Suite

Burp Suite comes in three editions, each catering to different use cases:

### 1. Community Edition
- Completely **free** and ideal for learners.
- Includes core features like Proxy, Repeater, Intruder (with limitations).
- Does not support automated scanning or saving projects across sessions.

### 2. Professional Edition
- A **paid upgrade** that unlocks the full potential of Burp Suite.
- Features include: 
  - An automated vulnerability scanner
  - Burp Collaborator for out-of-band testing
  - Project saving and advanced tools
- Ideal for security researchers and professional penetration testers.

### 3. Enterprise Edition
- Designed for **automated and continuous scanning** at scale.
- Deployed on servers and integrated with CI/CD pipelines.
- Targets organizations with ongoing application security needs.

---

## Core Tools in Burp Suite (Community Edition)

Even in its free form, Burp Suite offers a rich set of tools that are critical for manual testing:

### 🔹 Proxy
- The most essential component.
- Intercepts live requests and responses.
- Lets you inspect and modify HTTP messages in real-time.

### 🔹 Repeater
- Allows you to resend custom requests multiple times.
- Ideal for **manual testing** of payloads and observing server behavior.
- Useful in injection-based attacks like **SQL Injection**, **XSS**, etc.

### 🔹 Intruder
- Automates sending payloads to endpoints.
- Supports brute-forcing, fuzzing, and enumeration.
- Community edition has speed and functionality limitations.

### 🔹 Decoder
- Used for encoding and decoding data.
- Supports formats like Base64, URL encoding, Hex, and more.
- Handy when dealing with obfuscated or encoded payloads.

### 🔹 Comparer
- Highlights differences between two pieces of data.
- Can compare at word or byte level.
- Useful in identifying how requests or responses change during testing.

### 🔹 Sequencer
- Analyzes randomness in tokens like session IDs.
- Helps determine if token generation is predictable or weak.

### 🔹 Extender
- Allows integration of third-party and custom-built extensions.
- Example: `Logger++` adds advanced logging capabilities.
- Empowers users to expand Burp’s functionality based on their needs.

---

## Understanding the Burp Suite Dashboard

Burp Suite's **Dashboard** gives a centralized view of its internal operations. It is split into four main quadrants:

1. **Task Menu**  
   Displays background tasks that are running, such as scans or crawls.

2. **Event Log**  
   Tracks all actions taken by Burp, including connections and module activities.

3. **Issue Activity** *(Professional only)*  
   Lists detected vulnerabilities from automated scans.

4. **Advisory** *(Professional only)*  
   Provides detailed information about each discovered issue, including severity, description, and remediation guidance. These can be exported in reports.

---

## Navigating Through Burp Suite

Burp Suite uses a **tab-based interface**, where each tool/module has its own section. The top menu bar helps you switch between modules such as Proxy, Repeater, Intruder, etc.

### Detachable Tabs
- Tabs can be **detached into separate windows**, useful for multitasking or dual-monitor setups.
- You can **reattach** them anytime using the same option.

### Keyboard Shortcuts

```bash
Ctrl + Shift + D   → Dashboard
```
```bash
Ctrl + Shift + T   → Target tab
```
```bash  
Ctrl + Shift + P   → Proxy
```
```bash 
Ctrl + Shift + I   → Intruder
```
```bash  
Ctrl + Shift + R   → Repeater
```

_Started learning on [My TryHackMe](https://tryhackme.com/p/shreyagantayat03) — Let’s lock it in!_
