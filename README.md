# 🌦️ Conditions Climatiques — Pontcharra (Application Météo)

## Présentation générale

Application web météo complète en une seule page HTML dédiée aux prévisions détaillées pour Pontcharra (Isère, 38530), avec possibilité de changer de ville. Les données sont fournies par Météo-France (modèles AROME/ARPEGE haute résolution) via les API open-meteo.com et opendatasoft.com. L'application est conçue comme une PWA (Progressive Web App) installable, avec un thème sombre par défaut, entièrement accessible et responsive.

Développée par MIKLDOUY.

---

## 1. En-tête et identité

- Titre dynamique : "Conditions climatiques sur [Ville]"
- Sous-titre : département, code postal et mention du modèle météo utilisé (AROME haute résolution)
- Indicateur de ville actuelle affiché sous le titre
- Couleur de thème (theme-color) adaptée au mode sombre (#0b1e2d)
- Bouton "Installer l'application" flottant en haut à droite (PWA)
- Toast de notification discret en bas d'écran pour les messages système

---

## 2. Gestion des villes

### Barre de villes récentes
Historique des dernières villes consultées sous forme de chips cliquables.

### Barre de favoris
- Plusieurs villes favorites en chips (⭐ Pontcharra, ⭐ Massignieu-de-Rives, 🏠 Thollon-les-Mémises, ⭐ Carros)
- Chaque favori peut être déplacé (‹ ›), retiré (×), ou sélectionné en un clic
- Le favori actif est mis en évidence visuellement
- Bouton "+ Ajouter aux favoris"

### Modale "Changer de ville"
Deux onglets : 🔍 Rechercher (champ texte + résultats) et 📂 Parcourir par département (menus en cascade département → ville). Bouton Valider actif uniquement après sélection.

### Géolocalisation
Bouton 📍 Ma position : détecte automatiquement la position pour afficher la météo locale.

---

## 3. Barre d'outils principale

- 📍 Changer de ville
- 📍 Ma position
- 📊 Comparer des villes
- 🌕 Radar pluie
- °C / km/h (bascule unités)
- 🌙 Sombre (thème)
- ♿ Accessibilité
- 🔈 Lire la météo (synthèse vocale)
- 🔊 Alerte pluie sonore
- 🔔 Alertes activées
- 🔁 Partager le bulletin

---

## 4. Profil utilisateur

Trois profils : 👶 Enfant, 👤 Adulte, 👵 Senior. Modifie dynamiquement les recommandations d'activités et avertissements santé.

---

## 5. Bandeau de synthèse ("Points clés")

Liste à puces avec icônes : vigilance officielle, résumé conditions, écart à la normale, indice UV max, indice de chaleur, phase lunaire.

Texte narratif (💬) : résumé automatique en langage naturel de la journée avec recommandations.

---

## 6. Radar de précipitations

Carte Leaflet + tuiles RainViewer (passé 1h / prévu 30min), contrôles lecture/pause, curseur temporel, légende, bouton fermeture.

---

## 7. Cartes de prévisions journalières

7 jours, scroll horizontal : icône météo, jour/date, min/max, cumul pluie, UV coloré, lever/coucher soleil, libellé météo, mini-alerte pollen.

Navigation par jour (‹ ›) + résumé texte du jour sélectionné + narratif détaillé + bouton "Partager ce jour".

---

## 8. Indices de confort thermique

Indice de chaleur max (avec heure et niveau de risque), refroidissement éolien, note de conseils pratiques. Codes couleur : sûr/prudence/extrême/danger.

---

## 9. Pollens

Grille : 🌳 Bouleau, 🌾 Graminées, 🌿 Ambroisie, 🌿 Armoise, 🌲 Aulne, 🟢 Olivier. Niveaux nul→très élevé avec code couleur.

---

## 10. Activités recommandées

Pique-nique, jardinage, pêche, randonnée, vélo, course à pied — avec icône, avertissement contextualisé selon profil, score (Idéal/Correct/Déconseillé/Dangereux).

---

## 11. Conseils vestimentaires

Icônes + texte : ex. "Prévoyez : vêtements légers et respirants, lunettes de soleil et chapeau."

---

## 12. Conseils d'aération et de santé

Tags colorés : OUVRIR, FERMER, ATTENTION, HUMIDITÉ, UV ÉLEVÉ, AIR MOYEN/MAUVAIS, POLLEN, CHALEUR EXTRÊME PRUDENCE — chacun avec message horodaté.

---

## 13. Vigilance météorologique officielle

Niveau global coloré (vert/jaune/orange/rouge), source Météo-France, détail des phénomènes avec plages horaires (aujourd'hui/demain), lien vers vigilance.meteofrance.fr.

---

## 14. Comparatif multi-villes

Modale de sélection (jusqu'à 4 villes), tableau comparatif scrollable avec colonne ville fixée (sticky).

---

## 15. Graphiques de tendances

Deux graphiques : Température/précipitations, et Humidité/UV/qualité de l'air. Bouton "Aller à l'heure actuelle".

---

## 16. Tableau détaillé heure par heure

Colonnes : Heure, Temp., Ressenti, Pluie %, Humidité, Point de rosée, Pluie mm, Vent, Rafales, Pression, Nuages, UV, Qualité air. Codes couleur, flèches de tendance, ligne "now" surlignée.

---

## 17. Résumé collant (sticky summary)

Barre fixe en bas : icône météo, température actuelle, ville, % pluie.

---

## 18. Accessibilité

Rôles ARIA complets, aria-label détaillés, aria-pressed sur boutons à état, mode haut contraste, mode texte agrandi, focus visibles, synthèse vocale.

---

## 19. Thèmes visuels

Mode sombre par défaut (#0b1e2d→#123047), mode clair, arrière-plans dynamiques selon moment (aube/jour/crépuscule/nuit), accent bleu ciel (#4fc3f7) et jaune doré (#ffd54f).

---

## 20. Fonctionnalités techniques (PWA)

Manifest.json, bouton d'installation, cache avec indicateur d'âge, cartographie Leaflet 1.9.4, design responsive (≤600px).

---

## 21. Pied de page

"Données AROME/ARPEGE, vigilance et pollens Météo-France via open-meteo.com et opendatasoft.com · Développé par MIKLDOUY"

---

## Sources de données

- Prévisions : Open-Meteo (AROME/ARPEGE Météo-France)
- Vigilance : Météo-France (vigilance.meteofrance.fr)
- Pollens : Opendatasoft / Météo-France
- Radar : RainViewer
- Cartographie : Leaflet.js + OpenStreetMap 