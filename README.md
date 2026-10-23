# Pilule 💊

App iPhone de rappel : « T'as pris ta pilule ? 👀 » toutes les heures de 20h à 1h, jusqu'à ce qu'on réponde Oui.

Compilée automatiquement par GitHub Actions (aucun Mac récent nécessaire), installée avec Sideloadly.

## Compiler

1. Dépose tout le contenu de ce dossier dans un dépôt GitHub **public** (y compris le dossier caché `.github`).
2. Onglet **Actions** → le build « Compiler Pilule » démarre tout seul (5 à 10 min).
3. Quand il est vert ✅ : clique dessus → en bas, **Artifacts** → `Pilule-ipa` → dézippe → `Pilule.ipa`.

Pour relancer un build à la main : Actions → Compiler Pilule → **Run workflow**.

## Installer sur l'iPhone

1. Installe Sideloadly sur le Mac : https://sideloadly.io
2. Branche l'iPhone en USB, déverrouille-le, « Se fier à cet ordinateur ».
3. Glisse `Pilule.ipa` dans Sideloadly, entre ton Apple ID, clique **Start** (code de double authentification si demandé).
4. Sur l'iPhone :
   - Réglages → Général → VPN et gestion de l'appareil → ton Apple ID → **Faire confiance**
   - Réglages → Confidentialité et sécurité → **Mode développeur** → activer (redémarrage)
5. Ouvre Pilule et accepte les notifications.

## Tous les 7 jours

Avec un Apple ID gratuit, l'app expire au bout de 7 jours : rebranche l'iPhone et relance Sideloadly avec le même `Pilule.ipa`. L'historique de la plaquette est conservé.

## Contenu

- `Pilule/PiluleApp.swift` : le code de l'app (SwiftUI, iOS 17+)
- `Pilule/Assets.xcassets` : l'icône
- `project.yml` : description du projet (XcodeGen génère le projet Xcode)
- `.github/workflows/build.yml` : le script de compilation
