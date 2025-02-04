# Windows-Optimierungen & Anpassungen
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://badgen.net/github/license/SD-ITLab/OptimizeWindows)


## 🌟 Einleitung
Das Windows-Image kann auf viele unterschiedliche Weise optimiert und angepasst werden. Die hier bereitgestellten Optimierungen basieren auf einer Anleitung aus dem NTLite-Forum, welche ich für meine Zwecke angepasst und erweitert habe.

Ich stelle Windows für Kunden und Personen bereit, die ein optimiertes System ohne Einschränkungen wünschen. Daher beinhalten meine Anpassungen nur allgemeine Änderungen, die im laufenden Betrieb jederzeit rückgängig gemacht werden können.

Meine Voreinstellungen und Optimierungen sind auf GitHub verfügbar.  
https://sd-itlab.de/benutzerdefinierte-windowsiso/

## 📂 Verfügbare Optimierungs-Dateien
- **NTLite-Vorlagen**  
  - Enthält Voreinstellungen für Windows 10 und Windows 11.
  - Entfernt unnötige Apps und setzt Registry-Modifikationen.
- **Registry-Modifikationen**  
  - Optimierungen der Energieeinstellungen, Hintergrund-Apps und Windows-Start.
- **Windows 10 Start-Modifikation**  
  - Bereinigt das Startmenü von Werbung und unnötigen Verknüpfungen.

---

## 📁 NTLite-Vorlagen
Die bereitgestellten **NTLite-Vorlagen** existieren in zwei Versionen für **Windows 10** und **Windows 11**. Diese Vorlagen beinhalten:

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
- Privatsphären-Einstellungen auf minimalste Stufe

### Weitere Windows-Optimierungen:
- Kein automatischer Neustart bei Bluescreens
- Desktop-Icons: "Benutzerordner", "Dieser PC", "Systemsteuerung", "Netzwerk", "Papierkorb"
- Anzeige der Systemsteuerung in **großer Ansicht**
- Taskleiste: "Chat" und "Taskview" ausblenden
- Abschaltung nicht benötigter Hintergrund-Apps
- Energiesparmodus auf **Höchstleistung**
- Laufwerksname **C:\\** in "OS" umbenennen
- Entfernung von **Bloatware und Werbung**
- Bereinigung des **Windows-Startmenüs**

---

## 📁 Registry-Modifikationen
Einige Optimierungen werden über die Windows-Registry vorgenommen. Die Registry-Dateien sind zur besseren Übersicht in **sechs Kategorien** unterteilt:

### 1️⃣ Reg_1_Power
- Powerbutton führt zu **Herunterfahren**
- "Nichts tun" beim Schließen des Notebook-Deckels
- Festplatten-Abschaltung auf **Niemals** gesetzt
- Selektives USB-Energiesparen deaktiviert
- **Hibernate (Schnellstart)** deaktiviert (verursacht oft Probleme)
- Standard-Energiesparplan auf **Höchstleistung** gesetzt

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



💡 Hinweise

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
  - Includes presets for Windows 10 and Windows 11.
  - Removes unnecessary apps and applies registry modifications.
- **Registry Modifications**
  - Optimizations for power settings, background apps, and Windows startup.
- **Windows 10 Start Modification**
  - Cleans up the Start menu by removing ads and unnecessary shortcuts.

---

## 📁 NTLite Templates

The provided **NTLite templates** exist in two versions for **Windows 10** and **Windows 11**. These templates include:

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
- Privacy settings set to the lowest level

### Additional Windows Optimizations:

- No automatic restart on blue screens
- Desktop icons: "User Folder," "This PC," "Control Panel," "Network," "Recycle Bin"
- Control Panel displayed in **large icons**
- Taskbar: "Chat" and "Task View" hidden
- Disabling unnecessary background apps
- Power mode set to **High Performance**
- Drive name **C:\** renamed to "OS"
- Removal of **bloatware and ads**
- Cleaning up the **Windows Start Menu**

---

## 📁 Registry Modifications

Some optimizations are applied via the Windows Registry. The registry files are categorized into **six sections** for better clarity:

### 1️⃣ Reg\_1\_Power

- Power button set to **Shutdown**
- "Do nothing" when closing the laptop lid
- Hard drive shutdown set to **Never**
- Selective USB power saving disabled
- **Hibernate (Fast Startup)** disabled (often causes issues)
- Default power plan set to **High Performance**

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

