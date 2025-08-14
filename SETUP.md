# Discord Guardian 2025 - Setup Guide

## Prerequisites

- Node.js 16.0.0 or higher
- MongoDB (local or cloud)
- Discord Bot Token
- Discord Application ID

## Installation Steps

### 1. Clone the Repository

```bash
git clone https://github.com/NawNawNawNAw/Discord-Guardian-2025.git
cd Discord-Guardian-2025
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Environment Configuration

1. Copy the example environment file:
   ```bash
   cp .env.example .env
   ```

2. Edit `.env` file with your configuration:
   ```env
   DISCORD_TOKEN=your_discord_bot_token_here
   CLIENT_ID=your_application_id_here
   MONGODB_URI=mongodb://localhost:27017/discord-guardian
   GUILD_ID=your_guild_id_here  # Optional: for faster development
   DEFAULT_LANGUAGE=en
   ```

### 4. Discord Bot Setup

1. Go to [Discord Developer Portal](https://discord.com/developers/applications)
2. Create a new application
3. Go to "Bot" section and create a bot
4. Copy the bot token to your `.env` file
5. Enable the following bot permissions:
   - Send Messages
   - Manage Messages
   - Manage Channels
   - Ban Members
   - Kick Members
   - Manage Roles
   - Connect (for voice)
   - Speak (for voice)

### 5. Invite Bot to Server

Generate an invite link with the following scopes and permissions:
- Scopes: `bot`, `applications.commands`
- Permissions: Administrator (or the specific permissions listed above)

### 6. Deploy Commands

```bash
npm run deploy
```

### 7. Start the Bot

```bash
# Production
npm start

# Development (with auto-restart)
npm run dev
```

## MongoDB Setup

### Local MongoDB
1. Install MongoDB on your system
2. Start MongoDB service
3. Use connection string: `mongodb://localhost:27017/discord-guardian`

### MongoDB Atlas (Cloud)
1. Create account at [MongoDB Atlas](https://www.mongodb.com/atlas)
2. Create a cluster
3. Get connection string and add to `.env`

## Configuration

### Language Support
The bot supports English (`en`) and Arabic (`ar`). Set the default language in your `.env` file:
```env
DEFAULT_LANGUAGE=en  # or 'ar' for Arabic
```

### Guild-specific Settings
Users with appropriate permissions can change the server language using:
```
/lang set language:ar
```

## Available Commands

### Member Management
- `/ban` - Ban a member
- `/kick` - Kick a member
- `/warn` - Warn a member
- `/mute` - Mute a member

### Channel Management
- `/clear` - Clear messages
- `/lock` - Lock a channel
- `/unlock` - Unlock a channel
- `/slowmode` - Set slowmode

### Music (if enabled)
- `/play` - Play music
- `/stop` - Stop music
- `/skip` - Skip current song
- `/queue` - Show music queue
- `/volume` - Adjust volume

### Utility
- `/help` - Show all commands
- `/lang` - Change server language

## Troubleshooting

### Common Issues

1. **Bot not responding to commands**
   - Check if commands are deployed: `npm run deploy`
   - Verify bot has necessary permissions
   - Check console for errors

2. **Database connection issues**
   - Verify MongoDB is running
   - Check connection string in `.env`
   - Ensure network access (for Atlas)

3. **Permission errors**
   - Ensure bot role is above roles it needs to manage
   - Check bot permissions in server settings

### Logs
Check console output for detailed error messages and bot status.

## Support

For issues and questions:
1. Check this setup guide
2. Review console logs
3. Create an issue on GitHub

## License

MIT License - see LICENSE file for details.