Integration of additional LLMs in this version.

For **stable** release:

- `python -m pip install gpt-engineer`

For **development**:
- `git clone https://github.com/gpt-engineer-org/gpt-engineer.git`
- `cd gpt-engineer`
- `poetry install`
- `poetry shell` to activate the virtual environment

We actively support Python 3.10 - 3.12. The last version to support python 3.8 - 3.9 was [0.2.6](https://pypi.org/project/gpt-engineer/0.2.6/).

### Setup API Key

Choose **one** of:
- Export env variable (you can add this to .bashrc so that you don't have to do it each time you start the terminal)
    - `export OPENAI_API_KEY=[your api key]`
- .env file:
    - Create a copy of `.env.template` named `.env`
    Adding an api base and allowing the use of any open source LLM including litellm which already have similar endpoint as closed src LLMs
    allowing the open source community to participate and experience fully open source projects without limitations.
- Custom model:
    - See [docs](https://gpt-engineer.readthedocs.io/en/latest/open_models.html), supports local model, azure, etc.

Check the [Windows README](./WINDOWS_README.md) for windows usage.

**Other ways to run:**
- Use Docker ([instructions](docker/README.md))
- Do everything in your browser:
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/gpt-engineer-org/gpt-engineer/codespaces)

### Create new code (default usage)
- Create an empty folder for your project anywhere on your computer
- Create a file called `prompt` (no extension) inside your new folder and fill it with instructions
- Run `gpte <project_dir>` with a relative path to your folder
  - For example: `gpte projects/my-new-project` from the gpt-engineer directory root with your new folder in `projects/`

### Improve Existing Code
- Locate a folder with code which you want to improve anywhere on your computer
- Create a file called `prompt` (no extension) inside your new folder and fill it with instructions for how you want to improve the code
- Run `gpte <project_dir> -i` with a relative path to your folder
  - For example: `gpte projects/my-old-project -i` from the gpt-engineer directory root with your folder in `projects/`

By running gpt-engineer you agree to our [terms](https://github.com/gpt-engineer-org/gpt-engineer/blob/main/TERMS_OF_USE.md).


## Relation to gptengineer.app
[gptengineer.app](https://gptengineer.app/) is a commercial project for automatic generation of web-apps.
It features a UI for non-technical users, connected to a git controlled codebase.
The gptengineer.app team is actively supporting the open source community.


## Features

### Pre Prompts
You can specify the "identity" of the AI agent by overriding the `preprompts` folder, with your own version of the `preprompts`, using the `--use-custom-preprompts` argument.

Editing the `preprompts` is how you make the agent remember things between projects.

### Vision

By default, GPT Engineer expects text input via a `prompt` file. It can also accept imagine inputs for vision capable models. This can be useful for adding UX or architecture diagrams as additional context for GPT Engineer. You can do this by specifiying an image directory with the --image_directory flag and setting a vision capable model in the second cli argument.

E.g. `gpte projects/example-vision gpt-4-vision-preview --prompt_file prompt/text --image_directory prompt/images -i`

### Open source, local and alternative models

By defaul GPT Engineer supports OpenAI Models via the OpenAI API or Azure Open AI API, and Anthropic models.

With a little extra set up you can also run with open source models, like WizardCoder. See the [documentation](https://gpt-engineer.readthedocs.io/en/latest/open_models.html) for example instructions.

## Mission

The gpt-engineer community mission is to **maintain tools that coding agent builders can use and facilitate collaboration in the open source community**.

If you are interested in contributing to this, we are interested in having you.

If you want to see our broader ambitions, check out the [roadmap](https://github.com/gpt-engineer-org/gpt-engineer/blob/main/ROADMAP.md), and join
[discord](https://discord.gg/8tcDQ89Ej2)
to get input on how you can [contribute](.github/CONTRIBUTING.md) to it.

gpt-engineer is [governed](https://github.com/gpt-engineer-org/gpt-engineer/blob/main/GOVERNANCE.md) by a board of long term contributors. If you contribute routinely and have an interest in shaping the future of gpt-engineer, you will be considered for the board.

## Example



https://github.com/gpt-engineer-org/gpt-engineer/assets/4467025/40d0a9a8-82d0-4432-9376-136df0d57c99
