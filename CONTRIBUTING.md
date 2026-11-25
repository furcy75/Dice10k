# Contribuer à Dice10K

Merci de votre intérêt pour **Dice10K** ! Toutes les contributions sont les bienvenues, qu’il s’agisse de signaler un bug, d’améliorer la documentation, d’ajouter une langue ou de proposer du code.

## Signaler un bug ou proposer une idée

Ouvrez une [issue sur GitHub](https://github.com/furcy75/Dice10k/issues) en précisant :
- La version de **Dice10K** et la version d’Android utilisée.
- Les étapes pour reproduire le problème (ou le cas d’usage de votre suggestion).
- Le comportement attendu et le comportement observé.

## Proposer une modification (Pull Request)

1. **Forkez** le dépôt et créez une branche dédiée (`git checkout -b fix/mon-correctif` ou `feat/ma-fonctionnalite`).
2. Gardez le projet **léger, hors ligne et sans dépendances superflues** : c’est un choix fondamental de Dice10K.
3. Si vous ajoutez du texte visible à l’écran, pensez à le traduire dans les langues existantes (`MainActivity.java` : Français, English, Español).
4. Vérifiez que le projet compile correctement :
   ```sh
   ./gradlew testDebugUnitTest assembleDebug
   ```
5. Ouvrez une **Pull Request** en décrivant clairement le changement et vos vérifications.

## Ajouter une traduction

Les chaînes d’interface sont regroupées dans la table `TEXT` de `app/src/main/java/fr/jeudes10000/MainActivity.java`, et les règles détaillées se trouvent dans `REGLES.md`. Toute nouvelle langue est la bienvenue !

## Licence

En contribuant à ce dépôt, vous acceptez que vos contributions soient publiées sous la même licence **[GNU GPL v3.0](./LICENSE)** que le projet.
