
## ❗ Problem

GitHub Desktop zeigt:

> „Original oder Fork verwenden?“

Danach:

* ❌ Fetch / Pull funktioniert nicht
* ❌ Fehler: *Repository existiert nicht mehr*

👉 Ursache: Zugriff auf das Lehrer-Repository (`upstream`) ohne Rechte

---

# 🔧 Vorbereitung: Git richtig einrichten (Windows)

Damit die Befehle funktionieren, muss **git.exe im Pfad (PATH)** sein.

## Schritt 1: Suche öffnen

* Windows-Taste drücken
* eingeben:

```text
Umgebungsvariablen für dieses Konto bearbeiten
```

---

## Schritt 2: PATH bearbeiten

1. Klick auf **Umgebungsvariablen…**
2. Oben bei **Benutzervariablen** → `Path` auswählen
3. Klick auf **Bearbeiten**

---

## Schritt 3: Git-Pfad hinzufügen

Falls noch nicht vorhanden:

```text
C:\Users\ento\AppData\Local\GitHubDesktop\app-3.5.8\resources\app\git\cmd
```

👉 Falls Git woanders installiert ist, entsprechenden Pfad wählen
Tipp: `"Dateispeicherort öffnen"` beim `Github-Desktop-Link` am Desktop führt zum Programmordner!

---

## Schritt 4: Speichern

* Alle Fenster mit **OK** schließen
* Terminal danach **neu starten!**

---

## Schritt 5: Test

Im Terminal (CMD):

```bash
git --version
```

👉 Ausgabe sollte z. B. sein:

```text
git version 2.xx.x
```

---

# ✅ Lösung Teil 1: GitHub Desktop einstellen

## Fork Behavior setzen

1. Repository in **GitHub Desktop öffnen**
2. Menü:

```text
Repository → Repository Settings…
```

3. Links:

```text
Fork Behavior
```

4. auswählen:

```text
✅ For my own purposes
```

5. **Save**

---

# ✅ Lösung Teil 2: upstream entfernen

## Schritt 1: Terminal öffnen

In GitHub Desktop:

```text
Repository → Open in Command Prompt
```

---

## Schritt 2: Remotes anzeigen

```bash
git remote -v
```

👉 Wenn du **upstream** siehst:

```bash
origin    https://github.com/... (fetch)
origin    https://github.com/... (push)
upstream  https://github.com/... (fetch)
```

➡️ Dann ist das die Fehlerquelle ❌

---

## Schritt 3: upstream entfernen

```bash
git remote remove upstream
```

---

## Schritt 4: Kontrolle

```bash
git remote -v
```

👉 Es darf nur noch **origin** vorhanden sein:

```bash
origin https://github.com/... (fetch)
origin https://github.com/... (push)
```

---

# 🧠 Merksatz

> „Ich arbeite nur mit meinem eigenen Repo → kein upstream!“
