<p align="center">
  <strong>🇬🇧 English</strong> ·
  <a href="./README.fr.md">🇫🇷 Français</a> ·
  <a href="./README.es.md">🇪🇸 Español</a> ·
  <a href="./README.it.md">🇮🇹 Italiano</a> ·
  <a href="./README.de.md">🇩🇪 Deutsch</a>
</p>

<p align="center">
  <img src="./screenshots/logo.svg" alt="Dice10K Logo" width="88" height="88">
</p>

<h1 align="center">Dice10K</h1>

<p align="center">
  <strong>A free, lightweight, 100% offline Android scorekeeper for the 10,000 Dice Game (Farkle / Zilch).</strong>
</p>

<p align="center">
  <a href="https://github.com/furcy75/Dice10k/releases/latest">
    <img src="https://img.shields.io/github/v/release/furcy75/Dice10k?color=167D68&label=APK&style=flat-square" alt="Latest Release">
  </a>
  <a href="https://github.com/furcy75/Dice10k/actions/workflows/build-release.yml">
    <img src="https://img.shields.io/github/actions/workflow/status/furcy75/Dice10k/build-release.yml?style=flat-square&label=Build" alt="Build Status">
  </a>
  <a href="./LICENSE">
    <img src="https://img.shields.io/badge/License-GPL--3.0-blue?style=flat-square" alt="GPL-3.0 License">
  </a>
  <img src="https://img.shields.io/badge/Android-6.0%2B%20(API%2023)-3DDC84?style=flat-square&logo=android&logoColor=white" alt="Android 6.0+">
  <img src="https://img.shields.io/badge/Languages-FR%20%C2%B7%20EN%20%C2%B7%20ES%20%C2%B7%20IT%20%C2%B7%20DE-informational?style=flat-square" alt="Languages: FR, EN, ES, IT, DE">
</p>

<p align="center">
  <a href="https://github.com/sponsors/furcy75">
    <img src="https://img.shields.io/badge/GitHub%20Sponsors-Support-EA4AAA?style=flat-square&logo=githubsponsors&logoColor=white" alt="GitHub Sponsors">
  </a>
</p>

<p align="center">
  <a href="#-download--install-the-apk">Download APK</a> ·
  <a href="#-preview">Preview</a> ·
  <a href="#-features">Features</a> ·
  <a href="#-supported-rules">Rules</a> ·
  <a href="#-build-from-source">Build</a> ·
  <a href="#-contributing">Contributing</a> ·
  <a href="#-support-the-project">Support</a>
</p>

---

**Dice10K** is a companion app for real-life tabletop dice games (*10,000* / *Farkle* / *Zilch*). Players roll physical dice and enter their turn points: the app automatically handles totals, the 600-point opening threshold, score tiers, the 3-failures penalty, cascading point steals on exact ties, and winning at **exactly 10,000 points**.

- **Ultra-lightweight**: ~50 KB, written in pure native Android Java with zero external dependencies.
- **Privacy-first**: **zero Android permissions**, no ads, no tracking, 100% offline.
- **Free & open source**: licensed under the GNU GPL v3.

---

## 📥 Download & Install the APK

<p align="center">
  <a href="https://github.com/furcy75/Dice10k/releases/latest">
    <img src="https://img.shields.io/badge/Download%20Latest%20APK-GitHub%20Releases-167D68?style=for-the-badge&logo=android&logoColor=white" alt="Download APK on GitHub Releases">
  </a>
</p>

### Direct installation on Android
1. Open the **[Releases](https://github.com/furcy75/Dice10k/releases/latest)** page and download `Dice10K-v*.apk`.
2. Tap the downloaded APK on your phone.
3. If prompted by Android, allow installation from this source (*"Install unknown apps"*).
4. *(Optional)* Verify file integrity using the `.sha256` checksum attached to each release.

### Installation via ADB (computer)
```sh
adb install -r Dice10K-v1.1.0.apk
```

---

## 📱 Preview

<p align="center">
  <img src="./screenshots/accueil.svg" alt="Dice10K home screen" width="235">
  <img src="./screenshots/partie.svg" alt="Scoreboard and turn entry screen" width="235">
  <img src="./screenshots/abandon.svg" alt="Game history and delete confirmation" width="235">
</p>

---

## ✨ Features

| Feature | Details |
|---|---|
| **2 to 8 players** | Quick player count picker and custom player names. |
| **Complete turn tracking** | Enter points, record a farkle/failure, or apply manual corrections (negative points). |
| **Tiers & 3-failures rule** | Automatic failure cross tracking per tier and automatic tier removal on the 3rd failure. |
| **Cascading point steals** | Landing on an opponent's exact total removes their latest successful gain and cascades through any new ties with a summary popup. |
| **Exact 10,000 win** | Going over 10,000 cancels the turn and counts as a failure; winning locks the game and displays the winner. |
| **History & resume** | Instant resume for active games, per-player tier details, undo entries, and game history management. |
| **5 built-in languages** | Automatically matches your device language and switchable anytime: **Français, English, Español, Italiano, Deutsch**. |
| **100% offline** | Local SQLite database, no internet required. |

---

## 📜 Supported Rules

The 10,000 dice game has many house variants — agree on scoring combinations before starting. Dice10K enforces:

- **600-point opening**: score at least **600 points in one turn** to enter (or reopen if your score drops to 0 or below).
- **Exact 10,000 victory**: exceeding 10,000 rejects the score and counts as a failure.
- **3-failures rule**: failure crosses belong to the current tier; on its 3rd failure, that tier's gain is removed.
- **Ties & stolen points**: reaching an opponent's exact total removes their latest successful gain, cascading if new ties occur (a gain can only be removed once).

👉 Read the full rules in all 5 languages in **[REGLES.md](./REGLES.md)**.

---

## 🛠️ Build from Source

### Prerequisites
- **JDK 17** (or 21)
- **Android SDK** with **Android SDK Platform 35**

### Commands
```sh
git clone https://github.com/furcy75/Dice10k.git
cd Dice10k
./gradlew assembleDebug
```

On Windows:
```powershell
.\gradlew.bat assembleDebug
```

The generated APK is located at:
```text
app/build/outputs/apk/debug/app-debug.apk
```

---

## 🔒 Privacy

Dice10K requests **zero Android permissions** (not even network access).
Player names, scores, and game history stay strictly on your device in a private SQLite database. The *"Support the project"* button simply opens your default web browser if you choose to tap it.

---

## 💖 Support the Project

Dice10K is and will remain **free, open source, and ad-free**.
If the app makes your game nights better and you'd like to support its development:

- ⭐ **Star** this repository on GitHub;
- 💖 Sponsor via **[GitHub Sponsors](https://github.com/sponsors/furcy75)**;
- 🐛 Report bugs, suggest improvements, or help translate!

---

## 🤝 Contributing

Contributions are warmly welcome (bug fixes, unit tests, translations, accessibility, or optional rule variants).
See **[CONTRIBUTING.md](./CONTRIBUTING.md)**, or open an [issue](https://github.com/furcy75/Dice10k/issues) / [pull request](https://github.com/furcy75/Dice10k/pulls).

---

## 📄 License

Distributed under the **[GNU General Public License v3.0 (GPL-3.0)](./LICENSE)**.
