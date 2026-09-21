# Tales from the Sprawl Discord LARP bot

Discord bots and other utilities for the Shadowrun LARP "Tales from the Sprawl".

## Setup Discord application

Go to https://discord.com/developers/applications and create a Discord application.
Note the client id and secret.

Provide the required environment variables with your tool of choice. mise-en-place or direnv is recommended.

```sh
# Example config
export DISCORD_TOKEN="client secret here"
export APPLICATION_ID="client id here"
export HOST="127.0.0.1"
export PORT="5000"

export GUILD_NAME="Matrix 1"
export GM_ROLE_NAME=gm
export MAIN_SHOP_NAME=trinity_taskbar
export FILE_LOGGING=true
```

In the Discord application dashboard, go to the oauth tab and under OAuth2 URL Generator select `applications.commands`, `bot` and `Administrator`.
`Integration Type` should be `Guild Install` then go to the url under `Generated URL` and select a server to add the bot to.

## Setup python

To start the bot, first [install uv](https://docs.astral.sh/uv/getting-started/installation/) and run `uv sync` to install the required dependencies.
Finally run `uv run talesbot` to start the bot. Make sure the environment variables are loaded before starting.