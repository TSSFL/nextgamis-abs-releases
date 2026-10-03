# NEXTGAMIS ABS — Releases

Installation packages for **NEXTGAMIS ABS**, the offline-first agency banking
terminal from [TSSFL Technology Stack Team](https://www.tssfl.com).

**This repository holds releases only — no source code.**

---

## Download

Take the newest entry from **[Releases](../../releases)** and pick the file for
your system.

| File | For |
|------|-----|
| `NEXTGAMIS_ABS_<version>_Windows_x64.zip` | Windows 10 or 11, **64-bit** |
| `NEXTGAMIS_ABS_<version>_Linux_x64.tar.gz` | Ubuntu 20.04 or newer, and equivalents |

⚠️ **Windows must be 64-bit.** Check **Settings → System → About → System type**
before installing. A 32-bit build does not exist, and on a 32-bit installation
the installer finishes and reports success while the application never starts.

### Check your download

The download is large and a dropped connection leaves a file that looks complete
but is not. Compare it against `SHA256SUMS.txt` from the same release:

```bash
sha256sum -c SHA256SUMS.txt          # Linux
```
```powershell
Get-FileHash .\NEXTGAMIS_ABS_1.0.0_Windows_x64.zip -Algorithm SHA256   # Windows
```

A mismatch means the download broke — fetch it again. It does not mean the
software is damaged.

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

NEXTGAMIS ABS runs on a licence issued for one machine. On first start the
application shows your **Machine ID** — a long code in a box on screen. Send it
to **sales@tssfl.co** and we will issue your licence.

Whatever is wrong with a licence — missing, expired, damaged — the screen you
see shows that Machine ID. You never have to go looking for it.

Installing or renewing a licence:

```bash
sudo /opt/nextgamis-abs/update-license.sh /path/to/your.lic          # Linux
```
```
powershell -ExecutionPolicy Bypass -File "C:\Program Files\NEXTGAMIS ABS\update-license.ps1" -Licence C:\path\to\your.lic
```

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
