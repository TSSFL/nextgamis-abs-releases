# NEXTGAMIS ABS — Jinsi ya Kusakinisha

[English instructions](README.md)

Mwongozo mfupi wa kusakinisha na kutumia NEXTGAMIS ABS kwenye kompyuta yako.

---

## 1. Pakua

Pakua faili kutoka ukurasa wa [Releases](https://github.com/TSSFL/nextgamis-abs-releases/releases):

| Faili | Kwa ajili ya |
| ---------------------------------------- | ------------------------ |
| `NEXTGAMIS_ABS_<toleo>_Windows_x64.zip`  | Windows 10 au 11, 64-bit |
| `NEXTGAMIS_ABS_<toleo>_Linux_x64.tar.gz` | Linux |

### Mifumo inayotumika

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

Kila **'package' inafunguka kuwa folda moja**, na kila kitu hufanyika ndani yake.

| Package | Inafunguka kuwa |
| ---------------------------------------- | ----------------- |
| `NEXTGAMIS_ABS_<toleo>_Windows_x64.zip`  | `abs_windows\` |
| `NEXTGAMIS_ABS_<toleo>_Linux_x64.tar.gz` | `abs_dist_linux/` |

### Windows

1. **Right click** faili la ZIP → **Extract All**

2. Fungua folda hadi uone `install.bat` — iko **ndani ya `abs_windows\`**. Windows huongeza **folda lenye jina la ZIP pia**, hivyo **path sahihi/kamili** mara nyingi ni:

   ```text
   NEXTGAMIS_ABS_1.0.0_Windows_x64\abs_windows\
   ```

3. **Right click** `install.bat` → **Run as administrator**

⚠️ Idadi ya folda inategemea jinsi ulivyofungua ZIP, siyo **Package** chenyewe. Fuata `install.bat`, siyo majina ya folda — popote faili hiyo ilipo, ndiyo folda unayohitaji.

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

⚠️ Usifute folda hiyo mpaka leseni yako ifanye kazi. Njia rahisi ya kusakinisha leseni ni kuweka faili ya `.lic` ndani yake na kuendesha kisakinishi tena — angalia sehemu ya **Leseni** hapa chini.

---

## 3. Leseni

Unapoifungua mara ya kwanza, programu itaonyesha **Machine ID** yako — namba ndefu iliyo ndani ya kisanduku kwenye skrini.

### Tutumie mambo haya matano

Tuma taarifa hizi kwa **[sales@tssfl.co](mailto:sales@tssfl.co)** au WhatsApp **+255 762 896 544**:

| Taarifa | Mfano |
| ------------------- | ---------------------------------------------------- |
| Machine ID | Namba ndefu iliyo kwenye skrini — nakili kama ilivyo |
| Jina la biashara | `WAKALA BORA` — litaonekana kwenye kila ripoti yako |
| Barua pepe | Mahali leseni na ripoti zako zitakapotumwa |
| Aina ya kompyuta | `laptop`, `desktop`, au modeli, mfano `HP 250 G8` |
| Mfumo wa uendeshaji | `Windows 11`, `Windows 10`, `Ubuntu 22.04` |

⚠️ Jina la biashara linakuwa sehemu ya leseni yako na linaonekana kwenye kila ripoti. Litume jinsi unavyotaka lisomeke. Kulibadilisha baadaye kunahitaji leseni mpya.

⚠️ Leseni moja ni kwa kompyuta moja. Ukitumia mfumo kwenye kompyuta mbili, tutumie **Machine ID** ya kila kompyuta — kila kompyuta ina namba yake tofauti.

### Kusakinisha leseni

Njia rahisi ni kuweka faili la leseni pamoja na kisakinishi, kisha kuendesha kisakinishi tena.

Kisakinishi hutafuta faili yoyote ya `.lic` iliyo pamoja nacho na kuisakinisha yenyewe. Huhitaji kuandika komandi yoyote.

### Windows

1. Nakili faili la `.lic` kwenye folda yenye `install.bat` — ile `abs_windows\` uliyofungua kutoka kwenye ZIP.

2. **Right click** `install.bat` → **Run as administrator**

### Linux

```bash
cp leseni.lic abs_dist_linux/
cd abs_dist_linux
sudo bash install.sh
```

Kumbukumbu, mipangilio na ripoti zako havitaguswa — kuendesha kisakinishi tena kunaweka leseni tu.

### Kama ulifuta folda ya upakuaji

Programu ina zana ile ile ndani yake:

**Windows**

```powershell
powershell -ExecutionPolicy Bypass -File "C:\Program Files\NEXTGAMIS ABS\update-license.ps1" -Licence C:\njia\ya\leseni.lic
```

**Linux**

```bash
sudo /opt/nextgamis-abs/update-license.sh /njia/ya/leseni.lic
```

Kuhuisha leseni baadaye ni njia ile ile — faili mpya inachukua nafasi ya ya zamani, na leseni yenye muda mrefu zaidi haifutwi kamwe.

⚠️ Tatizo lolote la leseni — haipo, imeisha muda, au imeharibika — skrini itakayotokea daima itaonyesha **Machine ID** yako. Hutahitaji kuitafuta.

---

## 4. Kufungua programu

| Mfumo | Jinsi |
| ------- | ---------------------------------------------------------------- |
| Windows | Bonyeza aikoni ya **NEXTGAMIS ABS** kwenye Desktop au Start Menu |
| Linux | `cd /opt/nextgamis-abs && ./nextgamis-abs` |

---

## 5. Kuboresha (Update)

Sakinisha toleo jipya juu ya la zamani kwa njia ile ile.

Kumbukumbu zako, leseni na mipangilio yako havitaguswa.

---

## Mawasiliano

| | |
| ------------------- | ------------------------------------------- |
| Mauzo na leseni | [sales@tssfl.co](mailto:sales@tssfl.co) |
| Msaada | [support@tssfl.co](mailto:support@tssfl.co) |
| Simu, WhatsApp, SMS | +255 762 896 544 |

**TSSFL Technology Stack Team — Mifumo ya kidijitali tangu 2012**
