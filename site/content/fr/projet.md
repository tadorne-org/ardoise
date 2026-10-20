---
title: "L'instrument"
translationKey: project
url: /fr/projet/
description: "Un afficheur de pied de mât, lisible du cockpit, sur le bus NMEA 2000 du bord."
params:
  eyebrow: "Ardoise"
  figures:
    - label: "Alimentation et données"
      value: "NMEA 2000"
    - label: "Autres sources"
      value: "Signal K · téléphone"
    - label: "Rafraîchissement"
      value: "1 Hz"
    - label: "Commande"
      value: "Téléphone, sans bouton"
---

## Le besoin

En régate, les chiffres utiles se lisent d'un coup d'œil, depuis le cockpit ou le rail : compte à rebours, vitesse, cap et adonnante, angle et force du vent. À trois ou six mètres, en plein soleil, avec ou sans lunettes polarisées.

## L'écran

Un écran réfléchissant à mémoire : noir sur blanc, rafraîchi chaque seconde, sans la rémanence du papier électronique. Il renvoie la lumière du jour comme une feuille imprimée. Les pages sont dessinées pour la distance : trois chiffres géants plutôt que quatre petits.

<div class="photo-grid">
  <img src="/img/ecran-pre-depart.webp" alt="Maquette d'écran : compte à rebours de départ 4:59, en chiffres géants.">
  <img src="/img/ecran-pre-depart-inverse.webp" alt="Maquette d'écran : dernière minute avant le départ, en négatif.">
  <img src="/img/ecran-pres.webp" alt="Maquette d'écran : au près, cap en grand, adonnante, vitesse et pourcentage de la polaire.">
  <img src="/img/ecran-portant.webp" alt="Maquette d'écran : au portant, deux valeurs empilées.">
  <img src="/img/ecran-neutre.webp" alt="Maquette d'écran : quatre valeurs, vitesse et vent.">
  <img src="/img/ecran-tendance-vent.webp" alt="Maquette d'écran : tendance du vent sur dix minutes.">
</div>

*Maquettes d'étude, valeurs d'exemple. La définition et les polices de la série peuvent différer.*

## Les sources

Ardoise lit le **bus NMEA 2000** sur lequel elle est branchée : vitesse, cap, vent, profondeur, position. S'il y a un serveur **Signal K** à bord, elle le lit aussi, en Wi-Fi. Le téléphone règle les pages, pointe la ligne et synchronise le départ. Le compte à rebours tourne sur l'horloge de l'instrument : si la liaison tombe, il continue.

Un compas embarqué donne cap, gîte et tangage, même sans autre instrument à bord.

## Un câble

Une seule embase, au bas du tube : la dérivation du bus l'alimente et lui donne les données. Aucune autre traversée de câble, aucun bouton.

## L'endurance

Un tube d'aluminium usiné, fermé par une vitre affleurante et une plaque d'aluminium. Le pied de mât prend les paquets de mer, les UV, la chaleur d'une surface au soleil et la vibration du gréement. Les essais d'étanchéité et d'environnement seront menés, et leurs rapports publiés.

## Le service

Le micrologiciel se met à jour sans fil, par images signées. Le boîtier s'ouvre avec des outils et ses joints se remplacent : l'atelier pourra réparer chaque pièce.

## La façon

Ardoise sera faite en petite série numérotée.

Sur demande. [Prendre contact](mailto:contact@tadorne.org?subject=Ardoise)
