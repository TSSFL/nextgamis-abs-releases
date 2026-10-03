# NEXTGAMIS ABS — Releases

Installation packages for **NEXTGAMIS ABS**, the offline-first agency banking
terminal from [TSSFL Technology Stack Team](https://www.tssfl.com).

**This repository holds releases only — no source code.**

---

## Download

Take the newest entry from **[Releases](../../releases/latest)**.

### Either — click to download

| File | For |
|------|-----|
| `NEXTGAMIS_ABS_<version>_Windows_x64.zip` | Windows, **64-bit** |
| `NEXTGAMIS_ABS_<version>_Linux_x64.tar.gz` | Linux |
| `SHA256SUMS.txt` | to check the two above |

### Or — from a terminal

Useful on a server, or when a browser download keeps breaking: these resume.

```bash
# Linux
curl -LO https://github.com/TSSFL/nextgamis-abs-releases/releases/latest/download/NEXTGAMIS_ABS_1.0.0_Linux_x64.tar.gz
curl -LO https://github.com/TSSFL/nextgamis-abs-releases/releases/latest/download/SHA256SUMS.txt
sha256sum -c SHA256SUMS.txt --ignore-missing
```

```powershell
# Windows PowerShell
curl.exe -LO https://github.com/TSSFL/nextgamis-abs-releases/releases/latest/download/NEXTGAMIS_ABS_1.0.0_Windows_x64.zip
```

With the GitHub CLI, which resumes and verifies for you:

```bash
gh release download --repo TSSFL/nextgamis-abs-releases --pattern "*Linux*"
```

---

## Which systems this runs on

### Windows

| | |
|---|---|
| **Supported** | Windows 10 and Windows 11, **64-bit only** |
| **Tested on** | Windows 10 Pro, Windows 11 |
| **Not supported** | Any 32-bit Windows; Windows 8.1 and earlier |

⚠️ **64-bit is not a preference, it is a requirement.** Check **Settings →
System → About → System type**. On a 32-bit installation the installer finishes
and reports success, creates no working shortcut, and the application never
starts. A 32-bit build does not exist and cannot be made: one of the libraries
the system depends on publishes no 32-bit packages at all.

### Linux

Needs **glibc 2.29 or newer**, 64-bit.

**The one command that settles it**, whatever distribution you run:

```bash
ldd --version | head -1
```

If the number is **2.29 or higher**, the system runs. The list below is a guide,
not the rule — distributions move.

| Distribution | |
|---|---|
| Ubuntu 20.04 LTS and newer | yes — 22.04 and 23.04 tested |
| Debian 11 and newer | yes |
| Linux Mint 20 and newer | yes |
| Kali Linux (2020 onward) | yes — it tracks Debian testing |
| Fedora 30 and newer | yes |
| RHEL, Rocky, AlmaLinux 9 and newer | yes |
| openSUSE Leap 15.3 and newer, Tumbleweed | yes |
| SUSE Linux Enterprise 15 SP3 and newer | yes |
| Debian 10, RHEL/Rocky 8 | **no** — glibc 2.28 |
| openSUSE Leap 15.2 and earlier, SLES 12 | **no** — glibc 2.26 and older |

Nothing here is tied to a package manager: the installer calls no `apt`, `dnf`,
`zypper` or `pacman`, and installs nothing from the network. It needs `chattr`,
which every Linux has, and works on ext4, btrfs and XFS.

Everything the application needs travels with it — fonts and graphics
libraries included. **No internet connection and no extra packages are needed
to install it**, and none are needed to run it.

---

## Install

**Windows** — unzip, then right-click `install.bat` and choose
**Run as administrator**.

**Linux**

```bash
tar xzf NEXTGAMIS_ABS_<version>_Linux_x64.tar.gz
cd abs_dist_linux
sudo bash install.sh
```

Windows will ask *"Do you want to allow this app to make changes to your
device?"* — that is Windows asking permission to write to `Program Files`, and
every installer does it. Choose **Yes**.

---

## Licence

NEXTGAMIS ABS runs on a licence issued for **one machine**. On first start the
application shows your **Machine ID** — a long code in a box on screen.

### What to send us

Send these five things to **sales@tssfl.co**, or on WhatsApp to
**+255 762 896 544**:

| | Example |
|---|---|
| **Machine ID** | the long code shown on screen — copy it exactly |
| **Business name** | `WAKALA BORA` — this is printed on every report you generate |
| **Email address** | where the licence and your reports go |
| **Machine type** | `laptop`, `desktop`, or the model, e.g. `HP 250 G8` |
| **Operating system** | `Windows 11`, `Windows 10`, `Ubuntu 22.04` |

⚠️ **The business name becomes part of your licence** and appears on every
report, so send it exactly as you want it to read. Changing it later means a
new licence.

⚠️ **One licence covers one machine.** If you run the system on two computers,
send the Machine ID of each — they are different codes.

### Finding the Machine ID again

Whatever is wrong with a licence — missing, expired, damaged, or issued for a
different machine — **the screen you see shows your Machine ID**. You never
have to go looking for it.

If the application is running normally, it is also under
**System Utilities → 4 · License Info**.

### Installing the licence we send you

**Windows**
```
powershell -ExecutionPolicy Bypass -File "C:\Program Files\NEXTGAMIS ABS\update-license.ps1" -Licence C:\path\to\your.lic
```

**Linux**
```bash
sudo /opt/nextgamis-abs/update-license.sh /path/to/your.lic
```

Renewing later uses the same command with the new file.

---

## Upgrading

Install the new version over the old one the same way. **Your data, licence and
settings are kept** — the installer never touches them.

---

## Contact

| | |
|---|---|
| Sales and licences | **sales@tssfl.co** |
| Support | **support@tssfl.co** |
| Phone, WhatsApp, SMS | **+255 762 896 544** |
| | [www.tssfl.com](https://www.tssfl.com) · [www.tssfl.co](https://www.tssfl.co) |

© 2026 TSSFL Technology Stack Team — mifumo ya kidijitali tangu 2012
