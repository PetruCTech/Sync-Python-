# idat-sync

[![Build Windows](https://img.shields.io/github/actions/workflow/status/tony-97/idat-sync/build_and_deploy.yml?label=Windows&logo=windows&logoColor=white)](https://github.com/tony-97/idat-sync/actions/workflows/build_and_deploy.yml)
[![Build Linux](https://img.shields.io/github/actions/workflow/status/tony-97/idat-sync/build_and_deploy.yml?label=Linux&logo=linux&logoColor=white)](https://github.com/tony-97/idat-sync/actions/workflows/build_and_deploy.yml)
[![Build macOS](https://img.shields.io/github/actions/workflow/status/tony-97/idat-sync/build_and_deploy.yml?label=macOS&logo=apple&logoColor=white)](https://github.com/tony-97/idat-sync/actions/workflows/build_and_deploy.yml)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/tony-97/idat-sync/blob/main/colab.ipynb)

[![Latest Release](https://img.shields.io/github/v/release/tony-97/idat-sync?label=Release&logo=github)](https://github.com/tony-97/idat-sync/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/tony-97/idat-sync/total?label=Downloads&logo=github)](https://github.com/tony-97/idat-sync/releases)
[![License: MIT](https://img.shields.io/github/license/tony-97/idat-sync?label=License)](LICENSE)
[![Python 3.10+](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)](https://www.python.org/)

idat-sync automates the download and organization of your course materials (Moodle, SharePoint/OneDrive) and lecture recordings. It's designed to eliminate the tedious task of opening numerous links, manually creating folders, and wasting time searching for scattered files.

## What are you doing?

- Automatically downloads and organizes files by course and module.

- Downloads video recordings (while they are still accessible) and saves them within the course structure.

- Simple graphical interface for selecting the synchronization folder and viewing progress.

## Download

Download the latest version from [GitHub Releases](https://github.com/tony-97/idat-sync/releases/latest):

| Operating System | File | Notes |

| ----------------- | -------------------------------------------------------------------------------------------------------------- | ---------------------------------------------- |

**Windows** | [`idat_sync-Windows.exe`](https://github.com/tony-97/idat-sync/releases/latest/download/idat_sync-Windows.exe) | Portable executable, no installation required |

**Linux** | [`idat_sync-Linux`](https://github.com/tony-97/idat-sync/releases/latest/download/idat_sync-Linux) | Grant execute permissions before use |

**macOS** | [`idat_sync-macOS.dmg`](https://github.com/tony-97/idat-sync/releases/latest/download/idat_sync-macOS.dmg) | Unsigned application, see instructions below |

### macOS (unsigned application)

Because it's an unsigned application, macOS will block its execution by default. Follow these steps:

1. **Mount the DMG** by double-clicking `idat_sync-macOS.dmg` and dragging the app to the **Applications** folder.

2. **Remove the quarantine attribute** by opening Terminal and running:

``shell

xattr -cr /Applications/idat_sync.app

``

3. **Open the application** normally from Applications.

## Installation (from source code)

1. **Requirements**

> - Python 3.10+

> - ffmpeg (https://www.ffmpeg.org/)

2. **Install the package:**
```shell
pip install git+https://github.com/tony-97/idat-sync
```
3. **Install the browser for Playwright (Linux/macOS only):**

- For Linux:
```shell
playwright install chromium
```

- For macOS:
```shell
playwright install webkit
```

## How to use

1. Once installed, simply run the following command in your terminal to open the application:
```shell
idat_sync
```
2. In the window:

- Enter your student ID and password.

![Login](screenshots/login.png)

- Complete two-factor authentication (2FA) with the code received on your mobile device.

![2FA](screenshots/mfa.png)

- Once the main window loads, select the destination folder for your files.

- Click the **"Sync"** button to start the process. You will be able to see the progress in the same window.

![Progress](screenshots/sync_progress.png)

3. The files will be downloaded and organized in the folder you selected.

## Google Colab + Google Drive + NotebookLM

If you don't want to install anything locally, you can run **idat-sync** directly from Google Colab. The notebook [`colab.ipynb`](colab.ipynb) syncs your course materials to your Google Drive and generates links ready to import into [NotebookLM](https://notebooklm.google.com/).

### What's Included?

| Functionality | Description
