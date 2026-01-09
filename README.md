# Labels Generator 


[![Labels Generator](Images/Icon_96.png)](https://marketplace.visualstudio.com/items?itemName=DiogoPinheiro.LabelManager)


A Visual Studio extension that streamlines the creation, validation, and translation of labels — directly from your development workflow.



 **[Get it on Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=DiogoPinheiro.LabelManager)**

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

![alt text](<Images/Tool Window – Centralized Label Creation.png>)

---

## 📝 Create Labels Directly from the Code Editor

Labels can be created **inline from the code editor**, allowing you to stay focused while writing code.

From the editor context menu, you can:
- Create a new label
- Automatically insert the label reference
- Avoid manual navigation to label files

![alt text](<Images/Create Labels Directly from the Code Editor.png>)

![alt text](<Images/Create Labels Directly from the Code Editor2.png>)


---

## 🌍 Translation Support with DeepL

Labels Generator integrates with the **DeepL API** to translate labels into all languages derived from a selected master label file.

Features:
- Automatic translation on label creation
- Translation preview before commit
- On-the-fly editing of translated values

![alt text](<Images/Translation Support with DeepL.png>)

---

## ✍️ Spell Checking and Label Corrections Support with Apilayer Spell Checker API

The extension includes built-in spell checking to detect and correct issues in label text.

Capabilities:
- Spell check validation via API
- Automatic fixes
- Developer-assisted fixes 

![alt text](<Images/Spell Checking and Label Corrections.png>)


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
- Derived language files are selected automatically

![alt text](<Images/Source of Truth.png>)


### Behavior Settings
Control how labels are created and validated:
- Auto-fill descriptions using model name
- Auto-fill Label ID
- Automatic translation on creation
- Translation validation before commit
- Clipboard automation
- Spell check behavior
  
![alt text](<Images/Behavior Settings.png>)


### API Keys
Configure external services:
- Spell check (Apilayer Spell Checker API) API key
- Translation (DeepL) API key

![alt text](<Images/API Keys.png>)


### Language Mappings
Define how source languages are mapped to target languages during translation.
- Example: mapping `ar-sa` to `ar` ensures that content detected as `ar-sa` is translated to `ar`.



![alt text](<Images/Language Mappings.PNG>)


---

## 🧭 Menu Integration

Labels Generator integrates directly into Visual Studio menus for quick access to common actions:
- Generate labels – Useful for translating new labels in bulk when the “Automatic translation on creation” option is disabled.
- Trim unused labels – Deletes labels that exist in slave label files but do not exist in the master file.
- Open Create new labels Tool Window

![alt text](<Images/Menu Integration.png>)

---

## ⌨️ Keyboard Shortcuts (Key Bindings)

Labels Generator provides **chord-based keyboard shortcuts** to access its main features quickly without leaving the editor.

All shortcuts use a **two-step chord**, starting with `Ctrl + Alt + M`, followed by an action key.

### Available Shortcuts

| Action | Shortcut |
|------|----------|
| Create a new label (inline from the editor) | **Ctrl + Alt + M, N** |
| Open the Create Label Tool Window | **Ctrl + Alt + M, L** |
| Generate labels | **Ctrl + Alt + M, G** |

### How Chord Shortcuts Work

1. Press **Ctrl + Alt + M**
2. Release the keys
3. Press the second key (`N`, `L`, or `G`)

This approach keeps shortcuts organized, avoids conflicts with existing Visual Studio bindings, and makes them easy to remember.

### Customizing Shortcuts

All shortcuts can be customized through Visual Studio:

**Tools → Options → Environment → Keyboard**

Search for commands containing with:

Label

You can reassign any shortcut to better match your personal workflow.

---

## 🎯 Who Is This Extension For?

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
- Apilayer Spell Checker API (for Spell Check features)
- Internet connection for API-based services

---

## 📣 Feedback & Contributions

Feedback, bug reports, and feature suggestions are welcome.  
If you encounter issues or have ideas for improvement, feel free to open an issue or start a discussion.

---

## 📄 Contribute

After cloning the repository, **rename the root folder** to `LabelsGeneratorRepo` (or any name different from `Labels Generator`).

Using the same name for the repository root and the project folder can cause Visual Studio and NuGet resolution issues.

