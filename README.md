# 🎮 AngabeUnityProjekt_2bk_2026


## 📌 Projektüberblick

Ihr entwickelt in 2er oder 3er-Teams ein **2D-Spiel mit Unity**.

Ziel ist ein spielbares Game mit eigener Grafik, funktionierendem Gameplay und sauberer Teamarbeit über GitHub.

# 🎯 Anforderungen

## 🔧 Technologie

* Unity (2D)
* C#
* GitHub (Classroom)


## 🎮 Spielanforderungen

Euer Spiel muss enthalten:

* ein klares **Spielziel** (z. B. Punkte sammeln, Gegner besiegen, Level abschließen)
* mindestens **1 Spielfigur (Player)**
* mindestens **1 Interaktion** (z. B. Sammeln, Schaden, Trigger)
* mindestens **1 Spielmechanik**, z. B.:

  * Bewegung
  * Springen
  * Schießen
  * Kollisionslogik
* mindestens **1 einfache Spiel-Logik**, z. B.:

  * Punkte-System
  * Leben/Health
  * Timer


## 🎨 Grafische Anforderungen

* mindestens **1–2 selbst erstellte Grafiken pro Person**

  * z. B. Figuren, Items, Hintergründe
* Verwendung im Spiel verpflichtend
* jeder muss auch mindestens eine Animation erstellen



## 🧠 Programmierung

Beide Schüler müssen:

* aktiv **Code schreiben**
* mindestens einen eigenen Bereich implementieren

Beispiele für Aufgabenbereiche:

* Bewegungssystem
* Gegner-Logik
* UI (Score, Leben)
* GameManager
* Kollisionen/Trigger



# 👨‍💻 Arbeitsteilung

## 🧑‍🎓 Schüler A

* eigener Gameplay-Bereich
* eigener Code
* eigene Grafiken

## 🧑‍🎓 Schüler B (bzw. eventuell Schüler C)

* eigener Gameplay-Bereich
* eigener Code
* eigene Grafiken

## 🤝 Gemeinsam

* Integration der Teile
* Feinschliff
* Testing
* Spielbalance



# ⚠️ Wichtige Regeln (GitHub & Unity)

##  Kein paralleles Arbeiten an derselben Szene!

Warum:

* Unity speichert Szenen als **eine Datei**
* → führt zu **Merge-Konflikten**

✅ Lösung:

* klare Aufteilung:
  * verschiedene Szenen (z. B. Level1 / Level2)
  * oder getrennte Systeme (z. B. Player vs. Gegner)
* Absprechen vor Änderungen!
* regelmäßig pushen/pullen

## Projektordner

Das Unity-Projekt muss im Ordner UnityProjekt_GruppenName (GruppenName anpassen) gespeichert werden, da hier eine .gitignore-Datei vorhanden ist, die verhindert, dass alle Projektdateien (z.B. Unity-Libraries) auf Github geladen werden!!!

# 🗂️ GitHub-Regeln

* regelmäßige Commits
* sinnvolle Commit-Nachrichten
* beide Schüler müssen sichtbar beitragen

### Gute Beispiele:

* `Player Movement implementiert`
* `Gegner KI hinzugefügt`
* `UI für Punkte erstellt`
* `Level 1 fertiggestellt`



# 🧪 Technische Umsetzung (Mindestanforderungen)

Euer Projekt muss enthalten:

* mindestens **2 Szenen** (z. B. Menü + Spiel)
* Verwendung von:

  * `Update()` oder `FixedUpdate()`
  * Kollisionen (`OnCollision` oder `OnTrigger`)
* mindestens **2 Scripts pro Person**
* strukturierter Code (keine „eine riesige Datei“)



# 📁 Dokumentation mit Obsidian

## 📂 Ordnerstruktur im Repository

```markdown
/docs
│
├── 00_Start.md
├── 01_Projektidee.md
├── 02_GameDesign.md
├── 03_Technik.md
├── 04_Umsetzung.md
├── 05_Grafiken.md
├── 06_Teamarbeit.md
├── 07_Reflexion.md
└── assets/
```



## 🟢 00_Start

```markdown
# Projekt: [Name]

## Team
- Schüler A
- Schüler B
- (Schüler C)

## Kurzbeschreibung
[2–3 Sätze]

## Navigation
- [[01_Projektidee]]
- [[02_GameDesign]]
- [[03_Technik]]
- [[04_Umsetzung]]
- [[05_Grafiken]]
- [[06_Teamarbeit]]
- [[07_Reflexion]]
```



## 💡 01_Projektidee

* Spielidee
* Ziel des Spiels
* Zielgruppe



## 🎮 02_GameDesign

* Spielfigur(en)
* Spielmechaniken
* Regeln
* Skizzen (optional)



## ⚙️ 03_Technik

* verwendete Scripts
* Aufbau des Projekts
* wichtige Komponenten (z. B. Rigidbody, Collider)



## ⚙️ 04_Umsetzung

* Bereich Schüler A
* Bereich Schüler B
* Integration
* Screenshots



## 🎨 05_Grafiken

* selbst erstellte Assets
* wer hat was gemacht
* Verwendung im Spiel



## 👥 06_Teamarbeit

* Aufgabenverteilung
* Zusammenarbeit
* GitHub-Nutzung



## 🔍 07_Reflexion

* Was lief gut?
* Was war schwierig?
* Was wurde gelernt?



## 🖼️ assets-Ordner

* Screenshots
* Grafiken
* ggf. Skizzen

Einbindung:

```markdown
![[assets/bild.png]]
```



# 📦 Abgabe

## 1. GitHub Repository

* vollständiges Unity-Projekt
* lauffähig
* saubere Struktur

## 2. Dokumentation (`/docs`)

* vollständig ausgefüllt
* verständlich

## 3. README

* Spielbeschreibung
* Steuerung
* Startanleitung

## 4. Präsentation

* Spielidee
* Gameplay
* technische Umsetzung
* eigene Beiträge
* **Live-Demo des Spiels**



# 📋 Checkliste

* [ ] Unity Projekt ist in Ordner `UnityProjekt_GruppenName` (Gruppenname anpassen!)
* [ ] Spiel ist spielbar
* [ ] 2D-Spiel umgesetzt
* [ ] alle Schüler des Teams haben Code geschrieben
* [ ] eigene Grafiken verwendet
* [ ] mindestens 2 Szenen
* [ ] keine Scene-Konflikte (GitHub!)
* [ ] GitHub aktiv genutzt
* [ ] Dokumentation vollständig
* [ ] Präsentation vorbereitet


