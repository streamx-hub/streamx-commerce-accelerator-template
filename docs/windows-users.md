## Windows Specifics

In the case of Windows, all the commands outlined in this file should be run inside the Linux VM terminal, which hosts Docker, rather than in native Windows terminals (e.g., CMD or PowerShell). For instance, if Docker is used with WSL, the commands should be executed inside the WSL terminal.

To launch WSL: Press `Win + R`, type `wsl`, and hit `Enter`.

### Git Repository Checkout

WSL commands run in the linux context.
Therefore, you must check out / git clone this repository via the WSL terminal
to prevent Git from automatically converting newlines in bash scripts (`\n`) to Windows-style newlines (`\r\n`),
which could cause unexpected errors while parsing and running the scripts.

### Install Homebrew and java inside WSL

#### Install curl:
```bash
  sudo apt update
  sudo apt install -y build-essential curl file git
```

#### Install Homebrew:
```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Add brew to your shell
```bash
  echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"' >> ~/.bashrc
  eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
```

Restart your WSL shell or run:
```bash
  source ~/.bashrc
```

Verify:
```bash
  brew --version
```

#### Install java:
```bash
  brew update
  brew install openjdk@17
  brew link --force --overwrite openjdk@17
```

### Docker Resource Management

If heavy automation scripts (such as `publish-all.sh`) become unresponsive or "hang",
it typically indicates that Docker has reached the default resource ceiling allocated by Windows.

You can adjust these settings by creating or editing a global configuration file on your Windows host.

To do so, navigate to your Windows user profile folder by entering `%USERPROFILE%` in the File Explorer address bar.

Open or create a file named `.wslconfig`.
Add or update the following section:

```
[wsl2]
memory=80%
swap=4GB
```

For the changes to take effect - stop WSL using the `wsl --shutdown` command, and start `wsl` again.

---
