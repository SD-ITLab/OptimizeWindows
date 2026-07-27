# Windows-Optimierungen & Anpassungen
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://badgen.net/github/license/SD-ITLab/OptimizeWindows)


## 🌟 Einleitung
Das Windows-Image kann auf viele unterschiedliche Weise optimiert und angepasst werden. Die hier bereitgestellten Optimierungen basieren auf einer Anleitung aus dem NTLite-Forum, welche ich für meine Zwecke angepasst und erweitert habe.

Ich stelle Windows für Kunden und Personen bereit, die ein optimiertes System ohne Einschränkungen wünschen. Daher beinhalten meine Anpassungen nur allgemeine Änderungen, die im laufenden Betrieb jederzeit rückgängig gemacht werden können.

Meine Voreinstellungen und Optimierungen sind hier auf GitHub verfügbar.  

https://sd-itlab.de/benutzerdefinierte-windowsiso/

## 📂 Verfügbare Optimierungs-Dateien
- **NTLite-Vorlagen**  
  - Enthält Voreinstellungen für Windows 11.
  - Zwei Energievarianten: **High Performance** und **Balanced Performance**.
  - Entfernt unnötige Apps und setzt Registry-Modifikationen.
- **Registry-Modifikationen**  
  - Zwei alternative Power-Dateien sowie Optimierungen für Hintergrund-Apps und Windows-Start.
- **Windows 10 Start-Modifikation**  
  - Bereinigt das Startmenü von Werbung und unnötigen Verknüpfungen.

---

## 📁 NTLite-Vorlagen
Die bereitgestellten **Windows-11-NTLite-Vorlagen** stehen mit zwei Energieprofilen zur Verfügung: **High Performance** und **Balanced Performance**. Sie beinhalten:

### Entfernte Windows-Komponenten & Apps:
- Clipchamp
- Cortana
- Alte Version von Microsoft Edge
- Microsoft OfficeHub (Werbung)
- Solitaire Collection
- Sticky Notes
- Mixed Reality Portal
- Paint 3D
- OneNote
- Microsoft People
- Microsoft Todos
- Microsoft Family
- Microsoft Teams
- Skype
- Microsoft Wallet
- Windows Feedback Hub
- Your Phone
- Groove Music
- OneDrive (NTLite-Lizenz erforderlich)
- Demo-Inhalte für Einzelhandel (NTLite-Lizenz erforderlich)

### Automatische Windows-Installation (unattended.xml):
- Automatische Bestätigung der Lizenzbedingungen
- Erzwingen der lokalen Kontoerstellung (keine Online-Konten)
- Region- und Spracheinstellung auf **Deutsch**
- Erforderliche Diagnosedaten sowie reduzierte OOBE-, Werbe- und Vorschlagsinhalte

### Weitere Windows-Optimierungen:
- Kein automatischer Neustart bei Bluescreens
- Desktop-Icons: "Benutzerordner", "Dieser PC", "Systemsteuerung", "Netzwerk", "Papierkorb"
- Anzeige der Systemsteuerung in **großer Ansicht**
- Taskleiste: "Chat" und "Taskview" ausblenden
- Abschaltung nicht benötigter Hintergrund-Apps
- Energieprofil wahlweise **High Performance** oder **Balanced Performance**
- Laufwerksname **C:\\** in "OS" umbenennen
- Entfernung von **Bloatware und Werbung**
- Bereinigung des **Windows-Startmenüs**

---

## 📁 Registry-Modifikationen
Einige Optimierungen werden über die Windows-Registry vorgenommen. Die Registry-Dateien sind zur besseren Übersicht in **sechs Kategorien** unterteilt:

### 1️⃣ Power-Varianten

Es wird nur **eine** der beiden Dateien verwendet:

- **`Reg_1_Power.reg`** – ältere, aggressive High-Performance-Variante
- **`Reg_1_Power_Balanced.reg`** – empfohlene Balanced-Performance-Variante für PCs und Notebooks

> **Referenz:** Die Vergleichswerte basieren auf Windows 11 25H2. Abhängig von
> CPU, Chipsatztreiber, Firmware und Gerätehersteller können einzelne
> Standardwerte abweichen.

