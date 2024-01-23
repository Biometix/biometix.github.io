---
layout: page
title: FAQ
nav_order: 6
permalink: /faq/
---


# Frequently Asked Questions (FAQ)

## 1. How do I install Docker?

To install Docker, follow these steps:

- Download [Docker Desktop](https://www.docker.com/) for an easy-to-use graphical interface or [Docker Engine](https://docs.docker.com/engine/install/) for command-line installation.
- Follow the instructions provided on the official website. Note: You may need to sign up to get full access to Docker Desktop.

## 2. How do I start the Terminal to run scripts or Docker?

- **For Windows users:**
  - Press `Win + R` to open the Run dialog.
  - Type `cmd` or `powershell` and press Enter.

- **For Mac users:**
  - Press `Cmd + Space` to open Spotlight Search.
  - Type `Terminal` and press Enter.

- **For Linux users:**
  - Depending on the Linux distribution:
    - Press `Ctrl + Alt + T`.
    - Use a shortcut specific to your desktop environment.
    - Search for "Terminal" in the application menu.

## 3. How can I retrieve results when using the Web GUI interface?

Follow these steps to obtain results using the Web GUI interface:

1. Open your browser and visit the URL displayed in the terminal.
2. Drag or upload your images to the designated upload area.
3. Choose the desired model and click the "Submit" button.
4. Check the status of the task by clicking "Get Output." Wait until the task is marked as finished.
5. Press "Get Output" again, and export the data from the bottom of the page.

## 4. I encountered permission issues when running BQAT in the terminal. What should I do?

If you encounter permission issues, try the following:

- Prefix the command with `sudo` to run it with elevated privileges. For example:
  ```bash
  sudo your_bqat_command_here

