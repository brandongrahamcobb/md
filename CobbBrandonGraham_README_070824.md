---

# How to Create a Discord Bot Token

This guide will walk you through the steps to create a Discord bot token, which is essential for running and managing your Discord bot.

## Prerequisites

1. **Discord Account**: You need a Discord account to create and manage a bot. If you don't have one, [sign up here](https://discord.com/register).

2. **Discord Developer Portal Access**: You will use the Discord Developer Portal to create and manage your bot.

## Steps to Create a Discord Bot Token

### 1. Log in to Discord Developer Portal

1. Go to the [Discord Developer Portal](https://discord.com/developers/applications).
2. Log in with your Discord account credentials.

   ![Step 1 - Log in](png/CobbBrandonGraham_base_030824.png)

### 2. Create a New Application

1. Click on the **"New Application"** button in the top right corner.
2. Enter a name for your application and click **"Create"**. This will create a new application that you can use for your bot.

   ![Step 2 - Create Application](png/CobbBrandonGraham_create_030824.png)

### 3. Set Up Your Bot

1. In the application settings page, go to the **"Bot"** tab on the left-hand menu.
2. Click the **"Add Bot"** button and confirm by clicking **"Yes, do it!"**. Your bot will be created, and you will be redirected to the bot settings page.

   ![Step 3 - Add Bot](png/CobbBrandonGraham_created_030824.png)

### 4. Get Your Bot Token

1. In the bot settings page, you will see a **"Token"** section.
2. Click on the **"Copy"** button to copy your bot token to the clipboard. This token is what your bot will use to authenticate with the Discord API.

   ![Step 4 - Get Token](png/CobbBrandonGraham_reset_030824.png)

### 5. Keep Your Token Secure

- **Important**: Keep your bot token private. Do not share it with anyone or post it publicly. If someone gets hold of your token, they can control your bot.
- If you believe your token has been compromised, you can regenerate it by clicking the **"Regenerate"** button in the Token section.

   ![Step 5 - Regenerate Token](png/CobbBrandonGraham_reset_030824.png)

### 6. Add Your Bot to a Server

1. Go to the **"OAuth2"** tab on the left-hand menu.
2. In the **"OAuth2 URL Generator"** section, select **"bot"** under **"SCOPES"**.
3. Under **"BOT PERMISSIONS"**, select the permissions your bot needs.
4. Copy the generated URL and paste it into your browser.
5. Follow the instructions to invite your bot to a server you have administrative rights to.

   ![Step 6 - Invite Bot](png/CobbBrandonGraham_authorize_030824.png)

## Example

Here's a quick example of how you might use your bot token in a Python script with the `discord.py` library:

```python
import discord

intents = discord.Intents.default()
intents.message_content = True
client = discord.Client(intents=intents)

@client.event
async def on_ready():
    print(f'We have logged in as {client.user}')

@client.event
async def on_message(message):
    if message.author == client.user:
        return

    if message.content.startswith('$hello'):
        await message.channel.send('Hello!')

# Replace 'YOUR_BOT_TOKEN' with your actual bot token
client.run('YOUR_BOT_TOKEN')
```

Replace `'YOUR_BOT_TOKEN'` with the token you copied earlier.

## Conclusion

You now have a Discord bot token and have learned how to use it to set up and run your Discord bot. Make sure to keep your token secure and only share it with trusted individuals.

For more information and documentation, visit the [Discord Developer Portal Documentation](https://discord.com/developers/docs/intro).

---
