[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://pyrobbot.streamlit.app)

[![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)](https://github.com/paulovcmedeiros/pyRobBot)

[![Contributors Welcome](https://img.shields.io/badge/Contributors-welcome-<COLOR>.svg)](https://github.com/paulovcmedeiros/pyRobBot/pulls)
[![Linting](https://github.com/paulovcmedeiros/pyRobBot/actions/workflows/linting.yaml/badge.svg)](https://github.com/paulovcmedeiros/pyRobBot/actions/workflows/linting.yaml)
[![Tests](https://github.com/paulovcmedeiros/pyRobBot/actions/workflows/tests.yaml/badge.svg)](https://github.com/paulovcmedeiros/pyRobBot/actions/workflows/tests.yaml)
[![codecov](https://codecov.io/gh/paulovcmedeiros/pyRobBot/graph/badge.svg?token=XI8G1WH9O6)](https://codecov.io/gh/paulovcmedeiros/pyRobBot)

# pyRobBot

An interface to OpenAI's [GPT large language models (LLMs)](https://platform.openai.com/docs/models) that implements:
* A conventional chatbot that can be used either via web UI or terminal
* A personal assistant that can actually interact with you by voice

The package is written in Python. The web chatbot UI is made with [Streamlit](https://streamlit.io).

**See and try the [demo web app on Streamlit](https://pyrobbot.streamlit.app)!**

## Features
- [x] Text to speech and speech to text
  - Talk to the GPT assistant!
- [x] Web UI
  - Add/remove conversations dynamically
  - Automatic/editable conversation summary title
- [x] Fully configurable
  - Support for multiple GPT LLMs
  - Control over the parameters passed to the OpenAI API, with (hopefully) sensible defaults
  - Ability to pass base directives to the LLM
    - E.g., to make it adopt a persona, but you decide which directived to pass
  - Dynamically modifiable AI parameters in each chat separately
    - No need to restart the chat
- [x] Autosave & retrieve chat history
- [x] Chat context handling using [embeddings](https://platform.openai.com/docs/guides/embeddings)
- [x] Estimated API token usage and associated costs
- [x] OpenAI API key is **never** stored on disk



## System Requirements
- Python >= 3.9
- A valid [OpenAI API key](https://platform.openai.com/account/api-keys)
  - Set in the Web UI or through the environment variable `OPENAI_API_KEY`

## Installation
### Using pip
```shell
pip install pyrobbot
```

### From source
```shell
pip install git+https://github.com/paulovcmedeiros/pyRobBot.git
```

## Basic Usage
Upon succesfull installation, you should be able to run
```shell
rob [opts] SUBCOMMAND [subcommand_opts]
```
where `[opts]` and `[subcommand_opts]` denote optional command line arguments
that apply, respectively, to `rob` in general and to `SUBCOMMAND`
specifically.

**Please run `rob -h` for information** about the supported subcommands
and general `rob` options. For info about specific subcommands and the
options that apply to them only, **please run `rob SUBCOMMAND -h`** (note
that the `-h` goes after the subcommand in this case).

### Using the Web UI
```shell
rob
```

### Chatting by Voice
```shell
rob voice
```

### Running on the Terminal
```shell
rob .
```

## Disclaimers
This project's main purpose is to serve as a learning exercise for me (the author) and to serve as tool for and experimenting with OpenAI API and GPT LLMs. It does not aim to be the best or more robust OpenAI-powered chatbot out there.

Having said this, this project *does* aim to have a friendly user interface and to be easy to use and configure. So, please feel free to open an issue or submit a pull request if you find a bug or have a suggestion.

Last but not least: this project is **not** affiliated with OpenAI in any way.


