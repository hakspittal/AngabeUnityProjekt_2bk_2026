# 🔧 1. Arbeiten mit GitHub (Kurzüberblick)

## 🔁 Workflow (immer gleich!)

1. **Pull** (aktuelle Version holen)
2. **In Unity arbeiten**
3. **Commit** (Änderungen speichern)
4. **Push** (hochladen)

## ⚠️ Wichtig für Unity

❌ Nie gleichzeitig bearbeiten:

* gleiche Szene (`.unity`)
* gleiche Prefabs

👉 Sonst entstehen **Merge-Konflikte**

## ✅ Gute Aufteilung

| Schüler A | Schüler B |
| --------- | --------- |
| Szene A   | Szene B   |
| Player    | UI        |
| Logik     | Gegner    |

# 🎬 2. Arbeiten mit mehreren Szenen

Es gibt **2 wichtige Varianten**, wie ihr Szenen verwendet:

## 🧩 Variante 1: Klassischer Szenenwechsel (Level-System)

👉 Szenen werden **nacheinander geladen**

## Beispiel:

* `MainMenu`
* `Level1`
* `Level2`


### 🔀 Szene wechseln

```csharp
using UnityEngine;
using UnityEngine.SceneManagement;

public class SceneLoader : MonoBehaviour
{
    public void LoadScene(string sceneName)
    {
        SceneManager.LoadScene(sceneName);
    }
}
```

👉 Beispiel:

* Button → lädt `"Level1"`

### 🧠 Einsatz

✔ Level-System
✔ Menü → Spiel
✔ Game Over → Neustart

---

## 🧩 Variante 2: Szenen kombinieren (Additive Scenes) ⭐

👉 Mehrere Szenen werden **gleichzeitig geladen**

💡 Das ist perfekt für Teamarbeit!


### 🏗️ Idee

| Szene        | Inhalt            |
| ------------ | ----------------- |
| `MainScene`  | Spielwelt         |
| `UIScene`    | UI (Score, Leben) |
| `EnemyScene` | Gegner            |

👉 Jeder kann an **eigener Szene arbeiten**


### 🚀 Additive Szene laden

```csharp
using UnityEngine;
using UnityEngine.SceneManagement;

public class SceneLoaderAdditive : MonoBehaviour
{
    void Start()
    {
        SceneManager.LoadScene("UIScene", LoadSceneMode.Additive);
    }
}
```


### 🔄 Erklärung

* `LoadSceneMode.Additive`
  👉 lädt Szene **zusätzlich**, ohne die aktuelle zu ersetzen


### 🎯 Beispiel: Beim Start beide Szenen laden

### Szene 1:

* `MainScene` (Startszene)

### Script in MainScene:

```csharp
void Start()
{
    SceneManager.LoadScene("UIScene", LoadSceneMode.Additive);
}
```

👉 Ergebnis:

* Spielwelt + UI gleichzeitig aktiv


## ⚠️ Wichtig!

### 1. Szenen in Build Settings eintragen

👉 Sonst funktioniert das Laden nicht!


### 2. Mehrere Szenen im Editor öffnen

👉 Für Entwicklung praktisch:

* `File → Open Scene Additive`

### 3. Szene entladen (optional)

```csharp
SceneManager.UnloadSceneAsync("UIScene");
```

---

# 🧠 Vergleich der Varianten

| Variante      | Beschreibung     | Wann verwenden?        |
| ------------- | ---------------- | ---------------------- |
| **LoadScene** | ersetzt Szene    | Level-System           |
| **Additive**  | fügt Szene hinzu | Teamarbeit, UI, Module |


# 👥 3. Teamarbeit mit Additive Scenes (Empfohlen ⭐)

## 💡 Struktur

| Schüler | Szene     |
| ------- | --------- |
| A       | MainScene |
| B       | UIScene   |

👉 Vorteile:

* keine Konflikte
* klare Trennung
* paralleles Arbeiten


## 📦 Typische Kombination

* 🎮 Gameplay → eigene Szene
* 🧾 UI → eigene Szene
* 👾 Gegner → eigene Szene


# 🧪 4. Testen

✔ Werden alle Szenen geladen?
✔ Gibt es doppelte Objekte?
✔ Funktioniert UI + Gameplay zusammen?


## 🧨 Häufige Fehler

❌ Szene nicht im Build
❌ falscher Name (`"uiscene"` ≠ `"UIScene"`)
❌ beide Szenen haben z.B. je eine Kamera oder EventSystem

👉 Lösung:

* nur **eine Kamera aktiv**
* nur **ein EventSystem**

