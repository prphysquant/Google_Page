# Google — Page - Mon Travail expliqué !

## Description
Reproduction responsive de la page d'accueil Google avec logo typographique coloré et formulaire de recherche accessible.

# Commandes CSS Essentielles Expliquées

# Layout et Positionnement
display: flex;
Explication : Crée un conteneur flexible qui permet un alignement facile des éléments enfants.
Utilisation dans le projet :

css
.contain {
    display: flex;
    flex-direction: column;
    align-items: center;
}
Centre verticalement tous les éléments de la page

justify-content et align-items
Explication :

justify-content : Aligne horizontalement (axe principal)

align-items : Aligne verticalement (axe secondaire)
Utilisation :

css
.nav {
    justify-content: end;      /* Aligne à droite */
    align-items: end;          /* Aligne en bas */
}
gap: 20px;
Explication : Crée un espacement entre les éléments enfants sans utiliser de margins.
Avantage : Plus simple et plus propre que margin individuel.

 Styles Visuels Importants
border-radius: 999px;
Explication : Crée des bords parfaitement arrondis (forme "pill").
Utilisation : Barre de recherche et boutons

css
.search-bar {
    border-radius: 999px;  /* Forme ovale parfaite */
}
:focus-within
Explication : S'applique quand un enfant de l'élément reçoit le focus.
Utilisation : Style de la barre de recherche quand l'input est focus

css
.search-bar:focus-within {
    border-color: #4285F4;
    box-shadow: 0 0 5px rgba(66,133,244,0.5);
}
transition: all 0.2s ease;
Explication : Anime les changements de style sur 0.2 seconde avec acceleration douce.
Utilisation : Effets de hover fluides sur les boutons

 Responsive Design
@media (max-width: 768px)
Explication : Applique des styles seulement quand l'écran fait moins de 768px de large.
Utilisation : Adaptation mobile

css
@media (max-width: 768px) {
    .nav {
        justify-content: center;  /* Centre la nav sur mobile */
    }
}
transform: translateY(-2px);
Explication : Déplace l'élément de 2 pixels vers le haut.
Utilisation : Effet de "lévitation" au survol

css
.btn:hover {
    transform: translateY(-2px);  /* Bouton qui se soulève */
}

## Expliquation du Formulaire de Recherche
html
<form class="search" role="search" aria-label="Recherche Google" onsubmit="return false;">
    <div class="search-bar">
        <input type="text" id="search" class="search-input" placeholder="🔍 Search" autocomplete="off">
    </div>
</form>
Commande	Définition	Utilité
role="search"	Attribut ARIA définissant le rôle	Accessibilité pour lecteurs d'écran
aria-label="Recherche Google"	Étiquette descriptive	Contexte pour technologies d'assistance
onsubmit="return false;"	Bloque l'envoi du formulaire	Évite le rechargement en version statique
autocomplete="off"	Désactive l'auto-complétion	UX propre sans historique navigateur
placeholder="🔍 Search"	Texte indicatif	Guide l'utilisateur avec icône

Design System
Variables CSS
css
:root {
    --color-bg: #ffffff;
    --color-text: #202124;
    --color-border: #dfe1e5;
    --shadow: 0 1px 6px rgba(32,33,36,0.28);
    --radius-pill: 999px;
}

 Responsive Design
Breakpoints
≥ 768px : Layout desktop

< 768px : Adaptation tablette

< 375px : Version mobile compacte
https://prphysquant.github.io/Google_Page/
