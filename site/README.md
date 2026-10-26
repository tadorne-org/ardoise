# ardoise.tadorne.org — site du projet

Site Hugo d'**Ardoise**, présenté comme un instrument **Tadorne** : un
afficheur de pied de mât pour la régate. Bilingue EN (racine) / FR (`/fr/`),
sans thème externe, sans JavaScript, sans requête tierce.

## Construire

```console
$ hugo server          # http://localhost:1313/  (FR sur /fr/)
$ hugo --minify        # build de production dans public/
```

Requiert Hugo ≥ 0.146 (testé avec 0.166.0 extended, installé via Homebrew).
`public/` n'est pas versionné.

## Structure

```
hugo.toml              config, langues, menus, params (dont seoIndexable)
i18n/{en,fr}.toml      chaînes d'interface
content/en/            contenu anglais  → /
content/fr/            contenu français → /fr/
assets/css/            tokens.css (charte Tadorne) + fonts.css + main.css
static/fonts/          woff2 auto-hébergés
static/img/            logos Tadorne, captures d'écran de l'afficheur (WebP)
layouts/               home, page, roadmap, log/, _partials/, _markup/, _shortcodes/
```

## Publier une info (le journal)

Les deux fichiers doivent porter le **même `translationKey`** — c'est le seul
lien entre les langues :

```console
$ hugo new content/en/log/ma-note.md
$ hugo new content/fr/journal/ma-note.md
```

```yaml
---
title: "Titre"
translationKey: log/ma-note
date: 2026-09-15
description: "Une ou deux phrases : listes, RSS et og:description."
params:
  tags: ["ardoise"]
---
```

Le fil RSS est sur `/log/index.xml` et `/fr/journal/index.xml`.

## Photos et captures

```
{{</* photo src="img/journal/x.png" alt="…" caption="…" */>}}
```

L'image est cherchée dans `assets/`, réduite à 1400 px et convertie en WebP
au build. Les originaux restent dans `assets/` et ne sont jamais publiés
tels quels. Les captures d'écran de l'afficheur sont déjà en WebP sans perte
dans `static/img/` (`ecran-*.webp`), métadonnées retirées.

## Indexation : ouverte

`params.seoIndexable = true` dans `hugo.toml` : pas de `noindex`, et
`robots.txt` autorise l'exploration. Passer à `false` ferme à nouveau le
site (`<meta name="robots" content="noindex, nofollow">` sur chaque page et
`Disallow: /`).

## Déploiement

`hugo --minify` produit un `public/` statique — n'importe quel hébergeur
statique convient.

`baseURL` vaut `https://ardoise.tadorne.org/` ; le surcharger au besoin avec
`hugo --baseURL https://exemple/`.

## Licences

- Contenu (`content/`, images, vidéos) : [CC BY-SA 4.0](LICENSE-CONTENT).
- Gabarits, CSS et configuration : [MIT](LICENSE).
- Polices (`static/fonts/`) : SIL Open Font License 1.1, propriété de leurs auteurs.