#### Leistung und Reaktionsverhalten

| Einstellung | Standard Höchstleistung AC/DC | Standard Ausbalanciert AC/DC | Unser Balanced Performance AC/DC |
|---|---:|---:|---:|
| CPU-Maximum | 100 % / 100 % | 100 % / 100 % | **100 % / 100 %** |
| `CPMinCores` (mindestens ungeparkt) | 100 % / 50 % | 100 % / 10 % | **50 % / 30 %** |
| `PERFEPP` | 10 / 0 | 25 / 50 | **18 / 50** |
| `PERFEPP1` | 0 / 0 | 33 / 50 | **20 / 50** |
| `PERFBOOSTMODE` | 2 / 2 | 2 / 2 | **2 / 2** |
| `PERFINCPOL` | 2 / 2 | 2 / 0 | **2 / 0** |
| `PERFINCTHRESHOLD` | 30 / 30 | 30 / 90 | **30 / 90** |
| `PERFINCTIME` | 1 / 1 | 1 / 1 | **1 / 1** |
| `CPINCREASETIME` | 7 / 7 | 3 / 3 | **3 / 3** |
| `CPDECREASETIME` | 20 / 20 | 10 / 10 | **15 / 10** |

> **Hinweis zu Core Parking:** `CPMinCores = 100 %` verhindert das allgemeine
> Parken, bedeutet aber nicht, dass alle Kerne ständig aktiv sind; ungenutzte
> Kerne können weiterhin tiefe C-States nutzen. Unsere Einstellung von
> 50 % (AC) bzw. 30 % (DC) lässt bis zu 50 % bzw. 70 % der logischen
> Prozessoren parkbar. Welche Kerne oder CCDs tatsächlich geparkt werden,
> entscheiden Windows sowie CPU- und Chipsatztreiber dynamisch.

Bei modernen CPUs mit aktivem HWP/CPPC sind vor allem `PERFEPP`,
`PERFEPP1` und die Core-Parking-Werte relevant. Die klassischen
`PERFINC*`-Werte bleiben in unserem Profil auf Balanced-Standard und werden
nicht zusätzlich erzwungen.

#### Unterschiede der bereitgestellten REG-Dateien

| Einstellung | `Reg_1_Power.reg` | `Reg_1_Power_Balanced.reg` |
|---|---:|---:|
| Aktiver Energieplan | Höchstleistung | Ausbalanciert |
| CPU-Minimum AC/DC | 5 % / 5 % | 5 % / 5 % |
| CPU-Maximum AC/DC | 100 % / 100 % | 100 % / 100 % |
| Core Parking: mindestens ungeparkt AC/DC | 50 % / 30 % | 50 % / 30 % |
| `PERFEPP` AC/DC | 10 / 0 | 18 / 50 |
| `PERFEPP1` AC/DC | 0 / 0 | 20 / 50 |
| `CPDECREASETIME` AC/DC | 20 / 20 Intervalle | 15 / 10 Intervalle |
| Bildschirm aus AC/DC | Nie / 15 Minuten | Nie / 10 Minuten |
| Standby AC/DC | nicht in der REG festgelegt | Nie / 20 Minuten |
| Deckel schließen AC/DC | Nichts tun | Standby |
| Festplatte aus AC/DC | Nie / 5 Sekunden | Nie / 10 Minuten |
| USB Selective Suspend AC/DC | Aus / Ein | Aus / Ein |
| Kritischer Akku | Herunterfahren | Herunterfahren |
| Ruhezustand/Schnellstart | Aus | Aus |

Die Balanced-Variante erhält 100 % CPU-Maximalleistung und Turbo, reagiert am
Netz leistungsorientierter als Windows-Standard-Balanced und behält im Akku das
energiesparende Verhalten. Sie ist die empfohlene Auswahl für gemischte
Kundensysteme. Die High-Performance-Variante bleibt für Vergleich, Tests und
bewusst aggressiv konfigurierte Systeme verfügbar und enthält ältere manuelle
Performance-State-Timer.

Passende NTLite-Presets:

- `Windows_Tweaks - Windows 11_Power.xml` → `Reg_1_Power.reg`
- `Windows_Tweaks - Windows 11_Balanced.xml` → `Reg_1_Power_Balanced.reg`

