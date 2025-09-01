# Amazon Q CLI - Installation & User Guide

This guide provides installation steps, troubleshooting, and uninstallation instructions for the **Amazon Q Developer CLI** across macOS, Linux, and Ubuntu systems.

📄 Reference: [AWS Documentation - Installing Amazon Q CLI](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-installing.html?b=cli&p=overview&s=tiles)


## 📌 Installation Options

Amazon Q CLI can be installed in two modalities:

- **Minimal Installation**  
  Provides only the required binaries (`q` and `qterm`) for Amazon Q chat and autocomplete over SSH.  
  Useful if you want just the CLI without the full desktop integration.

- **Full Distribution**  
  Includes the desktop application, shell integrations, and autocomplete support for 500+ CLI tools.

---

## 🍏 macOS Installation

You can install Amazon Q for command line on macOS either by downloading the application directly or using **Homebrew**.

### Steps:

1. **Download Amazon Q for macOS**
   - Download the `.dmg` file from the official AWS release page.
2. **(Optional) Verify the download**.
3. **Install the application**
   - Double-click the `.dmg` file and drag the app into the **Applications** folder.
4. **Launch Amazon Q**
   - Open **Amazon Q** from Applications.
5. **Enable shell integrations**
   - Run Amazon Q from the shell with autocomplete enabled.
6. **Authenticate**
   - Use **Builder ID** or **IAM Identity Center** (via your account’s start URL).
7. **Grant permissions**
   - Follow prompts to install shell integrations and grant macOS accessibility permissions.

---

## 🐧 Linux Installation

### Using AppImage (GUI required)

1. Download the AppImage file.  
2. Make it executable:
   ```bash
   chmod +x amazon-q.appimage
    ```

3. Run it:

   ```bash
   ./amazon-q.appimage
   ```
4. Authenticate with **Builder ID** or **IAM Identity Center**.

⚠️ If installing on Linux **without GUI**, use the [zip file installation method](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-installing.html).

---

## 🟠 Ubuntu Installation

### Using `.deb` package (GUI required)

1. Download the package:

   ```bash
   wget https://desktop-release.q.us-east-1.amazonaws.com/latest/amazon-q.deb
   ```
2. Install it:

   ```bash
   sudo dpkg -i amazon-q.deb
   sudo apt-get install -f
   ```
3. Launch Amazon Q:

   ```bash
   q
   ```
4. Authenticate with **Builder ID** or **IAM Identity Center**.

---

## 🍺 Installation via Homebrew (macOS)

If you prefer Homebrew:

```bash
brew install --cask amazon-q
```

---

## 🗑️ Uninstallation

### On macOS

1. Open **Applications** folder in Finder.
2. Locate **Amazon Q Developer**.
3. Drag it to Trash or right-click → **Move to Trash**.
4. Empty Trash to finish.

### On Ubuntu

```bash
sudo apt-get remove amazon-q
sudo apt-get purge amazon-q
```

---

## 🔧 Debugging & Troubleshooting

### Health Check

Run:

```bash
q doctor
```

Expected output:

```
✔ Everything looks good!
```

If not, follow prompts to resolve issues.

### Common Issues

* **Authentication failures**
  Run:

  ```bash
  q login
  ```

* **Autocomplete not working**
  Ensure shell integration is installed:

  ```bash
  q doctor
  ```

* **SSH integration issues**
  Check SSH server configuration for required environment variables.

---

## 🚑 Troubleshooting Steps

1. Run `q doctor` to diagnose.
2. Check internet connection.
3. Verify environment compatibility (see supported environments).
4. Reinstall Amazon Q if needed.
5. Report issues:

   ```bash
   q issue
   ```
