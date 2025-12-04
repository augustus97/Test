# StreamElements Commands Database

This repository contains external command databases for StreamElements chatbot commands. Each file contains multiple message variations that are randomly selected when commands are used in Twitch chat.

## 🎯 Purpose

StreamElements has a 500-character limit per command, which restricts the number of random message variations you can include. By hosting the messages externally on GitHub, we can have unlimited variations while keeping the StreamElements commands lightweight.

## 📁 File Structure

Each `.txt` file corresponds to a specific chat command:

- `hug.txt` - Hug command variations

## 🔧 How It Works

1. **External Storage**: Command messages are stored in these text files
2. **StreamElements Integration**: Commands use `${customapi}` to fetch random messages
3. **Dynamic Content**: Each command execution pulls a fresh random message
4. **Unlimited Variations**: No character limits on external files

## 💬 StreamElements Setup

Use this format in your StreamElements dashboard:

```
!command edit !hug ${customapi https://raw.githubusercontent.com/augustus97/main/hug.txt}
```

## 📝 Message Format

Messages use StreamElements variables:
- `${sender}` - The user who triggered the command
- `${1}` - The target user (first parameter)

Example: `${sender} gives ${1} a big hug!` becomes "Tozuka1 gives teddie a big hug!"

## 🎮 Commands Available

- `!hug @username` - Send virtual hugs

## 🔄 Updates

Messages can be updated anytime by editing the files. Changes take effect immediately in StreamElements.

---

*Created for enhanced Twitch chat interaction via StreamElements*
