# CSLR_project
# OSINT Virtual Machine -- Debian 13 (AwesomeWM + Zsh)

This repository contains the full source code, installer, and
documentation for a **custom Debian-13 based OSINT machine** using
**AwesomeWM**, **oh-my-zsh**, and a hardened privacy-focused browser
environment.

------------------------------------------------------------------------

## 📦 Included Tools

Installed by the script:

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
-   **Firefox ESR hardened with enterprise policies**
-   **Updater utility + GUI launcher**

------------------------------------------------------------------------

## 📁 Repository Structure

    setup/
       osint-install.sh     # full installer
    scripts/
       (empty – reserved for future automation)
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

## 🛠 Installation (Debian 13)

Make script executable:

    chmod +x setup/osint-install.sh

Run:

    sudo ./setup/osint-install.sh

To validate only:

    sudo ./setup/osint-install.sh --validate-only

------------------------------------------------------------------------

## ▶️ Usage After Installation

### **Run SpiderFoot UI**

    spiderfoot -l 127.0.0.1:5001

Then open Firefox → *SpiderFoot (local)* bookmark.

### **Shodan**

    shodan init YOUR_API_KEY
    shodan host 8.8.8.8

### **Sherlock**

    sherlock username

### **PhoneInfoga**

    phoneinfoga scan -n "+12025550142"

------------------------------------------------------------------------

## 🧪 Example Dataset (sample_targets.txt)

Located in:

    examples/sample_targets.txt

Content:

    example.com
    github.com
    wikipedia.org

------------------------------------------------------------------------

## ♻️ Reproduce Results

1.  Install using `osint-install.sh`
2.  Add targets to: `examples/sample_targets.txt`
3.  Run any tool:

```{=html}
<!-- -->
```
    sherlock johndoe
    shodan domain example.com
    phoneinfoga scan ...

4.  Save your outputs into:

```{=html}
<!-- -->
```
    examples/sample_output/

------------------------------------------------------------------------

## ⚖️ Legal and Ethical Standards

This OSINT machine follows strict **non-intrusive**, **legally
compliant**, and **privacy-respecting** rules.

See:

-   `legal/ETHICS.md`
-   `legal/LEGAL_COMPLIANCE.md`

------------------------------------------------------------------------

## 📝 Dependencies

All dependencies are installed automatically:

-   Python3 + pipx\
-   Go\
-   Rust (cargo)\
-   Node + npm\
-   Java (OpenJDK 11)\
-   Firefox ESR\
-   Tor

