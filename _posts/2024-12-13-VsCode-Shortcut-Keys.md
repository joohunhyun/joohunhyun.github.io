---
layout: post
title: (ENG) VsCode Shortcut Keys(MacOS)
date: 2024-12-13
description:
tags: tools
categories: study
typograms: true
pretty_table: true
---
💡익숙해진 단축키는 문서에서 삭제

💡원본은 .md 파일에 존안

---

**Table of contents**
- [VScode Shortcuts](#vscode-shortcuts)
- [VSCode git status](#vscode-git-status)


<br>

#### VScode Shortcuts

| Action                         | Shortcut                   |
|-------------------------------|--------------------------|
| **General**                    |                            |
| Open Command Palette           | `⇧ + ⌘ + P`                |
| Open Settings                  | `⌘ + ,`                    |
| Open Keyboard Shortcuts        | `⌘ + K ⌘ + S`              |
| Open Extensions View           | `⇧ + ⌘ + X`                |
| Show Integrated Terminal       | `⌃ + \`                    |
| Close Window                   | `⌘ + W`                    |
| Quit VSCode                    | `⌘ + Q`                    |
|                                |                             |
| **GitHub Copilot**             |                             |
| Accept Suggestion              | `Tab`                      |
| Next Suggestion                | `Option(Alt) + ]`          |
| Previous Suggestion            | `Option(Alt) + [`          |
| Show Suggestions               | `Ctrl + Enter`             |
| Approve Suggestion             | `Cmd + ←` or `Cmd + →`     |
|                                |                             |
| **File Management**            |                             |
| Open File                      | `⌘ + O`                    |
| Save File                      | `⌘ + S`                    |
| Save All Files                 | `⌥ + ⌘ + S`                |
| Close Editor                   | `⌘ + W`                    |
| Reopen Closed Editor           | `⇧ + ⌘ + T`                |
| New File                       | `⌘ + N`                    |
| Open Recent Files              | `⌘ + R`                    |
|                                |                             |
| **Editing**                    |                             |
| Cut Line                       | `⌘ + X`                    |
| Copy Line                      | `⌘ + C`                    |
| Paste                          | `⌘ + V`                    |
| Delete Line                    | `⇧ + ⌘ + K`                |
| Duplicate Line                 | `⇧ + ⌥ + ↓` or `⇧ + ⌥ + ↑` |
| Move Line Up/Down              | `⌥ + ↑` or `⌥ + ↓`         |
| Indent Line                    | `⌘ + ]`                    |
| Outdent Line                   | `⌘ + [`                    |
| Comment Line                   | `⌘ + /`                    |
| Add Multi-Cursor               | `⌥ + Click`                |
| Select All Occurrences         | `⌘ + ⇧ + L`                |
| Expand Selection               | `⇧ + ⌥ + →`                |
| Shrink Selection               | `⇧ + ⌥ + ←`                |
| Format Document                | `⇧ + ⌥ + F`                |
| Go to Matching Bracket         | `⇧ + ⌘ + \`                |
|                                |                             |
| **Navigation**                 |                             |
| Go to File                     | `⌘ + P`                    |
| Go to Line                     | `⌃ + G`                    |
| Go to Definition               | `F12`                      |
| Go to Implementation           | `⌘ + F12`                  |
| Show References                | `⇧ + F12`                  |
| Navigate Back                  | `⌃ + -`                    |
| Navigate Forward               | `⌃ + ⇧ + -`                |
|                                |                             |
| **Search and Replace**         |                             |
| Find                           | `⌘ + F`                    |
| Find in Files                  | `⇧ + ⌘ + F`                |
| Replace                        | `⌘ + ⌥ + F`                |
| Replace in Files               | `⇧ + ⌘ + H`                |
|                                |                             |
| **Debugging**                  |                             |
| Start/Continue Debugging       | `F5`                       |
| Step Over                      | `F10`                      |
| Step Into                      | `F11`                      |
| Step Out                       | `⇧ + F11`                  |
| Restart Debugging              | `⇧ + ⌘ + F5`               |
| Stop Debugging                 | `⇧ + F5`                   |
|                                |                             |
| **Terminal**                   |                             |
| Create New Terminal            | `⌘ + ⇧ + ``                |
| Split Terminal                 | `⌘ + \``                   |
| Kill Terminal                  | `⌘ + K` (inside terminal)  |
| Navigate Terminals             | `⌃ + ←` or `⌃ + →`         |
|                                |                             |
| **Version Control**            |                             |
| Open Source Control            | `⇧ + ⌘ + G`                |
| Commit Changes                 | `⌘ + Enter` (in source control) |

<br>

#### VSCode git status

| Code | Status      | Description                                                                 |
|------|-------------|-----------------------------------------------------------------------------|
| A    | Added       | This is a new file that has been added to the repository                   |
| M    | Modified    | An existing file has been changed                                          |
| D    | Deleted     | A file has been deleted                                                   |
| U    | Untracked   | The file is new or has been changed but has not been added to the repository yet |
| C    | Conflict    | There is a conflict in the file                                            |
| R    | Renamed     | The file has been renamed                                                 |
| S    | Submodule   | In repository exists another subrepository                                |
| T    | Typechange  | The file changed from symlink to regular file, or vice versa              |



<!-- 원본 (익숙해지면 하나씩 지우기)
| Action                         | Shortcut                   |
|-------------------------------|--------------------------|
| **General**                    |                            |
| Open Command Palette           | `⇧ + ⌘ + P`                |
| Open Settings                  | `⌘ + ,`                    |
| Open Keyboard Shortcuts        | `⌘ + K ⌘ + S`              |
| Open Extensions View           | `⇧ + ⌘ + X`                |
| Show Integrated Terminal       | `⌃ + \`                    |
| Close Window                   | `⌘ + W`                    |
| Quit VSCode                    | `⌘ + Q`                    |
|                                |                             |
| **File Management**            |                             |
| Open File                      | `⌘ + O`                    |
| Save File                      | `⌘ + S`                    |
| Save All Files                 | `⌥ + ⌘ + S`                |
| Close Editor                   | `⌘ + W`                    |
| Reopen Closed Editor           | `⇧ + ⌘ + T`                |
| New File                       | `⌘ + N`                    |
| Open Recent Files              | `⌘ + R`                    |
|                                |                             |
| **Editing**                    |                             |
| Cut Line                       | `⌘ + X`                    |
| Copy Line                      | `⌘ + C`                    |
| Paste                          | `⌘ + V`                    |
| Delete Line                    | `⇧ + ⌘ + K`                |
| Duplicate Line                 | `⇧ + ⌥ + ↓` or `⇧ + ⌥ + ↑` |
| Move Line Up/Down              | `⌥ + ↑` or `⌥ + ↓`         |
| Indent Line                    | `⌘ + ]`                    |
| Outdent Line                   | `⌘ + [`                    |
| Comment Line                   | `⌘ + /`                    |
| Add Multi-Cursor               | `⌥ + Click`                |
| Select All Occurrences         | `⌘ + ⇧ + L`                |
| Expand Selection               | `⇧ + ⌥ + →`                |
| Shrink Selection               | `⇧ + ⌥ + ←`                |
| Format Document                | `⇧ + ⌥ + F`                |
| Go to Matching Bracket         | `⇧ + ⌘ + \`                |
|                                |                             |
| **Navigation**                 |                             |
| Go to File                     | `⌘ + P`                    |
| Go to Line                     | `⌃ + G`                    |
| Go to Definition               | `F12`                      |
| Go to Implementation           | `⌘ + F12`                  |
| Show References                | `⇧ + F12`                  |
| Navigate Back                  | `⌃ + -`                    |
| Navigate Forward               | `⌃ + ⇧ + -`                |
|                                |                             |
| **Search and Replace**         |                             |
| Find                           | `⌘ + F`                    |
| Find in Files                  | `⇧ + ⌘ + F`                |
| Replace                        | `⌘ + ⌥ + F`                |
| Replace in Files               | `⇧ + ⌘ + H`                |
|                                |                             |
| **Debugging**                  |                             |
| Start/Continue Debugging       | `F5`                       |
| Step Over                      | `F10`                      |
| Step Into                      | `F11`                      |
| Step Out                       | `⇧ + F11`                  |
| Restart Debugging              | `⇧ + ⌘ + F5`               |
| Stop Debugging                 | `⇧ + F5`                   |
|                                |                             |
| **Terminal**                   |                             |
| Create New Terminal            | `⌘ + ⇧ + ``                |
| Split Terminal                 | `⌘ + ``                    |
| Kill Terminal                  | `⌘ + K` (inside terminal)  |
| Navigate Terminals             | `⌃ + ←` or `⌃ + →`         |
|                                |                             |
| **Version Control**            |                             |
| Open Source Control            | `⇧ + ⌘ + G`                |
| Commit Changes                 | `⌘ + Enter` (in source control) | -->