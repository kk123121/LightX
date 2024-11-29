# LightX -  Utility Module

**LightX** is a versatile  utility module designed to simplify terminal color output, bot creation, and system-related tasks. It combines terminal text formatting, web requests, random sleep intervals, system command execution, and a simplified Discord bot interface all in one place.

This module is designed with both simplicity and flexibility in mind, making it ideal for developers looking to streamline common tasks like logging, bot development, and working with APIs.

---

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
  - [Terminal Colors](#terminal-colors)
  - [Fetch JSON Data](#fetch-json-data)
  - [Random Sleep](#random-sleep)
  - [Run System Commands](#run-system-commands)
  - [Discord Bot Setup](#discord-bot-setup)
- [Example Usage](#example-usage)
- [License](#license)
- [Contributing](#contributing)
- [Contact](#contact)

---

## Features
- **Terminal Colors:** Easily format terminal text with vibrant colors and styling.
- **Discord Bot:** A simple framework for creating Discord bots with ease. Handle commands and interact with users.
- **Utility Functions:** Fetch JSON data, execute system commands, and perform other useful tasks.
- **Command Registration:** Simple decorator for registering Discord bot commands.

---

## Installation

### Clone the Repository

To install **LightX** manually, clone the repository from GitHub:

```
git clone https://github.com/kk123121/LightX.git
cd LightX
Install via  Package
If you'd prefer to install LightX as a  package, ensure you have the setup.py file included in the repository and run the following command:



pip install .
Alternatively, you can install LightX directly from GitHub:



pip install git+https://github.com/kk123121/LightX.git
Usage
Import the Module
To use LightX in your project, import the module like this:



import LightX
Terminal Colors
Print colorful text in the terminal using built-in color constants. Here's how to use it:



print(LightX.colored_text("This is a red message!", "RED"))
print(LightX.colored_text("This is a green message!", "GREEN"))
Available Colors:
RED
GREEN
YELLOW
BLUE
MAGENTA
CYAN
WHITE
You can also use LightX's colored_text function with additional formatting like bold and underline.

Fetch JSON Data
LightX provides a simple function for fetching and parsing JSON data from any given URL:



data = LightX.fetch_json("https://api.github.com")
print(LightX.colored_text("Fetched Data:", "CYAN"), data)
This function returns the parsed JSON data, which you can then use as needed.

Random Sleep
Add a random sleep interval to your program, which can be useful for things like rate-limiting or simulating delays in bots:



LightX.random_sleep(2, 5)  # Sleeps for a random time between 2 and 5 seconds
Run System Commands
Execute any system command directly from . LightX will capture the output and return it:



output = LightX.run_command("ls")
print(LightX.colored_text(f"Command Output: {output}", "YELLOW"))
This can be particularly useful for system-level scripts or debugging.

Discord Bot Setup
Initialize the Bot
LightX includes a simple way to create and run a Discord bot. Begin by initializing the bot with a custom command prefix:



LightX.initialize_bot(command_prefix="!")
Create Commands
Define bot commands using the LightX.command() decorator. These commands will be registered automatically and can be triggered by users:



@LightX.command()
async def hello(ctx):
    """Send a simple greeting."""
    await ctx.send("Hello from LightX!")
Run the Bot
Finally, run the bot using your Discord bot token:



LightX._bot.run("YOUR_DISCORD_BOT_TOKEN")
This will start the bot and make it responsive to commands.

Example Usage
Here’s an example script that demonstrates how to use the key features of LightX:



import LightX

# Initialize the bot with a custom prefix
LightX.initialize_bot(command_prefix="!")

# Register a simple command that replies with "Pong!"
@LightX.command()
async def ping(ctx):
    """Responds with 'Pong!' when a user types !ping"""
    await ctx.send("Pong!")

# Fetch JSON data from an API
data = LightX.fetch_json("https://api.github.com")
print(LightX.colored_text("Fetched Data:", "CYAN"), data)

# Run a system command
output = LightX.run_command("ls")
print(LightX.colored_text(f"Command Output: {output}", "MAGENTA"))

# Sleep for a random duration between 1 and 3 seconds
LightX.random_sleep(1, 3)

# Run the bot
LightX._bot.run("YOUR_DISCORD_BOT_TOKEN")
License
LightX is licensed under the MIT License. See the LICENSE file for more details.

Contributing
We welcome contributions to LightX! If you have a feature or fix you'd like to contribute, follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature-name).
Commit your changes (git commit -am 'Add new feature').
Push to the branch (git push origin feature-name).
Create a new pull request.
If you're unsure where to start, feel free to open an issue, and we can help guide you.

Contact
If you have any questions, suggestions, or feedback about LightX, feel free to reach out:

Email: kaidenjclafli@gmail.com
Discord: mrnuggetthe1st#0001
GitHub: https://github.com/kk123121
Thank you for using LightX! We hope it makes your development easier and more efficient. Happy coding! ✨



