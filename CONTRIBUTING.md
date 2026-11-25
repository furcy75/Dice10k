# Contributing to Dice10K / Contribuer à Dice10K

Thank you for your interest in **Dice10K**! Contributions of all kinds are welcome — bug reports, translations, documentation improvements, unit tests, and code.

## Reporting Bugs & Suggesting Features

Open a [GitHub Issue](https://github.com/furcy75/Dice10k/issues) with:
- Your **Dice10K** version and Android version.
- Clear steps to reproduce the issue (or the use case for your suggestion).
- Expected vs. actual behavior.

## Submitting a Pull Request

1. **Fork** the repository and create a branch (`git checkout -b fix/my-fix` or `feat/my-feature`).
2. Keep the app **lightweight, offline-first, permission-free, and dependency-free**.
3. If you add user-facing strings, translate them into all supported languages in `app/src/main/java/fr/jeudes10000/MainActivity.java` (**Français, English, Español, Italiano, Deutsch**).
4. Make sure the project builds cleanly:
   ```sh
   ./gradlew testDebugUnitTest assembleDebug
   ```
5. Open a **Pull Request** describing your changes and how you tested them.

## Adding a Translation

UI strings live in the `TEXT` map in `app/src/main/java/fr/jeudes10000/MainActivity.java`, and detailed game rules are in `REGLES.md`. New languages are always welcome!

## License

By contributing to this repository, you agree that your contributions will be licensed under the **[GNU GPL v3.0](./LICENSE)**.
