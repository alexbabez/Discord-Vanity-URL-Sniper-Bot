# Discord Vanity URL Sniper Bot

This Discord bot allows users to monitor the availability of a specific vanity URL on Discord. The bot continuously checks if the specified vanity URL becomes available and sends real-time notifications when it does.

## Features

- **Vanity URL Monitoring**: Monitors the availability of a specified Discord vanity URL.
- **Customizable Check Interval**: Users can set the delay between checks, allowing for personalized monitoring intervals.
- **Real-Time Notifications**: Notifies users in the Discord channel when the vanity URL is available for use.

## Requirements

- Python 3.x
- Required Libraries:
  - `discord.py` for Discord bot functionality
  - `requests` for making HTTP requests

## Setup Instructions

1. **Install Required Libraries**:
   Make sure you have `discord.py` and `requests` installed. You can install them using pip:
   ```bash
   pip install discord.py requests
   ```

2. **Configure the Bot**:
   - Replace the `token` variable in the script with your bot's token:
     ```python
     token = "YOUR_DISCORD_BOT_TOKEN"
     ```

3. **Run the Bot**:
   - Start the bot by executing the script:
     ```bash
     python main.py
     ```

## How to Use the Bot

1. **Initiate the Sniping Command**:
   - In any Discord channel where the bot has access, type the command:
     ```bash
     !snipe
     ```

2. **Enter the Vanity URL**:
   - The bot will prompt you to enter the desired vanity URL. For example:
     ```bash
     myvanityurl
     ```

3. **Set the Check Delay**:
   - Next, the bot will ask how many seconds to wait between checks. Enter a number (e.g., `10`).

4. **Monitoring Process**:
   - The bot will continuously check the specified vanity URL and will notify you if it becomes available:
     ```bash
     Vanity URL is Available myvanityurl!
     ```

## Notes

- **Format for Vanity URL**: Only enter the part after `discord.gg/` (e.g., if the URL is `https://discord.gg/myvanityurl`, just enter `myvanityurl`).
- **Check Delay**: It’s advisable to choose a delay that is reasonable to avoid hitting Discord’s API rate limits. A delay between 5 to 30 seconds is recommended.
- **Stopping the Sniping Process**: The monitoring will stop once the vanity URL becomes available. You can manually interrupt the bot if needed.

## Troubleshooting

- **Invalid Token**: Ensure you have provided a valid Discord bot token in the script.
- **Permission Issues**: Make sure the bot has permission to read messages and send messages in the channel where the command is used.
