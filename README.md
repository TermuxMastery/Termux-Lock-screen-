### 🔒 Termux Lock Screen 🔒

Secure your Termux environment with a password or PIN! Perfect for keeping your sessions private and adding an extra layer of security.

✨ Features ✨

🔑 Password or PIN protection

💬 Customizable lock messages

🔔 Optional sound alerts

⚡ Lightweight and easy-to-use

### 📁 Termux Storage Commands
Grant Storage Permission
Before accessing storage, you need permission:
```
termux-setup-storage
```
### ✅ Update package lists
Fetches the latest list of available packages and versions.
Does not upgrade packages yet.
```
pkg update && pkg upgrade
```
### 📂 Termux Bash Configuration

This repository demonstrates how to customize your Termux terminal using the ~/.bashrc file. Opened with the Nano text editor, this file allows you to personalize your environment with:

⚡ Aliases – Shortcuts for frequently used commands

🌐 Environment variables – Customize paths, prompts, and more

🔒 Startup scripts – Run scripts automatically when Termux launches

🎨 Prompt styling – Add colors, emojis, or ASCII art for a fun terminal
```
nano ~/.bashrc
```
```
#!/bin/bash
# Termux Lock Screen 🔐
# Password: 123456

# --------------------------
# Colors for styling
# --------------------------
RED="\e[31m"
GREEN="\e[32m"
YELLOW="\e[33m"
CYAN="\e[36m"
MAGENTA="\e[35m"
RESET="\e[0m"

# --------------------------
# Header function
# --------------------------
header() {
    clear
    echo -e "${MAGENTA}╔══════════════════════════════╗${RESET}"
    echo -e "${CYAN}       🔐 Termux Lock Screen 🔐      ${RESET}"
    echo -e "${MAGENTA}╚══════════════════════════════╝${RESET}"
    echo ""
}

# --------------------------
# Lock screen function
# --------------------------
lock_screen() {
    header
    read -sp "Enter Password 🔑: " password
    echo ""
    if [ "$password" == "123456" ]; then
        echo -e "${GREEN}Access Granted ✅${RESET}"
        sleep 1
        clear
    else
        echo -e "${RED}Access Denied ❌ Try Again!${RESET}"
        sleep 1
        lock_screen
    fi
}

# --------------------------
# Start lock screen
# --------------------------
lock_screen
```
🔐 Termux Lock Screen (Password Protected)

A beautiful and lightweight Termux lock screen script written in Bash, designed to protect your Termux environment with a password.

This lock screen shows a colorful, emoji‑styled interface and keeps looping until the correct password is entered.

✨ Features

🔑 Password protection (default: 123456)

🎨 Colorful & clean terminal UI

😊 Emoji‑based design

🔄 Retry until correct password

⚡ Lightweight & fast

🛠️ Easy to customize

[![YouTube](https://img.shields.io/badge/YouTube-🔥TermuxMastery🔥-ff0000?style=for-the-badge&logo=youtube&logoColor=ffffff)](https://youtube.com/@termuxmastery?si=U8LvcGiAJZES7YHE)




