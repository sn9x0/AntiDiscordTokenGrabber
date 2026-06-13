# Token & Browser Protector 🛡️

Ein All-in-One Security Tool, das dich proaktiv vor Discord Token-Grabbern, bösartigen Scripts und Clipboard-Hijackern schützt. 

## ✨ Features

### 1. Discord Core & Sandbox Protection
Moderne Token-Grabber und Malware greifen Discord direkt an, um Passwörter und Tokens zu stehlen. Dieses Tool blockiert diese Angriffe auf zwei Ebenen:
- **`app.asar` Sandboxing:** Erstellt einen isolierten "Tresor"-Ordner für die Discord-Sitzung. Ein Virus findet an der üblichen Stelle in `AppData` keinen Token mehr.
- **`discord_desktop_core` Auto-Heal:** Das Tool überprüft bei jedem Start die berüchtigte `index.js`, in die sich fast alle Token-Grabber einschleusen. Findet es Schadcode, wird dieser gelöscht, die Datei wird in ihren Originalzustand zurückversetzt ("geheilt") und anschließend über das Windows-System schreibgeschützt (Read-Only). 
- **Unterstützte Clients:** Discord Stable, PTB, Canary, Development, Lightcord, ArmCord, Vesktop.

### 2. Anti-Clipboard-Hijacker (Clipper Protection)
Clipboard-Hijacker laufen unsichtbar im Hintergrund und warten darauf, dass du eine Krypto-Adresse (z. B. für eine Überweisung) kopierst. In Millisekunden tauschen sie deine kopierte Adresse gegen die Adresse des Hackers aus.
- Unser Tool läuft (wenn in den Einstellungen aktiviert) komplett unsichtbar im Hintergrund.
- Es scannt die Zwischenablage in Echtzeit nach BTC, ETH, LTC, XMR, TRX und SOL Adressen.
- Wenn eine Adresse in unter 1,5 Sekunden gegen eine *andere* Krypto-Adresse ausgetauscht wird, **blockiert das Tool den Virus**, stellt deine originale Adresse sofort wieder her und warnt dich mit einem Windows-Popup!

### 3. Auto-Start (Persistence)
- Du kannst das Tool so konfigurieren, dass es sich nahtlos in den Windows-Systemstart (Registry) integriert. 
- Es startet im Hintergrund (ohne störendes Fenster), überprüft blitzschnell Discord auf neue Infektionen, heilt diese gegebenenfalls und aktiviert den Anti-Clipboard-Hijacker.

## 🚀 Installation & Nutzung

Das Tool wurde als Standalone `.exe` kompiliert, sodass du weder Python noch andere Module installieren musst.

1. Öffne den Ordner `dist` (nach der Kompilierung).
2. Starte die Datei **`TokenProtector.exe`**.
3. **Im Dashboard:**
   - **Tab "Discord Protect":** Zeigt dir an, ob dein Discord infiziert oder geschützt ist. Klicke auf "Protect", um den Schutz scharfzuschalten.
   - **Tab "Browser Protect":** *(Aktuell im Ausbau)* Hier wird bald der direkte Datei-Lock für Chrome/Edge Cookies eingebaut.
   - **Tab "Clipboard Protect":** Setze den Haken bei "Enable Anti-Clipboard-Hijacker", damit das Tool im Hintergrund auf Viren aufpasst.
4. Setze ganz unten den Haken bei **"Enable Auto-Protection on PC Restart"**, damit du nach einem PC-Neustart nicht mehr an das Tool denken musst.

## ⚠️ Warnung
Dieses Tool verändert Kern-Dateien von Discord, um sie vor Hackern zu sperren. Wenn es ein offizielles Discord-Update gibt, kann es in seltenen Fällen sein, dass Discord meckert. In diesem Fall öffnest du einfach das Tool, klickst auf **"Unprotect"**, lässt Discord updaten und klickst danach wieder auf **"Protect"**.
