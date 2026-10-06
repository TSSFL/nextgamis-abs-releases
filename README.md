# NEXTGAMIS ABS

## Download

**One click starts the download.**

### ⬇ [Download for Windows (64-bit) — 85 MB](https://github.com/TSSFL/nextgamis-abs-releases/releases/latest/download/NEXTGAMIS_ABS_1.0.0_Windows_x64.zip)
### ⬇ [Download for Linux — 96 MB](https://github.com/TSSFL/nextgamis-abs-releases/releases/latest/download/NEXTGAMIS_ABS_1.0.0_Linux_x64.tar.gz)

### 🇹🇿 [Maelekezo kwa Kiswahili — bonyeza hapa](SETUP_SWAHILI.md)

---

This repository holds releases only — no source code. Packages for
**NEXTGAMIS ABS**, the offline-first agency banking terminal from
[TSSFL Technology Stack Team](https://www.tssfl.com).

### Also

- [SHA256SUMS.txt](https://github.com/TSSFL/nextgamis-abs-releases/releases/latest/download/SHA256SUMS.txt) — to check a download that may have broken
- [All releases](../../releases) — older versions and release notes

⚠️ The download links carry the version in the filename, so they work while
**1.0.0** is newest. After a newer release, take the files from
[Releases](../../releases/latest).

⚠️ A GitHub release also lists **"Source code (zip)"** and **"Source code
(tar.gz)"** at the bottom. GitHub adds those to every release automatically,
whatever the repository holds — here they are an 8 KB copy of these
instructions, not the application. Ignore them.

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
cd $HOME\Downloads
curl.exe -LO https://github.com/TSSFL/nextgamis-abs-releases/releases/latest/download/NEXTGAMIS_ABS_1.0.0_Windows_x64.zip
curl.exe -LO https://github.com/TSSFL/nextgamis-abs-releases/releases/latest/download/SHA256SUMS.txt

$file = "NEXTGAMIS_ABS_1.0.0_Windows_x64.zip"
$want = ((Select-String -Path SHA256SUMS.txt -Pattern ([regex]::Escape($file))).Line -split '\s+')[0]
$got  = (Get-FileHash $file -Algorithm SHA256).Hash
if ($got -eq $want.ToUpper()) { "$file : OK" } else { "$file : FAILED - download again" }
```

Then extract and install:

```powershell
Expand-Archive NEXTGAMIS_ABS_1.0.0_Windows_x64.zip -DestinationPath abs_release
Start-Process -Verb RunAs .\abs_release\abs_windows\install.bat
```

`-Verb RunAs` is *Run as administrator*. Answer **Yes** at User Account Control.

⚠️ It is normal for a computer to show a security warning for a file downloaded
from the internet. It is not a sign that anything is wrong with the software.

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

---

## 🤝 Rather not download it yourself?

**If you are in Dar es Salaam we can install it for you, or you can collect it
from us on a flash drive — no download, no data bundle.**

We can also walk you through the installation by **phone, Google Meet or
Zoom** — wherever you are.

| | |
|---|---|
| **Call, SMS or WhatsApp** | **+255 762 896 544** |
| **Email** | [sales@tssfl.co](mailto:sales@tssfl.co) |

Come with the computer you want it installed on, or tell us where you are. We
will set it up, install your licence and show you how to make your first entry.

---

## Install

Each package unpacks into **one folder**, and everything happens inside it.

| Package | Unpacks to |
|---|---|
| `NEXTGAMIS_ABS_<version>_Windows_x64.zip` | **`abs_windows\`** |
| `NEXTGAMIS_ABS_<version>_Linux_x64.tar.gz` | **`abs_dist_linux/`** |

**Windows**

1. Right-click the ZIP → **Extract All**
2. Open the folders until you see **`install.bat`** — it is inside
   `abs_windows\`. Windows adds a folder named after the ZIP as well, so the
   full path is usually
   `NEXTGAMIS_ABS_1.0.0_Windows_x64\abs_windows\`
3. Right-click **`install.bat`** → **Run as administrator**
4. **Open File - Security Warning** — *"The publisher could not be verified"* →
   **Run**
5. **User Account Control** — *"Do you want to allow this app to make changes to
   your device?"* → **Yes**

⚠️ **Both of those are expected, on a fresh install and on an upgrade.** The
first appears because the file came from the internet and does not carry a
code-signing certificate; the second is Windows asking permission to write to
`Program Files`, which every installer needs. Neither says anything is wrong
with the software.

⚠️ **In the User Account Control box, `No` is the highlighted button.** Pressing
Enter cancels the installation — click **Yes**.

⚠️ The number of folders depends on how you extracted, not on the package.
**Go by `install.bat`, not by the folder names** — wherever that file is, that
is the folder you want.

**Linux**

```bash
tar xzf NEXTGAMIS_ABS_<version>_Linux_x64.tar.gz
cd abs_dist_linux
sudo bash install.sh
```

Windows will ask *"Do you want to allow this app to make changes to your
device?"* — that is Windows asking permission to write to `Program Files`, and
every installer does it. Choose **Yes**.

⚠️ **Keep that folder** until your licence is working. The simplest way to
install a licence is to drop the `.lic` file into it and run the installer
again — see below.

---

## Opening the application

| System | How |
|---|---|
| Windows | **Double click** the **NEXTGAMIS ABS** icon on the Desktop or in the Start Menu |
| Linux | **Double click** the **NEXTGAMIS ABS** icon on the Desktop, or find it in the applications list |

On Linux, if no icon appears on the Desktop — the installer only puts one there
if a Desktop folder exists — **search the applications list**: press
**Activities** or **Show Applications** and type `NEXTGAMIS`.

When you find it, **right-click → Add to Favorites**. It then stays in the
left-hand panel, so it opens in one click every launch.

If it still does not appear, use this command — it always works:

```bash
cd /opt/nextgamis-abs && ./nextgamis-abs
```

⚠️ On Linux the first click may ask you to confirm the launcher
(*Allow Launching* or *Trust*). Allow it — this happens once.

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
| **Business name** | For example, `WAKALA BORA` — this is printed on every report you generate |
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

**The simple way — put the file with the installer and run it again.**

The installer looks for any `.lic` file sitting beside it and installs it for
you. You do not have to type anything.

**Windows**

1. Copy the `.lic` file into the folder holding **`install.bat`** — the
   `abs_windows\` folder you unzipped
2. Right-click `install.bat` → **Run as administrator**

**Linux**

```bash
cp your.lic abs_dist_linux/
cd abs_dist_linux
sudo bash install.sh
```

Your data, settings and reports are untouched — re-running the installer only
puts the licence in place.

<br>

**If you deleted the download folder**, the application carries the same tool
and can install a licence on its own:

**Windows**
```
powershell -ExecutionPolicy Bypass -File "C:\Program Files\NEXTGAMIS ABS\update-license.ps1" -Licence C:\path\to\your.lic
```

**Linux**
```bash
sudo /opt/nextgamis-abs/update-license.sh /path/to/your.lic
```

Renewing later works the same way by either route — the new file replaces the
old one, and a licence that still has longer to run is never overwritten.

---

## Upgrading

Install the new version over the old one the same way. **Your data, licence and
settings are kept** — the installer never touches them.

---

### Locking the computer when it is left unattended

The application signs you out after a period of no activity — **on Linux and
macOS**. On Windows, use Windows itself, which locks the whole computer rather
than one program:

**Settings → Accounts → Sign-in options → If you've been away, when should
Windows require you to sign in again?**

Or set a screen saver with **On resume, display logon screen** ticked.

⚠️ This is worth doing wherever the computer sits in a shop. The screen holds
customer names, float figures and commissions, and anyone walking past can read
them.

## Uninstalling

| | |
| --- | --- |
| **Windows** | In the folder you extracted: right-click `uninstall.bat` → **Run as administrator** |
| **Linux** | In the folder you extracted: `sudo bash uninstall.sh` |
| | If you deleted that folder: `sudo bash /opt/nextgamis-abs/uninstall.sh` |

⚠️ Uninstalling **deletes all your data**, auto-backups included. A Desktop
backup is not touched. If you need the data, take one first
(**System Utilities → 3**).

---

## Contact

| | |
|---|---|
| Sales and licences | **sales@tssfl.co** |
| Support | **support@tssfl.co** |
| Phone, WhatsApp, SMS | **+255 762 896 544** |
| Conversation | **[Follow Conversation on TSSFL Technology Stack](https://tssfl.com/viewtopic.php?t=7529)** |
| | [www.tssfl.com](https://www.tssfl.com) · [www.tssfl.co](https://www.tssfl.co) |

© 2026 TSSFL Technology Stack Team — Digital systems since 2012
