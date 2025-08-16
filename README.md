# Install-Zsh-Powerlevel10k-and-Awesome-Plugins-on-Linux

---

# 🚀 How to Install Zsh, Powerlevel10k, and Awesome Plugins on Linux

If you're bored with the default terminal and want something more **aesthetic, interactive, and productive**, then **Zsh + Powerlevel10k** is the perfect combo for you.

This guide works on most Linux distros like Arch, Fedora, Ubuntu, and others.

---

## 🛠️ 1. Install Zsh

### Ubuntu / Debian

```bash
sudo apt update
sudo apt install zsh -y
```

### Arch Linux / Manjaro

```bash
sudo pacman -S zsh
```

### Fedora

```bash
sudo dnf install zsh
```

---

## ⚙️ 2. Set Zsh as the Default Shell

```bash
chsh -s $(which zsh)
```

Then log out and back in to apply the changes.

---

## 🧪 3. Install Oh My Zsh

Oh My Zsh is a popular framework that makes managing Zsh configurations easier.

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

---

## 🎨 4. Install Powerlevel10k Theme

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
```

Then edit your `~/.zshrc` file and set the theme:

```bash
ZSH_THEME="powerlevel10k/powerlevel10k"
```

Reload Zsh:

```bash
source ~/.zshrc
```

You’ll be prompted to configure Powerlevel10k. Just follow the wizard!

---

## 🔌 5. Install Useful Zsh Plugins

### 📘 5.1 Autosuggestions

Suggests previously used commands as you type:

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

### ✨ 5.2 Syntax Highlighting

Highlights commands with color for easier reading:

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```

### ⚡ 5.3 Fast Syntax Highlighting (Faster Alternative)

```bash
git clone https://github.com/zdharma-continuum/fast-syntax-highlighting.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/fast-syntax-highlighting
```

> ⚠️ **Use only one:** either `zsh-syntax-highlighting` or `fast-syntax-highlighting`, not both.

### 🔍 5.4 Autocomplete

A smart and fast autocomplete plugin:

```bash
git clone --depth 1 -- https://github.com/marlonrichert/zsh-autocomplete.git $ZSH_CUSTOM/plugins/zsh-autocomplete
```

---

## 🔧 6. Enable Plugins in `.zshrc`

Open `~/.zshrc` and edit the plugin section. Example:

```bash
plugins=(
  git
  zsh-autosuggestions
  fast-syntax-highlighting
  zsh-autocomplete
)
```

> Replace `fast-syntax-highlighting` with `zsh-syntax-highlighting` if you use that instead.

---

## 🔄 7. Reload Zsh Configuration

```bash
source ~/.zshrc
```

---

## 🏁 Done!

Now your terminal is not only prettier, but also smarter and more helpful. Enjoy your new Zsh setup! 😎
