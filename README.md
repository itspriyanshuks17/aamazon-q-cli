# Amazon Q CLI – Installation & User Guide

The **Amazon Q Developer CLI** enables AI-powered chat, autocomplete, and SSH integrations directly from your terminal.  
This guide covers installation, authentication, troubleshooting, and uninstallation for **macOS, Linux, and Ubuntu**.

📖 Reference: [Official AWS Documentation](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-installing.html?b=cli&p=overview&s=tiles)

---

## Installation Options

Amazon Q CLI can be installed in two modes:

- **Minimal Installation**  
  Provides only `q` and `qterm` for Amazon Q chat and SSH autocomplete.  
  Suitable if you only need the CLI.

- **Full Distribution**  
  Includes the desktop application, shell integrations, and autocomplete for 500+ CLI tools.  
  Recommended for the complete feature set.

---

## macOS Installation

Amazon Q CLI can be installed on macOS via direct download or Homebrew.

### Direct Download
1. Download the `.dmg` file from the AWS release page.  
2. (Optional) Verify the checksum.  
3. Install → Double-click `.dmg` and drag the app into **Applications**.  
4. Launch Amazon Q from Applications.  
5. Enable shell integrations for CLI usage and autocomplete.  
6. Authenticate using either:
   - Builder ID  
   - IAM Identity Center (SSO)  
7. Grant permissions for shell integration and accessibility.

### Homebrew
```bash
brew install --cask amazon-q
```

---

## Linux Installation

### AppImage (GUI required)

```bash
chmod +x amazon-q.appimage
./amazon-q.appimage
```

Then authenticate using Builder ID or IAM Identity Center.

> For Linux systems without a GUI, use the [zip file installation method](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-installing.html).

---

## Ubuntu Installation

### Using `.deb` Package (GUI required)

```bash
wget https://desktop-release.q.us-east-1.amazonaws.com/latest/amazon-q.deb
sudo dpkg -i amazon-q.deb
sudo apt-get install -f
q
```

Authenticate using Builder ID or IAM Identity Center.

---

## Uninstallation

### macOS

1. Open the **Applications** folder.
2. Locate **Amazon Q Developer**.
3. Move it to Trash.
4. Empty Trash to complete removal.

### Ubuntu

```bash
sudo apt-get remove amazon-q
sudo apt-get purge amazon-q
```

---

## Debugging and Troubleshooting

### Run Health Check

```bash
q doctor
```

Expected output:

```
✔ Everything looks good!
```

If problems persist:

```bash
q issue
```

### Common Issues

* **Authentication failures** → Re-authenticate using `q login`.
* **Autocomplete not working** → Ensure shell integration is installed, then run `q doctor`.
* **SSH integration issues** → Verify that the SSH server supports the required environment variables.

---

## Troubleshooting Steps

1. Run `q doctor`.
2. Confirm your internet connection.
3. Check that your environment is supported.
4. Reinstall Amazon Q CLI if needed.
5. Report issues using:

   ```bash
   q issue
   ```

---

## Getting Started

Once installed, launch Amazon Q from your terminal:

```bash
q
```

You now have access to:

* AI-assisted shell commands
* Autocomplete across 500+ CLI tools
* Secure authentication with Builder ID or IAM Identity Center
