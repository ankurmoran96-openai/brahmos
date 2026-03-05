# ⚡ BrahMos Core (God Mode AI CLI)

BrahMos is an autonomous, terminal-based AI orchestrator capable of reading, writing, planning, and executing complex software engineering tasks directly on your machine.

## ✨ Features
* **Modern Rich UI**: Fully animated terminal interface with Markdown parsing and syntax highlighting.
* **Autonomous Workspace**: Automatically creates and safely isolates all generated code into a local `Workspace` directory.
* **Interactive Architect Mode**: Uses GPT-4o to brainstorm and map out project blueprints before executing them.
* **Dynamic Navigation**: Move the AI seamlessly through your file system using `/cd path/to/folder`.
* **Sub-Shell Drop-in**: Use the `/shell` command to instantly drop into an interactive terminal in your active workspace without breaking context.
* **Auto-dependency Resolution**: Never worry about missing packages; the system installs what it needs dynamically.

## 🚀 Installation

You can install BrahMos directly via `pip`. This will automatically download the code, install dependencies, and register the global `brahmos` command.

```bash
# Clone the repository
git clone https://github.com/YourUsername/BrahMos.git

# Enter directory
cd BrahMos

# Install the package globally
pip install -e .
```

## 🔑 Setup

BrahMos requires an API key to function.

1. Create a `.env` file in the directory where you plan to run BrahMos (or copy the example).
```bash
cp .env.example .env
```
2. Open the `.env` file and paste your API key:
```env
BRAHMOS_API_KEY="your_api_key_here"
```

## 💻 Usage

Once installed, you can launch the AI from anywhere in your terminal by simply typing:

```bash
brahmos
```

### Commands
* `/cd <path>` - Change the directory the AI is actively working in.
* `/shell` - Drop into an interactive terminal inside the current working directory.
* `clear` - Clear the terminal screen.
* `exit` or `quit` - Shutdown BrahMos.

## 🛡️ Architecture & Safety
By default, the AI is sandboxed into a `./Workspace` directory that is created wherever you run the `brahmos` command. It will write files, start servers, and execute code within this directory unless you explicitly tell it to navigate elsewhere using the `/cd` command.
