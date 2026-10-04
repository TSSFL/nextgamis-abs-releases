# NEXTGAMIS ABS — Jinsi ya Kusakinisha (Kuinstall)

[English instructions](README.md)

Mwongozo mfupi wa kusakinisha na kutumia NEXTGAMIS ABS kwenye kompyuta yako.

---

## 1. Pakua

**Bonyeza kiungo, upakuaji unaanza mara moja.**

### ⬇ [PAKUA KWA WINDOWS (64-bit) — 85 MB](https://github.com/TSSFL/nextgamis-abs-releases/releases/latest/download/NEXTGAMIS_ABS_1.0.0_Windows_x64.zip)
### ⬇ [PAKUA KWA LINUX — 96 MB](https://github.com/TSSFL/nextgamis-abs-releases/releases/latest/download/NEXTGAMIS_ABS_1.0.0_Linux_x64.tar.gz)

[SHA256SUMS.txt](https://github.com/TSSFL/nextgamis-abs-releases/releases/latest/download/SHA256SUMS.txt) — kwa kuhakikisha faili lako halikukatika wakati wa kupakua.

<details>
<summary><b>Kuhakikisha faili lako halikukatika (si lazima)</b></summary>

Intaneti ikikatika wakati wa upakuaji, faili linaweza kuonekana zima lakini
likawa pungufu. Likijaribu kusakinisha, makosa yanayotokea huwa hayaeleweki.
`SHA256SUMS.txt` lina alama ya kipekee ya kila faili — ukipata alama ile ile,
faili lako ni zima.

**Windows** — fungua PowerShell kwenye folda lenye faili ulilopakua:

```powershell
cd $HOME\Downloads
Get-FileHash NEXTGAMIS_ABS_1.0.0_Windows_x64.zip -Algorithm SHA256 | Format-List Hash
```

Linganisha jibu na alama iliyo kwenye `SHA256SUMS.txt`. Zikifanana, faili ni zima.

**Linux** — weka faili mbili kwenye folda moja, kisha:

```bash
cd ~/Downloads
curl -LO https://github.com/TSSFL/nextgamis-abs-releases/releases/latest/download/SHA256SUMS.txt
sha256sum -c SHA256SUMS.txt --ignore-missing
```

| Jibu | Maana |
| --- | --- |
| `OK` | Faili ni zima — endelea kusakinisha |
| `FAILED` | Faili lilikatika — **pakua tena** |

⚠️ Ukaguzi huu unaonyesha kama faili lilikatika wakati wa kupakua. Hauonyeshi
kama faili limebadilishwa na mtu — anayeweza kubadilisha programu anaweza pia
kubadilisha alama zake. Thamani yake halisi ni kwenye intaneti isiyo thabiti.

</details>

⚠️ Ukurasa wa Matoleo unaonyesha pia **"Source code (zip)"** na **"Source
code (tar.gz)"** chini kabisa. GitHub huweka yenyewe kwenye kila toleo.
Hivyo siyo programu — ni nakala ndogo ya maelekezo haya. **Usizipakue.**

### Mifumo ya Kompyuta (OS) Yenye Sifa ya Kusanikisha

**Windows** — Windows 10 na Windows 11, 64-bit pekee.

⚠️ Angalia **Settings → System → About → System type** kabla ya kupakua. Kwenye Windows ya 32-bit, usakinishaji unakamilika na kuonyesha umefanikiwa, lakini programu haitafunguka. Toleo la 32-bit halipo.

**Linux** — inahitaji glibc 2.29 au mpya zaidi:

| Mfumo | |
| -------------------------------------------- | ------ |
| Ubuntu 20.04 LTS na mpya zaidi | ndiyo |
| Debian 11 na mpya zaidi | ndiyo |
| Linux Mint 20 na mpya zaidi | ndiyo |
| Kali Linux (2020 na kuendelea) | ndiyo |
| Fedora 30, RHEL/Rocky 9 na mpya zaidi | ndiyo |
| openSUSE Leap 15.3, Tumbleweed, SLES 15 SP3+ | ndiyo |
| Debian 10, RHEL/Rocky 8 | hapana |
| openSUSE Leap 15.2 na za zamani, SLES 12 | hapana |

Angalia kwa **komandi** hii:

```bash
ldd --version | head -1
```

Ikiwa namba ni **2.29 au zaidi**, mfumo utafanya kazi.

Kila kitu kinachohitajika kinakuja pamoja na programu. Hakuna intaneti wala vifurushi vya ziada vinavyohitajika **kusakinisha au kutumia** programu.

---

## 2. Sakinisha

Kila **'package' inafunguka kuwa folda moja**, na usakinishaji hufanyika ndani yake.

| Package | Inafunguka kuwa |
| ---------------------------------------- | ----------------- |
| `NEXTGAMIS_ABS_<toleo>_Windows_x64.zip`  | `abs_windows\` |
| `NEXTGAMIS_ABS_<toleo>_Linux_x64.tar.gz` | `abs_dist_linux/` |

### Windows

1. **Right click** faili la ZIP → **Extract All**

2. Fungua folda hadi uone faili `install.bat` — liko **ndani ya `abs_windows\`**. Windows huongeza **folda lenye jina la ZIP pia**, hivyo **path sahihi** mara nyingi ni:

   ```text
   NEXTGAMIS_ABS_1.0.0_Windows_x64\abs_windows\
   ```

3. **Right click** `install.bat` → **Run as administrator**

⚠️ Idadi ya folda inategemea jinsi ulivyofungua ZIP, siyo **Package** yenyewe. Fuata `install.bat`, siyo majina ya folda — popote faili hilo lilipo, ndiyo folda unayohitaji.

4. Windows itauliza:

   **"Do you want to allow this app to make changes to your device?"**

   Bonyeza **Yes**.

⚠️ Swali hilo ni la kawaida. Windows huuliza hivyo kwa kila programu inayosakinishwa kwenye `Program Files`. Siyo onyo kuhusu usalama.

### Linux

```bash
tar xzf NEXTGAMIS_ABS_<toleo>_Linux_x64.tar.gz
cd abs_dist_linux
sudo bash install.sh
```

⚠️ Usifute folda hiyo mpaka leseni yako ifanye kazi. Njia rahisi ya kusakinisha leseni ni kuweka faili la `.lic` ndani yake na kurun kisakinishi tena — angalia sehemu ya **Leseni** hapa chini.

---

## Jinsi ya kufungua Terminal au PowerShell

Sehemu chache za mwongozo huu zinahitaji kuandika komandi. Hivi ndivyo
unavyofungua mahali pa kuziandika.

### Linux — Terminal

Njia yoyote kati ya hizi:

| Njia | Jinsi |
| --- | --- |
| Kwa kiibodi | Bonyeza **Ctrl + Alt + T** |
| Kwa kutafuta | Bonyeza **Activities** au **Show Applications**, andika `terminal`, kisha ifungue |
| Kwa Right click | **Right click** kwenye folda au Desktop → **Open in Terminal** |

Dirisha (mara nyingi jeusi) litafunguka. Andika komandi, kisha bonyeza **Enter**.

### Windows — PowerShell

| Njia | Jinsi |
| --- | --- |
| Kwa kutafuta | Bonyeza **Start**, andika `powershell`, kisha ibonyeze |
| Kwa Right click | **Right click** kitufe cha **Start** → **Terminal** au **Windows PowerShell** |
| Kwa Run | Bonyeza **Windows + R**, andika `powershell`, bonyeza **Enter** |
| Kwa njia ya moja kwa moja | Bonyeza **Windows + S**, andika `powershell`, bonyeza **Enter** |

⚠️ Komandi za kusakinisha leseni zinahitaji **ruhusa ya admin**. Badala ya
kuifungua kawaida, **Right click** → **Run as administrator**. Ukiiona PowerShell
yenye maandishi `Administrator` juu, upo sahihi.

⚠️ Unapoandika path yenye nafasi — mfano `C:\Program Files\NEXTGAMIS ABS` —
iweke ndani ya alama za nukuu `"..."` kama zilivyoonyeshwa kwenye komandi.

---

## 3. Leseni

Unapoifungua mara ya kwanza, programu itaonyesha **Machine ID** yako — namba ndefu iliyo ndani ya kisanduku kwenye skrini.

### Tutumie taarifa hizi tano

Tuma taarifa hizi kwenda **[sales@tssfl.co](mailto:sales@tssfl.co)** au WhatsApp **+255 762 896 544**:

| Taarifa | Mfano |
| ------------------- | ---------------------------------------------------- |
| Machine ID | Namba ndefu iliyo kwenye skrini — nakili kama ilivyo |
| Jina la biashara | Mfano, `WAKALA BORA` — litaonekana kwenye kila ripoti yako |
| Barua pepe | Mahali leseni na nyaraka zingine kama manual zitakapotumwa |
| Aina ya kompyuta | `laptop`, `desktop`, au modeli, mfano `HP 250 G8` |
| Mfumo wa Kompyuta (Operating System - OS) | `Windows 11`, `Windows 10`, `Ubuntu 22.04` |

⚠️ Jina la biashara linakuwa sehemu ya leseni yako na litaonekana kwenye kila ripoti. Litume jinsi unavyotaka lisomeke. Kulibadilisha baadaye kunahitaji leseni mpya.

⚠️ Leseni moja ni kwa kompyuta moja. Ukitumia mfumo kwenye kompyuta mbili, tutumie **Machine ID** ya kila kompyuta — kila kompyuta inahitaji leseni yake.

### Kusakinisha leseni

Njia rahisi ni kuweka faili la leseni pamoja na kisakinishi, kisha kurun kisakinishi tena.

Kisakinishi hutafuta faili lolote la `.lic` lililo pamoja nacho na kulisakinisha yenyewe. Huhitaji kuandika komandi yoyote.

### Windows

1. Nakili faili la `.lic` kwenye folda lenye `install.bat` — `abs_windows\` ulilolifungua kutoka kwenye ZIP.

2. **Right click** `install.bat` → **Run as administrator**

### Linux

```bash
cp leseni.lic abs_dist_linux/
cd abs_dist_linux
sudo bash install.sh
```

Data, settings na ripoti zako havitaguswa — kurun kisakinishi tena kunaweka leseni tu.

### Kama ulifuta folda ulilopakua

Programu ina zana ile ile ndani yake, kwa hiyo tumia komandi:

**Windows**

```powershell
powershell -ExecutionPolicy Bypass -File "C:\Program Files\NEXTGAMIS ABS\update-license.ps1" -Licence C:\path\ya\leseni.lic
```

**Linux**

```bash
sudo /opt/nextgamis-abs/update-license.sh /path/ya/leseni.lic
```

Kuhuisha leseni baadaye utahitaji kufuata njia ile ile — faili mpya linachukua nafasi ya la zamani, na leseni yenye muda mrefu zaidi haifutwi, inabaki.

⚠️ Kama kuna tatizo lolote la leseni — haipo, imeisha muda wake, au imeharibika — hilo tatizo litaonyehswa kwenye skrini pamoja na **Machine ID** yako mara tu unapoanzisha (launch) mfumo. Hutahitaji kuitafuta.

---

## 4. Kufungua programu

| Mfumo | Jinsi |
| ------- | ---------------------------------------------------------------- |
| Windows | **Double click** aikoni ya **NEXTGAMIS ABS** kwenye Desktop au Start Menu |
| Linux | **Double click** aikoni ya **NEXTGAMIS ABS** kwenye Desktop, au itafute kwenye orodha ya programu |

Kwa Linux, kama aikoni haionekani kwenye Desktop (kama hakuna Desktop folda),
**itafute kwenye orodha ya programu** — bonyeza **Activities** au **Show
Applications**, kisha andika `NEXTGAMIS`.

Ukiiona, **Right click** aikoni yake → **Add to Favorites**. Baada ya hapo
itabaki kwenye panel ya upande wa kushoto, hivyo utaifungua kwa kubonyeza mara moja tu
kila mara.

Kama bado haionekani, tumia komandi hii — hii hufanya kazi daima:

```bash
cd /opt/nextgamis-abs && ./nextgamis-abs
```

⚠️ Kwenye Linux, mara ya kwanza unapobonyeza aikoni, mfumo unaweza kukuuliza
uiamini au kuiruhusu programu hii (*Allow Launching* au *Trust*). Bonyeza kuruhusu — hii hutokea mara
moja tu.

---

## 5. Kuboresha (Update)

Sakinisha toleo jipya juu ya la zamani kwa njia ile ile.

Data zako, leseni na settings zako havitaguswa.

---

## 6. Kuondoa programu

| Windows | Right click `uninstall.bat` → **Run as administrator** |
| --- | --- |
| **Linux** | `sudo bash /opt/nextgamis-abs/uninstall.sh` |

⚠️ Kuondoa programu **kunafuta data zako zote** pamoja na backup za
kiotomatiki. Backup ya Desktop haiguswi. Kama unahitaji data zako, chukua
backup ya Desktop kwanza (**System Utilities → 3**).

---

## Mawasiliano

| | |
| ------------------- | ------------------------------------------- |
| Mauzo na leseni | [sales@tssfl.co](mailto:sales@tssfl.co) |
| Msaada | [support@tssfl.co](mailto:support@tssfl.co) |
| Simu, WhatsApp, SMS | +255 762 896 544 |
| Mjadala | **[Fuatilia Mjadala TSSFL Technology Stack](https://tssfl.com/viewtopic.php?t=7529)** |

**TSSFL Technology Stack Team — Mifumo ya kidijitali tangu 2012**
