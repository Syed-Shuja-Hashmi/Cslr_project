# CSLR_project
# OSINT Virtual Machine -- Debian 13 (AwesomeWM + Oh-My-Zsh)

This repository contains the full source code, installer, documentation,
and environment configuration for a **custom Debian 13 OSINT machine**
built with:

-   **AwesomeWM (window manager)**
-   **Oh-My-Zsh (Zsh framework)**
-   **Custom OSINT tools installer**
-   **Hardened Firefox ESR**
-   **Full CLI/GUI toolset for OSINT investigations**

------------------------------------------------------------------------

# 🖥️ Desktop Environment Setup

This OSINT VM uses a lightweight and highly customizable environment
based on **AwesomeWM** and **Oh-My-Zsh**.

Below are the exact installation steps.

------------------------------------------------------------------------

## 🚀 Install AwesomeWM (Debian 13)

Run:

    sudo apt update
    sudo apt install -y awesome awesome-extra

Enable it in your display manager (LightDM/GDM/Slim):

    sudo systemctl restart lightdm

If you use `.xinitrc`:

    echo "exec awesome" > ~/.xinitrc
    startx

------------------------------------------------------------------------

## 🎨 Recommended AwesomeWM Addons

Install common utilities:

    sudo apt install -y rofi feh picom xterm lxappearance

Optional themes directory:

    mkdir -p ~/.config/awesome/themes

Reload Awesome:

    super + ctrl + r

------------------------------------------------------------------------

# 💻 Install Oh-My-Zsh

Install Zsh:

    sudo apt install -y zsh

Make Zsh your default shell:

    chsh -s /usr/bin/zsh

Log out & log back in.

------------------------------------------------------------------------

## ⚡ Install Oh-My-Zsh

Run:

    sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

------------------------------------------------------------------------

## 🔌 Recommended Oh-My-Zsh Plugins

Edit `~/.zshrc`:

    plugins=(
      git
      z
      fzf
      colored-man-pages
      sudo
    )

Reload:

    source ~/.zshrc

------------------------------------------------------------------------

# 🧰 OSINT Tooling (Installed via Script)

Tools installed automatically:

-   **Sherlock**
-   **Shodan CLI**
-   **PhoneInfoga**
-   **SpiderFoot (venv)**
-   **sn0int**
-   **Metagoofil**
-   **Sublist3r**
-   **Tor + Tor Browser Launcher**
-   **Exiftool**
-   **Steghide / Stegseek**
-   **translate-shell**
-   **Hardened Firefox ESR**
-   **Custom updater (CLI + desktop launcher)**

------------------------------------------------------------------------

# 📁 Repository Structure

    setup/
       osint-install.sh
    scripts/
    examples/
       sample_targets.txt
       sample_output/
    config/
       api_keys.example
    legal/
       ETHICS.md
       LEGAL_COMPLIANCE.md
    README.md
    LICENSE

------------------------------------------------------------------------

# 🛠 Installation

    chmod +x setup/osint-install.sh
    sudo ./setup/osint-install.sh

To validate only:

    sudo ./setup/osint-install.sh --validate-only

------------------------------------------------------------------------

# ▶️ Usage Examples

### Shodan CLI

    shodan init YOUR_API_KEY
    shodan host 1.1.1.1

### Sherlock

    sherlock username

### PhoneInfoga

    phoneinfoga scan -n "+12025550142"

### SpiderFoot

    spiderfoot -l 127.0.0.1:5001

------------------------------------------------------------------------

# 🧪 Example Dataset

    example.com
    github.com
    wikipedia.org

------------------------------------------------------------------------

# ♻️ Reproducing Results

1.  Install VM using the script\
2.  Add targets to `examples/sample_targets.txt`\
3.  Run OSINT tools\
4.  Export results into `examples/sample_output/`

------------------------------------------------------------------------

# ⚖️ Legal & Ethical Compliance

See:

-   `legal/ETHICS.md`
-   `legal/LEGAL_COMPLIANCE.md`

This OSINT VM only performs **legal**, **non-intrusive**,
**public-data** reconnaissance.


