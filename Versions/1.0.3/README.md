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

## 💼 TODOs



## 📋 Patch notes

### Label Manager version 1.2.0
 
- Improvements & UI Enhancements

New lines are now inserted at the top of the label instead of the bottom when appending.

Text input now scrolls with the cursor inside the Label Manager window, making it easier to see what you’re typing.

Adjusted textbox sizes (Label ID, Description, Corrected Label) to ensure descenders (g, p, y, etc.) are fully visible.

Refined the Label Manager window UI for a cleaner, more consistent look.
 
- New Features


Recent Labels: the last 5 generated labels are now saved for quick access.

    Double-click a label to copy it and paste it where needed.
 
- Behavior Changes

Removed the warning shown on Visual Studio startup when the solution is not in the current model.

        The warning is now displayed only when label creation is triggered.

Spellcheck behavior improved:

        Spellcheck options are now disabled (greyed out) unless Allow spellcheck is enabled.

---

### Label Manager version 1.3.0

## Bug Fixes

Fixed the Trim Labels command removing all labels from child files instead of only obsolete ones. The bug was caused by label lines being identified by `StartsWith("Label")`, which failed for any non-`Label`-prefixed ID (e.g. `OA`).

Fixed the Generate Labels command incorrectly using the first child file as the reference, which could cause a newly created file to report no missing labels.

Fixed the Similar Label dialog placing the label reference when Cancel was pressed, due to the decision checks being evaluated in the wrong order.

## New Features

Generate Labels — per-file target selection: a dialog now lets you choose which label file to use as the reference for detecting missing labels, with two modes: *Only this file* or *All files* (each file gets only its own missing labels). An option to clear the selected file before adding labels is also available.

Label similarity detection: the Create Label tool window now warns when the entered label text is similar to an existing one, showing both labels side by side and letting you choose to copy the reference, create anyway, or cancel.

Spellcheck reintroduced using LanguageTool (replaced the previous third-party API).

Language Mapping options page reworked: redesigned with a proper add form (Source + Target fields) instead of inline DataGrid editing. Add and Remove now save immediately so mappings can be tested right away via the Test Languages button.

Config — max recent labels & similarity threshold: both values are now configurable in Behavior Options instead of being hardcoded.

Label ID auto-generator improvements: the generator now produces more descriptive IDs by prioritising domain objects before intent keywords (e.g. `VendorInactive` instead of `CannotBe`). Added contraction normalisation (`isn't` → `is not`), numeric suffix fallback when all candidates are taken, expanded domain and attribute vocabularies, crash guard on empty tokens, and new intent rules for `inactive`, `mandatory`, `cannot be empty`, and others.

## Adjustments

Similar label dialog now places the label reference directly into the file instead of copying to clipboard.

All dialogs now spawn at the center of the screen.

Package validation check added to the Trim Labels command.

Font weight and size aligned across dialogs for visual consistency.

