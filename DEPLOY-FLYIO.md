
## Prerequisites

- A [Fly.io](https://fly.io) account
- [Fly.io's CLI is installed on your machine](https://fly.io/docs/flyctl/)
- [Prerequisites in the repository](https://github.com/n3d1117/chatgpt-telegram-bot#prerequisites)
    - An OpenAI account and [API key](https://help.openai.com/en/articles/4936850-where-do-i-find-my-secret-api-key) (note: this is pay as you go).
    - Telegram, a Telegram bot, and its token.
    - Python 3.10 and pipenv (optional, only if you want to edit the bot locally)

## Guide

1. Optional: Fork the [`n3d1117/chatgpt-telegram-bot`](https://github.com/n3d1117/chatgpt-telegram-bot) repository.
2. Clone the repository using Git to a local folder:
    ```bash
    $ git clone https://github.com/n3d1117/chatgpt-telegram-bot.git
    $ cd chatgpt-telegram-bot
    ```
3. Configure the [Telegram bot's settings](https://github.com/n3d1117/chatgpt-telegram-bot#configuration) as pointed out in the repository.
4. Once you're satisfied with the settings, launch a Fly.io app with the command:
    ```bash
    $ flyctl launch
    ```
5. Configure the settings for the Fly.io app with prompts asked by the CLI, for example in the [Fly.io Dockerfile guide](https://fly.io/docs/languages-and-frameworks/dockerfile/):
    ```bash
    ? App Name (leave blank to use an auto-generated name): telechatgpt
    ? Select organization: Your Name Here (personal)
    ? Select region: lax (Los Angeles, California (US))
    Created app telechatgpt in organization personal
    Wrote config file fly.toml
    ? Would you like to deploy now? (y/N) y
    
    ```
6. Wait until the app has finished deploying by checking out the monitoring.
7. Once done, you can start chatting by sending `/start` to your bot in Telegram which you configured in step 3.