### 2️⃣ Reg_2_Apps
- Abschaltung von Hintergrund-Apps zur Reduzierung der CPU-Last

### 3️⃣ Reg_3_Settings
- Deaktivierung von Werbeeinblendungen und Popups

### 4️⃣ Reg_4_Control
- Explorer öffnet standardmäßig "Dieser PC" statt "Schnellzugriff"
- Schnellzugriff in der Navigation ausgeblendet

### 5️⃣ Reg_5_Other
- Entfernung von Werbung und Bloatware
- Blockierung der automatischen Installation von Werbe-Apps

### 6️⃣ Reg_6_StartLayout
- Anpassung des **Windows 11 Startmenüs**
- Entfernung von Werbung/Bloatware aus dem Startmenü

---

## 🎓 Lizenz
Dieses Projekt steht unter der **MIT-Lizenz**. Jeder kann es frei verwenden, anpassen und weitergeben.

---

## 💡 Hinweise
Falls Fragen oder Verbesserungsvorschläge bestehen, gerne ein Issue auf GitHub erstellen oder eine Diskussion starten!


---

# ENGLISH

# Windows Optimizations & Adjustments

## 🌟 Introduction

The Windows image can be optimized and customized in various ways. The optimizations provided here are based on a guide from the NTLite forum, which I have adapted and expanded for my needs.

I provide Windows for customers and individuals who want an optimized system without restrictions. Therefore, my adjustments only include general changes that can be reverted at any time during operation.

My presets and optimizations are available on GitHub.
https://sd-itlab.de/benutzerdefinierte-windowsiso/

## 📂 Available Optimization Files

- **NTLite Templates**
  - Includes presets for Windows 11.
  - Two power variants: **High Performance** and **Balanced Performance**.
  - Removes unnecessary apps and applies registry modifications.
- **Registry Modifications**
  - Two alternative power files plus optimizations for background apps and Windows startup.
- **Windows 10 Start Modification**
  - Cleans up the Start menu by removing ads and unnecessary shortcuts.

---

## 📁 NTLite Templates

The provided **Windows 11 NTLite templates** are available with two power profiles: **High Performance** and **Balanced Performance**. They include:

### Removed Windows Components & Apps:

- Clipchamp
- Cortana
- Old version of Microsoft Edge
- Microsoft OfficeHub (ads)
- Solitaire Collection
- Sticky Notes
- Mixed Reality Portal
- Paint 3D
- OneNote
- Microsoft People
- Microsoft Todos
- Microsoft Family
- Microsoft Teams
- Skype
- Microsoft Wallet
- Windows Feedback Hub
- Your Phone
- Groove Music
- OneDrive (NTLite license required)
- Retail demo content (NTLite license required)

### Automated Windows Installation (unattended.xml):

- Automatic acceptance of license agreements
- Enforces local account creation (no online accounts)
- Region and language set to **German**
- Required diagnostic data with reduced OOBE, advertising and suggestion content

### Additional Windows Optimizations:

- No automatic restart on blue screens
- Desktop icons: "User Folder," "This PC," "Control Panel," "Network," "Recycle Bin"
- Control Panel displayed in **large icons**
- Taskbar: "Chat" and "Task View" hidden
- Disabling unnecessary background apps
- Power profile selectable as **High Performance** or **Balanced Performance**
- Drive name **C:\** renamed to "OS"
- Removal of **bloatware and ads**
- Cleaning up the **Windows Start Menu**

---

## 📁 Registry Modifications

Some optimizations are applied via the Windows Registry. The registry files are categorized into **six sections** for better clarity:

### 1️⃣ Power variants

Use only **one** of the two files:

- **`Reg_1_Power.reg`** – older, aggressive High Performance variant
- **`Reg_1_Power_Balanced.reg`** – recommended Balanced Performance variant for desktops and notebooks

> **Reference:** The comparison values are based on Windows 11 25H2. Individual
> defaults can vary depending on the CPU, chipset driver, firmware and device
> manufacturer.

#### Performance and responsiveness

