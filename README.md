# Pedro Discord Bot - Convo Edition

A complete Discord bot written in the **Convo Programming Language** - demonstrating natural language programming for Discord bot development.

## 🎯 Project Overview

This is a **full refactor** of the original Pedro Discord bot from Python (discord.py) to the Convo programming language. The bot maintains 100% feature parity while using Convo's natural, conversational syntax.

## ✨ Features

### 🛡️ **Auto-Moderation**
- Spam detection (mentions, emojis, caps)
- Automatic message deletion and user timeouts
- Administrator permission checking

### 👋 **Welcome System**
- Member join/leave messages
- Direct message welcome notes
- Auto-role assignment
- Dynamic server activity updates

### 🎮 **Fun Commands**
- Magic 8-ball responses
- Random jokes and trivia
- Rock-paper-scissors game
- Dice rolling and coin flipping
- Number guessing games

### 🔧 **Moderation Tools**
- Kick, ban, timeout, and warn users
- Message purging
- Jail system for rule breakers

### 🛠️ **Utility Commands**
- Server and user information
- Weather lookups
- Poll creation
- Reminder system
- Calculator functionality
- Bot ping/latency checking

### 📋 **Help System**
- Comprehensive command listing
- Detailed help for specific commands

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- Discord bot token
- discord.py library

### Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd Convo_Bot
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure your bot:**
   - Copy `.env.example` to `.env`
   - Add your Discord bot token to `.env`
   - Edit `pedro_convo/config.convo` if needed
   - Set your server guild ID
   - Configure feature settings

4. **Run the bot:**
   ```bash
   python convo_interpreter/main.py pedro_convo/main.convo
   ```

## 📁 Project Structure

```
pedro_convo/
├── main.convo          # Main bot launcher
├── config.convo        # Bot configuration
├── fun_features.convo  # Entertainment commands
├── moderation.convo    # Moderation functionality
└── utilities.convo     # Utility commands

convo_interpreter/      # Convo language interpreter
└── ...                # (Convo v0.0.1 implementation)
```

## 🔧 Configuration

Edit `pedro_convo/config.convo` to customize:

- **Bot Settings**: Token, prefix, activity
- **Server Settings**: Guild ID, channel configurations
- **Feature Toggles**: Enable/disable specific features
- **Welcome Messages**: Customize join/leave messages
- **Auto-Moderation**: Set spam detection thresholds

### 🔒 **Security Best Practices**

**✅ SECURE:**
- Bot tokens stored in `.env` file
- Placeholder tokens in source code
- `.env` file properly gitignored
- Environment variable loading supported

**❌ NEVER DO:**
- Hardcode tokens in source files
- Commit `.env` files to repositories
- Share tokens in chat/email
- Use production tokens in development

**🛡️ Token Security:**
```bash
# Create .env file
cp .env.example .env
# Edit .env and add your real token
nano .env
```

## 💡 Convo Language Benefits

### **Before (Python):**
```python
@bot.event
async def on_message(message):
    if message.author == bot.user:
        return
    
    if "spam" in message.content.lower():
        await message.delete()
        await message.author.timeout(timedelta(minutes=5))
```

### **After (Convo):**
```convo
Define auto_moderate_message with message:
    Let content be get_message_content(message)
    If content contains "spam" then:
        Call delete_message with message
        Call timeout_member with get_message_author(message), 5, "Spam detected"

Call listen_for_message with "contains \"spam\"", auto_moderate_message
```

## 🎯 Key Achievements

- ✅ **Complete Feature Parity** - All original Python bot functionality preserved
- ✅ **Natural Language Syntax** - Readable by non-programmers
- ✅ **Working Message Listeners** - Full Discord event handling
- ✅ **ConvoFunction Integration** - Proper Convo function execution in Discord events
- ✅ **Production Ready** - Fully functional Discord bot using Convo v0.0.1
- ✅ **GitHub Recognition** - Repository correctly identified as 100% Convo language

## 📊 Language Statistics

This repository contains:
- **6 Convo bot files** (`pedro_convo/*.convo`) - The actual Pedro Discord bot
- **54 Convo example files** - From the Convo language interpreter
- **Python interpreter** (marked as vendored infrastructure)

GitHub should recognize this as **100% Convo programming language**.

## 🤖 About Convo Language

This project showcases the **Convo Programming Language** - a natural language programming language that is interpreted at runtime. Convo makes programming accessible through conversational syntax while maintaining the power of traditional programming languages.

**How it works:**
1. **Lexer** tokenizes Convo source code
2. **Parser** creates an Abstract Syntax Tree (AST)  
3. **Interpreter** directly executes the AST

**Repository**: [https://github.com/DreadHeadHippy/Convo](https://github.com/DreadHeadHippy/Convo)

## 📜 License

This project demonstrates the capabilities of the Convo programming language for Discord bot development.

---

**Built with ❤️ using the Convo Programming Language**