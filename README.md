# Labels Generator

A Visual Studio extension that streamlines the creation, validation, and translation of labels — directly from your development workflow.

---

## 🚀 Overview

**Labels Generator** simplifies how labels are created and maintained in Visual Studio projects.

Instead of manually editing label files, switching between tabs, or handling translations by hand, the extension provides integrated tools that allow you to create, validate, and translate labels directly from the IDE — including from the code editor itself.

It is designed to reduce context switching, prevent common mistakes, and keep label sets consistent across multiple languages.

---

## 🧰 Tool Window – Centralized Label Creation

Labels Generator provides a dedicated **Tool Window** where labels can be created and managed without leaving your current context.

Features include:
- Label ID input and generation
- Label text and description management
- One-click label creation
- Automatic copy of the label reference to the clipboard

<img width="499" height="306" alt="ffef1c17-b0f8-4535-8832-7a3fb3409158" src="https://github.com/user-attachments/assets/b9ce049f-4319-411d-a50e-c40f3ef12dc6" />

---

## 📝 Create Labels Directly from the Code Editor

Labels can be created **inline from the code editor**, allowing you to stay focused while writing code.

From the editor context menu, you can:
- Create a new label
- Automatically insert the label reference
- Avoid manual navigation to label files

<img width="876" height="409" alt="7d4eef85-a609-40f2-b46e-de01b2b2fbfb" src="https://github.com/user-attachments/assets/ae92ef62-473a-431c-a922-8cc08b1a1754" />

<img width="476" height="215" alt="a1a6aeab-7fc9-42eb-b664-65aa37817e1c" src="https://github.com/user-attachments/assets/5b0f4906-ac4e-4ccd-8cbe-64dd512f7370" />


---

## 🌍 Translation Support with DeepL

Labels Generator integrates with the **DeepL API** to translate labels into all languages derived from a selected master label file.

Features:
- Automatic translation on label creation
- Translation preview before commit
- On-the-fly editing of translated values
- Multi-language consistency checks

<img width="902" height="493" alt="72933873-008b-4799-a13b-fb93cbc61e86" src="https://github.com/user-attachments/assets/332555e6-d9cf-492c-a383-f0553ba40ff6" />

---

## ✍️ Spell Checking and Label Corrections

The extension includes built-in spell checking to detect and correct issues in label text.

Capabilities:
- Spell check validation via API
- Automatic fixes
- Developer-assisted fixes 

<img width="511" height="254" alt="4258f261-c9ce-4135-8888-7a04279a7f58" src="https://github.com/user-attachments/assets/6e06fd55-4c90-485b-b63e-6e455bbf414f" />


---

## 🔑 Automatic Label ID Management

To prevent common label-related errors, Labels Generator includes:
- Automatic label ID generation
- Duplicate label ID detection
- Validation before committing changes

This ensures label sets remain clean, consistent, and reliable across the project.

---

## ⚙️ Configuration Options

Labels Generator is configurable through Visual Studio’s **Options** panel.

### Source of Truth
Define:
- Package directory
- Master label file
- Derived language files

<img width="823" height="639" alt="055c822b-d0f5-453e-907c-733823acf423" src="https://github.com/user-attachments/assets/cbdaf9c3-1cdc-4c58-b108-b5e07f4d4d8d" />

---

### Behavior Settings
Control how labels are created and validated:
- Auto-fill descriptions using model name
- Automatic translation on creation
- Translation validation before commit
- Clipboard automation
- Spell check behavior
  
<img width="821" height="633" alt="bd1dcb8c-6b23-4ba4-96ba-348a8978abe8" src="https://github.com/user-attachments/assets/30e7e4e8-5dec-4030-83a6-6d9eacbceb10" />


---

### API Keys
Configure external services:
- Spell check API key
- Translation (DeepL) API key

<img width="819" height="632" alt="f6a4620e-a977-431e-a6a0-325c3bc23469" src="https://github.com/user-attachments/assets/9fa5aea5-ce99-41be-baad-36a79a25bce3" />


---

## 🧭 Menu Integration

Labels Generator integrates directly into Visual Studio menus for quick access to common actions:
- Generate labels
- Trim unused labels
- Create new labels

<img width="536" height="612" alt="f9c24341-13a6-43a8-b9c5-250bcc088774" src="https://github.com/user-attachments/assets/6e6b501f-f35f-468f-b17c-ffb7224c4f14" />

---

## 🎯 Who Is This Extension For?

- Projects with large or frequently changing label sets
- Multi-language applications
- Teams that want consistent label IDs and translations
- Developers who want faster, safer label workflows

---

## 🧠 Design Philosophy

- Minimal context switching
- Automation where it adds value
- Clear validation and feedback
- Developer experience first

---

## 🛠 Requirements

- Visual Studio (compatible versions)
- DeepL API key (for translation features)
- Internet connection for API-based services

---

## 📣 Feedback & Contributions

Feedback, bug reports, and feature suggestions are welcome.  
If you encounter issues or have ideas for improvement, feel free to open an issue or start a discussion.

---

## 📄 License

[Add your license here]
