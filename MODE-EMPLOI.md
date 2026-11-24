# Mode d'emploi — site de Kévin Marion

Site en ligne : https://kevin-marion-chef.pages.dev

Le site tient dans un seul fichier, `index.html`, avec les photos dans le dossier `images/`.
Chaque modification enregistrée sur GitHub est mise en ligne automatiquement par Cloudflare en 30 secondes environ.

---

## 1. Modifier un texte avec ChatGPT ou Gemini

1. Sur GitHub, ouvre `index.html`.
2. Clique sur l'icône **copier** (deux petits carrés, en haut à droite du fichier).
3. Colle le tout dans ChatGPT ou Gemini, suivi de ta demande (exemples plus bas).
4. Copie le fichier complet que l'IA te renvoie.
5. Retour sur GitHub, dans `index.html` : clique sur le **crayon** (Edit), sélectionne tout (Ctrl+A / Cmd+A), colle la nouvelle version.
6. Clique sur **Commit changes**, écris en une ligne ce que tu as changé, puis valide.
7. Attends 30 secondes et recharge le site.

## 2. Ajouter une photo

1. Sur GitHub, ouvre le dossier `images`.
2. Clique sur **Add file → Upload files** et dépose ta photo.
   - Nom simple, sans accents ni espaces : `plat-homard.jpg`
   - 2 Mo maximum. Une photo envoyée une fois par WhatsApp est déjà compressée.
3. Clique sur **Commit changes**.
4. Demande ensuite à l'IA de l'ajouter dans la page (exemples plus bas), puis suis l'étape 1.

## 3. Demandes prêtes à copier

Commence toujours par cette phrase, puis ajoute ta demande :

> Voici le fichier HTML de mon site. Fais uniquement la modification demandée, sans rien changer d'autre au design ni au code, et renvoie-moi le fichier COMPLET du début à la fin.

**Nouveau poste dans le parcours**
> Dans la liste du parcours (section id="parcours", liste class="postes"), ajoute en premier : année 2027, « Chef de cuisine, [NOM DU RESTAURANT] », description « [VILLE]. [une phrase] ». Garde exactement le même format que les autres lignes.

**Nouvelle photo dans la galerie**
> Dans la galerie (section id="assiettes", bloc class="rail"), ajoute en premier une figure avec l'image images/[NOM-DU-FICHIER].jpg, titre « [NOM DU PLAT] » et description « [ingrédients] », sur le même modèle que les autres figures.

**Changer une photo du diaporama du haut**
> Dans le header (bloc class="defile"), remplace l'image images/[ANCIENNE].jpg par images/[NOUVELLE].jpg.

**Modifier un texte**
> Remplace la phrase « [ancienne phrase] » par « [nouvelle phrase] ».

**Ajouter un réseau social (Instagram, LinkedIn…)**
> Dans la section contact (id="contact", bloc class="reseaux"), ajoute un bouton « Instagram » vers [LIEN], au même format que le bouton Facebook, avec une icône SVG Instagram simple.

## 4. Les règles à respecter

- **Toujours demander le fichier complet.** Avant de coller, vérifie que le texte commence par `<!doctype html>` et se termine par `</html>`. Les IA coupent parfois les longs fichiers.
- **Une modification à la fois.** Plus simple à vérifier, plus simple à annuler.
- **Ne pas toucher** aux dossiers `fonts/` ni aux fichiers `og.jpg`, `favicon.svg` et `apple-touch-icon.png`, sauf si tu sais ce que tu fais.

## 5. Si le site casse

Rien n'est jamais perdu :

1. Sur GitHub, ouvre `index.html` → clique sur **History**.
2. Ouvre la dernière version qui fonctionnait, puis clique sur **View file**, ensuite sur l'icône **copier**.
3. Recolle-la dans `index.html` (crayon → tout sélectionner → coller) → **Commit changes**.

## 6. Bon à savoir

- **Vignette de partage** (l'image qui s'affiche quand on colle le lien sur Facebook ou WhatsApp) : c'est le fichier `og.jpg`, en 1200 × 630 pixels. Après l'avoir changé, passe le lien du site dans l'outil https://developers.facebook.com/tools/debug/ et clique sur « Scrape again ».
- **Nom de domaine** : un domaine type `kevinmarion-chef.fr` coûte environ 8 €/an. Il se branche dans Cloudflare → Workers & Pages → le projet → Custom domains.

---

Site réalisé par Fenix Services.
