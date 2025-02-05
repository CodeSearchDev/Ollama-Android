# Ollama on Android using Termux

This guide explains how to install and run the **Ollama language model** on an Android device using **Termux**. By following this tutorial, you can leverage **LLMs (Large Language Models)** directly on your mobile device without needing a desktop environment.

## 📌 Prerequisites

Before starting, ensure you have the following:

- An Android device with sufficient storage and RAM.
- A stable internet connection.
- Basic familiarity with Termux commands.

## 🚀 Installation Steps

### Step 1: Install F-Droid

F-Droid is an open-source app store for Android. Download and install it from:  
🔗 [https://f-droid.org/](https://f-droid.org/)

### Step 2: Install Termux

1. Open **F-Droid**.
2. Search for **Termux** and install it.

### Step 3: Update and Upgrade Termux Packages

Open Termux and run the following command:

```bash
pkg update && pkg upgrade
```

### Step 4: Install Proot-Distro

Proot-Distro allows you to run Linux distributions inside Termux. Install it with:

```bash
pkg install proot-distro
```

Now, install **Debian**:

```bash
pd install debian
```

### Step 5: Log in to Debian

Start your Debian environment:

```bash
pd login debian
```

### Step 6: Install Tmux

Tmux allows you to run multiple terminal sessions. Install it with:

```bash
apt update && apt upgrade
apt install tmux
```

### Step 7: Install Ollama

Download and install Ollama inside Debian:

```bash
curl -fsSL https://ollama.com/install.sh | sh
```

### Step 8: Create a New Tmux Session

Start a new session for running Ollama:

```bash
tmux new -s llm
```

### Step 9: Start the Ollama Server

Inside the Tmux session, run:

```bash
ollama serve
```

### Step 10: Create a New Pane in Tmux

Split the Tmux window by pressing `Ctrl+b` and then `"`.

### Step 11: Run an Ollama Model

To run the **Gemma 2B** model:

```bash
ollama run gemma:2b
```

To run the **Phi-3** model:

```bash
ollama run phi3
```

### Step 12: Test the Model

Interact with the model by entering prompts directly in the terminal.


## 🎯 Conclusion

With this setup, you can now run **Ollama** on your Android device, unlocking the potential of **on-device AI** for development and experimentation.

## 📜 License

This project is licensed under the **MIT License**.

## 👨‍💻 Contributions & Issues

Feel free to contribute or report issues in the repository. Your feedback and contributions are highly appreciated.

Enjoy exploring the capabilities of **on-device AI** with Ollama on your Android device. 🚀