# NEXTGAMIS ABS — Jinsi ya Kusakinisha

Mwongozo mfupi wa kusakinisha NEXTGAMIS ABS kwenye kompyuta yako.

---

## 1. Pakua

Pakua faili kutoka ukurasa wa **Releases**:

| Faili | Kwa ajili ya |
|-------|--------------|
| `NEXTGAMIS_ABS_<toleo>_Windows_x64.zip` | Windows 10 au 11, **64-bit** |
| `NEXTGAMIS_ABS_<toleo>_Linux_x64.tar.gz` | Ubuntu 20.04 au mpya zaidi |

⚠️ **Windows lazima iwe 64-bit.** Angalia **Settings → System → About → System
type** kabla ya kusakinisha. Kwenye Windows ya 32-bit usakinishaji unakamilika
lakini programu haitafunguka kamwe.

---

## 2. Sakinisha

### Windows

1. Fungua faili ya ZIP (bonyeza kulia → **Extract All**)
2. Bonyeza kulia `install.bat` → **Run as administrator**
3. Windows itauliza: *"Do you want to allow this app to make changes to your
   device?"* — bonyeza **Yes**

⚠️ Swali hilo ni la kawaida. Windows huuliza hivyo kwa kila programu
inayosakinishwa kwenye `Program Files`. Siyo onyo kuhusu usalama.

### Linux

```bash
tar xzf NEXTGAMIS_ABS_<toleo>_Linux_x64.tar.gz
cd abs_dist_linux
sudo bash install.sh
```

---

## 3. Leseni

Unapoifungua mara ya kwanza, programu itaonyesha **Machine ID** yako — namba
ndefu ndani ya kisanduku skrini.

**Tutumie namba hiyo kwa sales@tssfl.co au WhatsApp +255 762 896 544**, nasi
tutakutumia leseni yako.

Ukipata faili ya leseni (`.lic`), isakinishe hivi:

**Windows**
```
powershell -ExecutionPolicy Bypass -File "C:\Program Files\NEXTGAMIS ABS\update-license.ps1" -Licence C:\njia\ya\leseni.lic
```

**Linux**
```bash
sudo /opt/nextgamis-abs/update-license.sh /njia/ya/leseni.lic
```

⚠️ Tatizo lolote la leseni — haipo, imeisha muda, au imeharibika — skrini
itakayotokea **daima inaonyesha Machine ID yako**. Hutahitaji kuitafuta.

---

## 4. Kufungua programu

| Mfumo | Jinsi |
|-------|-------|
| Windows | Bonyeza aikoni ya **NEXTGAMIS ABS** kwenye Desktop au Start Menu |
| Linux | `cd /opt/nextgamis-abs && ./nextgamis-abs` |

---

## 5. Kuboresha (update)

Sakinisha toleo jipya juu ya la zamani kwa njia ile ile. **Kumbukumbu zako,
leseni na mipangilio yako havitaguswa.**

---

## Mawasiliano

| | |
|---|---|
| Mauzo na leseni | **sales@tssfl.co** |
| Msaada | **support@tssfl.co** |
| Simu, WhatsApp, SMS | **+255 762 896 544** |

TSSFL Technology Stack Team — mifumo ya kidijitali tangu 2012
