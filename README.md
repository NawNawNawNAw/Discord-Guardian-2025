# Discord Guardian 2025

A comprehensive Discord bot for server management and security with multilingual support (Arabic/English).

## Features

- 🛡️ **Security & Protection**: Anti-join protection, whitelist management, verification system
- 👥 **Member Management**: Ban, kick, mute, warn, role management
- 🔧 **Channel Management**: Lock/unlock channels, slowmode, message clearing
- ⚙️ **Server Configuration**: Language settings, logging, bot customization
- 🌐 **Multilingual Support**: Full Arabic and English language support

## Commands

### Member Management
- `/ban` - Ban a member from the server
- `/kick` - Kick a member from the server
- `/mute` - Temporarily mute a member
- `/warn` - Warn a member
- `/role` - Add or remove roles from members

### Channel Management
- `/clear` - Delete messages (max 100)
- `/lock` - Lock a text channel
- `/unlock` - Unlock a text channel
- `/slowmode` - Set slowmode for a channel

### Security & Protection
- `/antijoin` - Anti-join protection settings
- `/whitelist` - Manage server whitelist
- `/verify` - Set up verification system

### Configuration
- `/lang` - Change bot language
- `/setlog` - Set logging channel
- `/help` - Display all available commands

## Installation

1. Clone this repository
2. Install dependencies: `npm install`
3. Configure your bot token and database
4. Run the bot: `node index.js`

## Requirements

- Node.js v16 or higher
- Discord.js v14
- MongoDB (for configuration storage)

## License

MIT License