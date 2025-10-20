#  Google — Page

Reproduction simplifiée et stylisée de la page d'accueil Google avec un logo en lettres colorées.

##  Fonctionnalités

- **Logo Google coloré** - Chaque lettre avec sa couleur emblématique
- **Barre de recherche interactive** avec effets de focus
- **Design responsive** adapté mobile/desktop
- **Animations fluides** au survol des boutons
- **Interface épurée** et moderne

##  Technologies

- HTML5 sémantique
- CSS3 avec variables modernes
- Flexbox pour le layout
- Design responsive avec media queries
  
## Guide du Code
Variables CSS Principales
css
:root {
    --color-bg: #ffffff;                    /* Couleur de fond */
    --color-muted: #5f6368;                /* Texte secondaire */
    --color-border: #dfe1e5;               /* Bordures */
    --color-button-bg: #f8f9fa;            /* Fond boutons */
    --shadow: 0 1px 6px rgba(32,33,36,0.28); /* Ombre portée */
    --radius-pill: 999px;                  /* Bord arrondi pill */
}
Commandes Flexbox Importantes
css
.contain {
    display: flex;
    flex-direction: column;    /* Empilement vertical */
    align-items: center;       /* Centrage horizontal */
}

.nav {
    display: flex;
    justify-content: end;      /* Alignement à droite */
    gap: 20px;                 /* Espacement entre éléments */
}

.search-buttons {
    display: flex;
    justify-content: center;   /* Centrage horizontal */
    gap: 12px;                 /* Espace entre boutons */
}
Media Queries Responsive
css
/* Tablettes */
@media (max-width: 768px) {
    .nav {
        justify-content: center;  /* Centrage sur mobile */
        width: 100%;              /* Pleine largeur */
    }
}

/* Petits mobiles */
@media (max-width: 375px) {
    .btn {
        font-size: 0.7rem;        /* Texte plus petit */
        width: 120px;             /* Largeur réduite */
    }
}
Animations des Boutons
css
.btn {
    transition: all 0.2s ease;    /* Animation fluide */
}

.btn:hover {
    transform: translateY(-2px);  /* Effet de lévitation */
    box-shadow: 0 8px 25px rgba(0,0,0,0.2); /* Ombre accentuée */
    color: #34A853;               /* Changement couleur texte */
}
 Points Techniques Clés
1. Logo Coloré
css
.logo-text .g { color: #4285F4; }    /* Bleu Google */
.logo-text .o1 { color: #EA4335; }   /* Rouge */
.logo-text .o2 { color: #FBBC05; }   /* Jaune */
.logo-text .l { color: #34A853; }    /* Vert */
2. Barre de Recherche Interactive
css
.search-bar:focus-within {
    border: 1px solid #4285F4;           /* Bordure bleue au focus */
    box-shadow: 0 0 5px rgba(66,133,244,0.5); /* Effet glow */
}
3. Accessibilité
html
<form class="search" role="search" aria-label="Recherche Google">
<!-- Attributs ARIA pour l'accessibilité -->
 Breakpoints Responsive
Device	Breakpoint	Comportement
Desktop	≥ 768px	Layout complet
Tablette	< 768px	Navigation centrée
Mobile	< 375px	Boutons compactés