| Setting | Default High Performance AC/DC | Default Balanced AC/DC | Our Balanced Performance AC/DC |
|---|---:|---:|---:|
| Maximum CPU state | 100% / 100% | 100% / 100% | **100% / 100%** |
| `CPMinCores` (minimum unparked) | 100% / 50% | 100% / 10% | **50% / 30%** |
| `PERFEPP` | 10 / 0 | 25 / 50 | **18 / 50** |
| `PERFEPP1` | 0 / 0 | 33 / 50 | **20 / 50** |
| `PERFBOOSTMODE` | 2 / 2 | 2 / 2 | **2 / 2** |
| `PERFINCPOL` | 2 / 2 | 2 / 0 | **2 / 0** |
| `PERFINCTHRESHOLD` | 30 / 30 | 30 / 90 | **30 / 90** |
| `PERFINCTIME` | 1 / 1 | 1 / 1 | **1 / 1** |
| `CPINCREASETIME` | 7 / 7 | 3 / 3 | **3 / 3** |
| `CPDECREASETIME` | 20 / 20 | 10 / 10 | **15 / 10** |

> **Core Parking note:** `CPMinCores = 100%` disables general core parking,
> but does not mean that every core remains active continuously; unused cores
> can still enter deep C-states. Our setting of 50% (AC) and 30% (DC) allows
> up to 50% and 70% of the logical processors to be parked. Windows and the
> CPU/chipset drivers dynamically decide which cores or CCDs are actually
> parked.

On modern CPUs with active HWP/CPPC, `PERFEPP`, `PERFEPP1` and the core
parking values are the most relevant settings. The classic `PERFINC*` values
remain at the Balanced defaults and are not explicitly overridden.

#### Differences between the provided REG files

| Setting | `Reg_1_Power.reg` | `Reg_1_Power_Balanced.reg` |
|---|---:|---:|
| Active power plan | High Performance | Balanced |
| Minimum CPU state AC/DC | 5% / 5% | 5% / 5% |
| Maximum CPU state AC/DC | 100% / 100% | 100% / 100% |
| Core Parking: minimum unparked AC/DC | 50% / 30% | 50% / 30% |
| `PERFEPP` AC/DC | 10 / 0 | 18 / 50 |
| `PERFEPP1` AC/DC | 0 / 0 | 20 / 50 |
| `CPDECREASETIME` AC/DC | 20 / 20 intervals | 15 / 10 intervals |
| Display timeout AC/DC | Never / 15 minutes | Never / 10 minutes |
| Standby timeout AC/DC | Not defined in REG | Never / 20 minutes |
| Lid close action AC/DC | Do nothing | Sleep |
| Disk timeout AC/DC | Never / 5 seconds | Never / 10 minutes |
| USB Selective Suspend AC/DC | Disabled / Enabled | Disabled / Enabled |
| Critical battery action | Shut down | Shut down |
| Hibernate/Fast Startup | Disabled | Disabled |

The Balanced variant keeps the maximum CPU state and turbo at 100%, improves
plugged-in responsiveness over standard Windows Balanced, and retains efficient
battery behavior. It is recommended for mixed customer systems. The High
Performance variant remains available for comparisons, testing and intentionally
aggressive systems, and contains older manual performance-state timer overrides.

Matching NTLite presets:

- `Windows_Tweaks - Windows 11_Power.xml` → `Reg_1_Power.reg`
- `Windows_Tweaks - Windows 11_Balanced.xml` → `Reg_1_Power_Balanced.reg`

### 2️⃣ Reg\_2\_Apps

- Disabling background apps to reduce CPU load

### 3️⃣ Reg\_3\_Settings

- Disabling ads and popups

### 4️⃣ Reg\_4\_Control

- Explorer opens "This PC" instead of "Quick Access" by default
- Quick Access hidden from the navigation panel

### 5️⃣ Reg\_5\_Other

- Removal of ads and bloatware
- Blocking automatic installation of sponsored apps

### 6️⃣ Reg\_6\_StartLayout

- Adjusting the **Windows 11 Start Menu**
- Removing ads/bloatware from the Start Menu

---

## 🎓 License

This project is licensed under the **MIT License**. Everyone is free to use, modify, and distribute it.

---

## 💡 Notes

If you have any questions or suggestions for improvements, feel free to open an issue on GitHub or start a discussion!


---

