<h1 align="center">
<br>
  <img src="https://raw.githubusercontent.com/thedaviddias/Front-End-Checklist/master/src/img/banners/logo-front-end-checklist.jpg" alt="Front-End Checklist" width="170">
  <br>
    <br>
  Front-End Checklist [traduction FR]
  <br>
</h1>

<h4 align="center">La Checklist Front-End est une liste exhaustive de tous les élements dont vous avez besoin avant de lancer votre site HTML en production.</h4>

<p align="center">
  <a href="http://makeapullrequest.com">
    <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square" alt="PRs Welcome">
  </a>
  <a href="https://gitpod.io/#https://github.com/thedaviddias/Front-End-Checklist">
  <img src="https://img.shields.io/badge/Gitpod-Ready--to--Code-blue?logo=gitpod" alt="Gitpod Ready-to-Code">
  </a>
    <a href="https://github.com/thedaviddias/Front-End-Checklist/graphs/contributors">
    <img src="https://img.shields.io/github/contributors/thedaviddias/Front-End-Checklist.svg?style=flat-square" alt="Contributors">
  </a>
  <a href="https://spectrum.chat/front-end-checklist">
    <img src="https://img.shields.io/badge/chat-on_spectrum-4837E2.svg?style=flat-square" alt="Spectrum">
  </a>
      <a href="https://github.com/thedaviddias/Front-End-Checklist/">
    <img src="https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg?style=flat-square" alt="Front‑End_Checklist followed">
</a>
    <a href="https://creativecommons.org/publicdomain/zero/1.0/">
    <img src="https://img.shields.io/badge/license-CC0-green.svg?style=flat-square" alt="CC0">
  </a>
</p>

<p align="center">
  <a href="#comment-lutiliser">Comment utiliser</a> • <a href="#contribuer">Contribuer</a> • <a href="https://frontendchecklist.io">Site Web [EN]</a> • <a href="https://www.producthunt.com/posts/front-end-checklist">Product Hunt</a>
</p>
<p align="center">
    <span>Autres Checklists:</span>
    <br>
  <a href="https://github.com/thedaviddias/Front-End-Performance-Checklist#---------front-end-performance-checklist-">🎮 Front-End Performance Checklist [EN]</a> • <a href="https://github.com/thedaviddias/Front-End-Design-Checklist#front-end-design-checklist">💎 Front-End Design Checklist [EN]</a>
</p>

Celle-ci est basée sur des années d'experience de développeurs Front-End, en y ajoutant divers checklists de projets open-source.

## Table des matières

1. **[Head](#head)**
2. **[HTML](#html)**
3. **[Webfonts](#webfonts)**
4. **[CSS](#css)**
5. **[Images](#images)**
6. **[JavaScript](#javascript)**
7. **[Securité](#securité)**
8. **[Performance](#performance-1)**
9. **[Accessibilité](#accessibilité)**
10. **[SEO](#seo)**
11. **[Traductions](#traduction)**

---

## Comment l'utiliser ?

Tous les élements de la **Front-End Checklist** sont requis dans la majorité de vos projets, mais certains peuvent être omis ou ne sont pas essentiels (par exemple, dans le cas d'une application d'administration, vous n'avez pas besoin de flux RSS). Nous avons choisi d'utiliser 3 niveaux de flexibilité:

* ![Bas][low_img] signifie que l'élement est **recommandé** mais peut être omis dans certaines situations.
* ![Moyen][medium_img] signifie que l'élement est **hautement recommandé** et peut éventuellement être omis dans certains cas particuliers. Certains élements, s'ils sont omis, peuvent avoir des mauvais effets secondaires en terme de performance ou de référencement (SEO).
* ![Haut][high_img] signifie que l'élement **est indispensable**. Vous pouvez provoquer des dysfonctionnements dans votre page, ou avoir des problèmes d'accessibilité, voir de SEO. La priorité des tests doit d'abord s'assurer de ces éléments en premier.

Plusieurs resources possèdent un emoticon pour vous aider à comprendre quel type de contenu il s'agit :

* 📖: documentation ou article
* 🛠: outil online  / outil de test
* 📹: media ou contenu vidéo

---

## Head

> **Notes:** Vous pouvez trouver [une liste de toute les balises](https://github.com/joshbuchea/HEAD) qui peuvent être trouvées dans la section  `<head>` d'un document HTML.

### Meta tag

* [ ] **Doctype:** ![Haut][high_img] Le Doctype en HTML5 doit être en haut de toutes vos pages HTML.

```html
<!-- Doctype HTML5 -->
<!doctype html>
```

> * 📖 [Determiner l'encodage - HTML5 W3C (en)](https://www.w3.org/TR/html5/syntax.html#determining-the-character-encoding)

*Les prochains 2 meta tags (Charset et Viewport) doivent venir en premier dans le head.*

* [ ] **Charset:** ![Haut][high_img] Le charset (UTF-8) est correctement declaré.

```html
<!-- Set character encoding for the document -->
<meta charset="utf-8">
```

* [ ] **Viewport:** ![Haut][high_img] Le viewport est correctement déclaré.

```html
<!-- Viewport for responsive web design -->
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
```

* [ ] **Title:** ![Haut][high_img] Un titre est utilisé sur chaque page (SEO: Google calcule la largeur des pixels de chaque caractères utilisés dans le titre, et coupe entre 472 et 482 pixels. La limite moyenne de caractères se situe autour des 55).

```html
<!-- Document Title -->
<title>Page Title less than 55 characters</title>
```

> * 📖 [Title - HTML - MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Element/title)
> * 🛠 [SERP Snippet Generator (en)](https://www.sistrix.com/serp-snippet-generator/)

* [ ] **Description:** ![Haut][high_img] Une meta description est fournie, elle est unique et ne contient pas plus de 150 caractères.

```html
<!-- Meta Description -->
<meta name="description" content="Description of the page less than 150 characters">
```

> * 📖[Meta Description - HTML - MDN](https://developer.mozilla.org/fr/docs/Apprendre/HTML/Introduction_%C3%A0_HTML/The_head_metadata_in_HTML#Ajouter_le_nom_de_lauteur_et_une_description)

* [ ] **Favicons:** ![Moyen][medium_img] Chaque favicon a été créé et s'affiche correctement. Si vous avez un `favicon.ico`, posez le à la racine de votre site. Normalement vous n'avez pas besoin d'utiliser de balise. Cependant, cela reste une bonne pratique de le relier comme dans l'exemple ci-dessous. Aujourd'hui, **Le PNG est recommandé** en remplacement du format `.ico` (dimensions: 32x32px).

```html
<!-- Standard favicon -->
<link rel="icon" type="image/x-icon" href="https://example.com/favicon.ico">
<!-- Recommended favicon format -->
<link rel="icon" type="image/png" href="https://example.com/favicon.png">
```

> * 🛠 [Favicon Generator (en)](https://www.favicon-generator.org/)
> * 🛠 [RealFaviconGenerator (en)](https://realfavicongenerator.net/)
> * 📖 [Favicon Cheat Sheet (en)](https://github.com/audreyr/favicon-cheat-sheet)
> * 📖 [Favicons, Touch Icons, Tile Icons, etc. Which Do You Need? - CSS Tricks (en)](https://css-tricks.com/favicon-quiz/)
> * 📖 [PNG favicons - caniuse (en)](https://caniuse.com/#feat=link-icon-png)

* [ ] **Apple Web App Meta:** ![Bas][low_img] Les meta-tags spécifiques à Apple sont présents.*

```html
<!-- Apple Touch Icon (at least 200x200px) -->
<link rel="apple-touch-icon" href="/custom-icon.png">

<!-- To run web application in full-screen -->
<meta name="apple-mobile-web-app-capable" content="yes">

<!-- Status Bar Style (see Supported Meta Tags below for available values) -->
<!-- Has no effect unless you have the previous meta tag -->
<meta name="apple-mobile-web-app-status-bar-style" content="black">
```

> * 📖 [Configurer des Web Applications (en)](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)
> * 📖 [Supported Meta Tags (en)](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariHTMLRef/Articles/MetaTags.html)

- [ ] **Windows Tiles:**![Bas][low_img] Les tuiles Windows sont présentes et liées.

```html
<!-- Microsoft Tiles -->
<meta name="msapplication-config" content="browserconfig.xml" />
```

Le balisage xml minimum requis pour le balisage du fichier `browserconfig.xml` doit être:

```xml
<?xml version="1.0" encoding="utf-8"?>
<browserconfig>
   <msapplication>
     <tile>
        <square70x70logo src="small.png"/>
        <square150x150logo src="medium.png"/>
        <wide310x150logo src="wide.png"/>
        <square310x310logo src="large.png"/>
     </tile>
   </msapplication>
</browserconfig>
```

> * 📖 [Browser configuration schema reference (en)](https://msdn.microsoft.com/en-us/library/dn320426(v=vs.85).aspx)

* [ ] **Canonical:** ![Moyen][medium_img] Utiliser `rel="canonical"` pour éviter le contenu dupliqué.

```html
<!-- Helps prevent duplicate content issues -->
<link rel="canonical" href="http://example.com/2017/09/a-new-article-to-red.html">
```

> * 📖 [Use canonical URLs - Search Console Help - Google Support (en)](https://support.google.com/webmasters/answer/139066?hl=en)
> * 📖 [5 common mistakes with rel=canonical - Google Webmaster Blog (en)](https://webmasters.googleblog.com/2013/04/5-common-mistakes-with-relcanonical.html)

### HTML tags

* [ ] **Language attribute:** ![Haute][high_img] L'attribut `lang` de votre site est spécifié et indique le langage de la page courante.

```html
<html lang="fr">
```

* [ ] **L'attribut direction :** ![Moyen][medium_img] Le sens de lecture est specifié dans le tag html (Il peut être indiqué dans un autre élément HTML).

```html
<html dir="rtl">
```

> * 📖 [dir - HTML - MDN](https://developer.mozilla.org/fr/docs/Web/HTML/Attributs_universels/dir)

* [ ] **Alternate language:** ![Low][low_img] Un lien vers la traduction de la page courante est spécifié.

```html
<link rel="alternate" href="https://es.example.com/" hreflang="es">
```

* [ ] **Commentaire conditionel:** ![Low][low_img] Les commentaires conditionnels sont présents pour IE si besoin.

> * 📖 [About conditional comments (Internet Explorer) - MSDN - Microsoft (en)](https://msdn.microsoft.com/en-us/library/ms537512(v=vs.85).aspx)

* [ ] **Flux RSS:** ![Bas][low_img] Si votre projet est un blog ou possède des articles, un flux RSS est fourni.

* [ ] **Inline critical CSS:** ![Moyen][medium_img] Les CSS des contenus qui doivent être immédiatement visibles pendant le chargement ("au dessus de la ligne de flottaison") sont appelés "CSS critiques". Ils sont inclus avant le CSS principal et entre les balises `<style></style>` dans une seule ligne (en étant minifié).

> * 🛠 [Critical by Addy Osmani on GitHub (en)](https://github.com/addyosmani/critical) automatise cela.

* [ ] **Ordre des CSS :** ![Haute][high_img] Tous les fichiers CSS sont chargés avant n'importe quel fichier JavaScript dans la section `<head>`. (Parfois certains fichiers JS sont chargés en asynchrone en haut de page, et font donc exception à la règle).

### Social meta

Visualisez et générez automatiquement vos meta pour réseaux sociaux avec [Meta Tags](https://metatags.io/)

***Facebook OG*** et ***Twitter Cards*** sont pour tous les sites, hautement recommandés. Les autres tags de média sociaux peuvent être utiles si vous ciblez une audience particulère et que vous voulez vous assurer un affichage particulier.

* [ ] **Facebook Open Graph:** ![Low][low_img] Tous les Open Graph Facebook (OG) sont testés et aucun ne manque ou contient de fausses informations. Les images doivent être au minimum de 600 x 315 pixels, mais 1200 x 630 pixels est recommandé.

> **Notes:** L'utilisation des balises `og:image:width` et `og:image:height` qui spécifient les dimensions des images au crawler permettent le rendu des images immédiatement sans avoir besoin de les redimensionner avec un système asynchrone.

```html
<meta property="og:type" content="website">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:title" content="Content Title">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:description" content="Description Here">
<meta property="og:site_name" content="Site Name">
<meta property="og:locale" content="en_US">
<!-- Next tags are optional but recommended -->
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
```

> * 📖 [Guide du partage pour les Webmasters](https://developers.facebook.com/docs/sharing/webmasters/)
> * 📖 [Bonnes pratiques du partage](https://developers.facebook.com/docs/sharing/best-practices/)
> * 🛠 Tester votre page avec [Facebook OG testing (en)](https://developers.facebook.com/tools/debug/)

* [ ] **Twitter Card:** ![Low][low_img]

```html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Content Title">
<meta name="twitter:description" content="Content description less than 200 characters">
<meta name="twitter:image" content="https://example.com/image.jpg">
```

> * 📖 [Getting started with cards — Twitter Developers (en)](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/guides/getting-started)
> * 🛠 Tester votre page avec [Twitter card validator](https://cards-dev.twitter.com/validator)

**[⬆ Retour en haut](#table-des-matières)**

---

## HTML

### Bonnes pratiques

* [ ] **HTML5 Semantic Elements:** ![Haut][high_img] Les élements sémantiques HTML5 ont une utilisation spécifique (header, section, footer, main...).

> * 📖 [HTML Reference (en)](http://htmlreference.io/)

* [ ] **Error pages:** ![Haut][high_img] Les pages d'erreurs 404 et 5xx existent. Rappelez vous que les pages d'erreurs 5xx ont besoin de CSS intégrés (pas d'appel externe au serveur courant).

* [ ] **Noopener:** ![Moyen][medium_img] Dans le cas ou vous utilisez des liens externes avec `target="_blank"`, votre lien devrait avoir l'attribut `rel="noopener"` pour prévenir du tab nabbing (piratage par onglet). Si vous devez supporter les anciennes versions de Firefox, utiliser alors `rel="noopener noreferrer"`.

> * 📖 [A propos de rel=noopener (en)](https://mathiasbynens.github.io/rel-noopener/)

* [ ] **Nettoyage de commentaires:** ![Bas][low_img] Le code non nécessaire doit être supprimé avant l'envoi en production.

### HTML testing

* [ ] **W3C compliant:** ![Haut][high_img] Toutes les pages doivent avoir passé la validation W3C pour identifier de possibles problèmes dans le code HTML.

> * 🛠 [W3C validator](https://validator.w3.org/)

* [ ] **HTML Lint:** ![Haut][high_img] Utiliser ces outils pour vous aider à analyser des problèmes que vous auriez dans votre code HTML.

> * 🛠 [Dirty markup (en)](https://www.10bestdesign.com/dirtymarkup/)

> * 🛠 [webhint](https://webhint.io/)

* [ ] **Link checker:** ![Haut][high_img] Vérification qu'il n'y ai pas de liens brisés (pages 404).

> * 🛠 [W3C Link Checker](https://validator.w3.org/checklink)

* [ ] **Adblockers test:** ![Moyen][medium_img] Votre site doit affiché un contenu correct malgré la présence d'adblocker (Vous pouvez fournir un message pour encourager les gens à les désactiver).

> * 📖 [Utiliser AdBlockers en environnement de développement (en)](https://andreicioara.com/use-adblocking-in-your-dev-environment-48db500d9b86)

**[⬆ Retour en haut](#table-des-matières)**

---

## Webfonts

> **Notes:** Utiliser les webfonts peut causer des problèmes de textes invisibles/non stylisés le temps du chargement de la fonte - envisager d'avoir des polices de secours et / ou d'utiliser des chargeurs webfont pour contrôler le comportement.
> * 📖 [Google Technical considerations about webfonts (en)](https://developers.google.com/fonts/docs/technical_considerations)

* [ ] **Webfont format:** ![Haut][high_img] WOFF, WOFF2 et TTF sont tous supportés par les navigateurs modernes.

> * 📖 [WOFF - Web Open Font Format - Caniuse](https://caniuse.com/#feat=woff).
> * 📖 [WOFF 2.0 - Web Open Font Format - Caniuse](https://caniuse.com/#feat=woff2).
> * 📖 [TTF/OTF - TrueType and OpenType font support](https://caniuse.com/#feat=ttf)
> * 📖 [Using @font-face - CSS-Tricks (en)](https://css-tricks.com/snippets/css/using-font-face/)

* [ ] **Webfont size:** ![Haut][high_img] La taille des Webfonts ne doit pas excéder 2 MB (toutes les variantes incluses).

* [ ] **Webfont loader:** ![Bas][low_img] Controler le comportement du chargement avec un loader de webfont.

> * 🛠 [Typekit Web Font Loader](https://github.com/typekit/webfontloader)

**[⬆ retour en haut](#table-des-matières)**

---

## CSS

> **Notes:** Regardez les [guidelines CSS (en)](https://cssguidelin.es/) et les [Guidelines Sass (en)](https://sass-guidelin.es/) suivis par de nombreux développeurs Front-End. Si vous avez des doutes sur des propriétés CSS, vous pouvez visiter la [Reference CSS (en)](http://cssreference.io/). Il y a aussi ce court [Guide](http://codeguide.co/) pour la cohérence.

* [ ] **Responsive Web Design:** ![Haut][high_img] Le site utilise un design responsive.
* [ ] **CSS Print:** ![Moyen][medium_img] Une feuille d'impression CSS est incluse et permet une impression correcte sur chacune des pages.
* [ ] **Preprocessors:** ![Bas][low_img] L'utilisation d'un preprocessor CSS ([Sass](http://sass-lang.com/), [Less](http://lesscss.org/) ou [Stylus](http://stylus-lang.com/)) est conseillée).
* [ ] **Unique ID:** ![Haut][high_img] Si des IDs sont utilisés, ils sont uniques sur chaque page.
* [ ] **Reset CSS:** ![Haut][high_img] Un CSS reset (reset, normalize ou reboot) est utilisé et mis à jour. *(Si vous utiliser un  Framework CSS comme Bootstrap ou Foundation, une feuille Normalize est déjà incluse.)*

> * 📖 [Reset.css](https://meyerweb.com/eric/tools/css/reset/)
> * 📖 [Normalize.css](https://necolas.github.io/normalize.css/)
> * 📖 [Reboot](https://getbootstrap.com/docs/4.0/content/reboot/)

* [ ] **JS prefix:** ![Bas][low_img] Toutes les classes (ou les IDs) utilisés dans les fichiers JavaScript commencent par **js-** et ne sont pas stylés dans les fichiers CSS.

```html
<div id="js-slider" class="my-slider">
<!-- Or -->
<div id="id-used-by-cms" class="js-slider my-slider">
```

* [ ] **Embedded ou inline CSS:** ![Haut][high_img] Tous les CSS embarqués dans des balises `<style>` ou utilisant le CSS en ligne (attribut `style`) le sont uniquement pour de bonnes raisons (background-image pour des sliders, ou CSS critiques).
* [ ] **Vendor prefixes:** ![Haut][high_img] les préfixes CSS sont utilisés et générés en fonction des navigateurs que vous ciblez.

> * 🛠 [Autoprefixer CSS online](https://autoprefixer.github.io/)

### Performance

- [ ] **Concatenation:** ![Haut][high_img] Les fichiers CSS sont concatenés dans un fichier unique. *(Pas besoin pour HTTP/2)*
- [ ] **Minification:** ![Haut][high_img] Les fichiers CSS sont minifiés.
- [ ] **Non-blocking:** ![Moyen][medium_img] Les fichiers CSS ne doivent pas être bloquants pour que le DOM puisse se charger rapidement.

> * 📖 [loadCSS by filament group (en)](https://github.com/filamentgroup/loadCSS)
> * 📖 [Example of preload CSS using loadCSS (en)](https://gist.github.com/thedaviddias/c24763b82b9991e53928e66a0bafc9bf)

- [ ] **CSS non utilisés:** ![Bas][low_img] Supprimer les CSS inutilisés.

> * 🛠 [UnCSS Online](https://uncss-online.com/)
> * 🛠 [PurifyCSS](https://github.com/purifycss/purifycss)
> * 🛠 [PurgeCSS](https://github.com/FullHuman/purgecss)
> * 🛠 [Chrome DevTools Coverage](https://developers.google.com/web/updates/2017/04/devtools-release-notes#coverage)

### CSS testing

* [ ] **Stylelint:** ![Haut][high_img] Tous les fichiers CSS ou SCSS ne doivent pas avoir une seule erreur.

> * 🛠 [stylelint, a CSS linter (en)](https://stylelint.io/)
> * 📖 [Sass guidelines (en)](https://sass-guidelin.es/)

* [ ] **Responsive web design:** ![Haut][high_img] Toutes les pages ont étés testées sur les résolutions suivantes: 320px, 768px, 1024px (peut être plus / d'autres en fonction de vos statistiques de visites).

* [ ] **CSS Validator:** ![Moyen][medium_img] Le CSS a été testé et il n'y a aucune erreur.

> * 🛠 [CSS Validator](https://jigsaw.w3.org/css-validator/)

* [ ] **Desktop Browsers:** ![Haut][high_img] Toutes les pages ont étés testées sur différents navigateurs (Safari, Firefox, Chrome, Internet Explorer, EDGE...).
* [ ] **Mobile Browsers:**  ![Haut][high_img] Toutes les pages ont étés testées sur différents navigateurs mobiles (Native browser, Chrome, Safari...).
* [ ] **OS:**  ![Haut][high_img] Toutes les pages ont étés testées sur différents OS (Windows, Android, iOS, Mac...).

- [ ] **Pixel perfect:** ![Haut][high_img] Les pages collent parfaitement au pixel près aux maquettes. Cela dépend de la qualité qu'on vous a fourni. Vous ne pourrez pas forcément avoir 100% en précision, mais cela doit ressembler le plus possible.

> [Pixel Perfect - Chrome Extension](https://chrome.google.com/webstore/detail/perfectpixel-by-welldonec/dkaagdgjmgdmbnecmcefdhjekcoceebi?hl=en)

* [ ] **Reading direction:** ![Haut][high_img] Les pages ont étés testées dans les 2 sens de lecture si les 2 sont supportés (gauche à droite et droite à gauche).

> * 📖 [Building RTL-Aware Web Apps & Websites: Part 1 - Mozilla Hacks (en)](https://hacks.mozilla.org/2015/09/building-rtl-aware-web-apps-and-websites-part-1/)
> * 📖 [Building RTL-Aware Web Apps & Websites: Part 2 - Mozilla Hacks (en)](https://hacks.mozilla.org/2015/10/building-rtl-aware-web-apps-websites-part-2/)

**[⬆ retour en haut](#table-des-matières)**

---

## Images

> **Notes:** Pour une complète compréhension de l'optimisation des images, lisez ce livre gratuit **[Essential Image Optimization (en)](https://images.guide/)** d'Addy Osmani.

### Bonnes pratiques

* [ ] **Optimisation:** ![Haut][high_img]Toutes les images sont optimisées pour un rendu sur navigateur. Le format WebP peut être utilisé pour des pages critiques (comme la page d'accueil).

> * 🛠 [Imagemin (en)](https://github.com/imagemin/imagemin)
> * 🛠 Utiliser [ImageOptim (en)](https://imageoptim.com/) pour optimiser gratuitement vos images.
> * 🛠 Utiliser [KeyCDN Image Processing (en)](https://www.keycdn.com/support/image-processing) pour optimiser les images en temps réel.
> * 🛠 Utiliser [Kraken.io (en)](https://kraken.io/web-interface) une alternative incroyable pour des optimisations sur des png et des jpg. Jusqu'à 1 Mb en version gratuite.
> * 🛠 [TinyPNG (en)](https://tinypng.com/) optimise les PNG, PNG animés ey jpg sans perte. Il existe des intégrations gratuites et payantes.
> * 🛠 [ZorroSVG (en)](http://quasimondo.com/ZorroSVG/) PNG transparents pour le poids d'un JPG grace à l'utilisation de masking svg.
> * 🛠 [SVGO (en)](https://github.com/svg/svgo) outils basé sur Node.js pour optimiser les SVG.
> * 🛠 [SVGOMG](https://jakearchibald.github.io/svgomg/) interface graphique web pour utiliser SVGO directement depuis le web.

* [ ] **Picture/Srcset:** ![Moyen][medium_img] Vous pouvez utiliser des éléments HTML `picture` / l'attribut `srcset` pour fournir l'image la plus appropriée à la résolution de l'utilisateur.

> * 📖 [Comment constuire des images responsives avec srcset (en)](https://www.sitepoint.com/how-to-build-responsive-images-with-srcset/)

* [ ] **Retina:** ![Bas][low_img] Vous fournissez des layout d'images 2x or 3x, pour l'affichage sur un support retina.
* [ ] **Sprite:** ![Moyen][medium_img] Les petites images sont dans un seul fichier sprite (dans le cas d'icones, elles peuvent être dans un sprite d'image SVG).
* [ ] **Width and Height:** ![Haut][high_img] Ajouter les attributs `width` et `height` sur la balise `<img>` si la taille est connue (peut être omis pour le dimensionnement par CSS).
* [ ] **Text alternatif:** ![Haut][high_img] Toute les balises `<img>` ont un texte alternatif qui décrit l'image visuellement.

> * 📖 [Alt-texts: The Ultimate Guide (en)](https://axesslab.com/alt-texts/)

* [ ] **Lazy loading:** ![Medium][medium_img] Les images sont chargées au fur et à mesure (Un noscript fallback est toujours fourni).

**[⬆ retour en haut](#table-des-matières)**

---

## JavaScript

### Bonnes pratiques

* [ ] **JavaScript Inline:** ![Haute][high_img] Vous n'avez aucun code javascript inline (contenu dans votre code HTML).
* [ ] **Concatenation:** ![Haute][high_img] Les fichiers JavaScript sont concatenés.
* [ ] **Minification:** ![Haute][high_img] Les fichiers JavaScript sont minifiés (vous pouvez ajouiter le suffixe `.min`).

> * 📖 [Minification des Ressources (HTML, CSS, and JavaScript) (en)](https://developers.google.com/speed/docs/insights/MinifyResources)

* [ ] **Securité JavaScript:**

> * 📖 [Guidelines for Developing Secure Applications Utilizing JavaScript (en)](https://www.owasp.org/index.php/DOM_based_XSS_Prevention_Cheat_Sheet#Guidelines_for_Developing_Secure_Applications_Utilizing_JavaScript)

* [ ] **`noscript` tag:** ![Medium][medium_img]  Utiliser l'élément `<noscript>` dans le body HTML dans le cas d'un script non supporté ou si le JS est désactivé dans le navigateur. Cela peut s'avérer utile dans le cas de Single Page Applications basés sur React par exemple, voir ces [exemples](https://webdesign.tutsplus.com/tutorials/quick-tip-dont-forget-the-noscript-element--cms-25498).

```html
<noscript>
  Vous devez activer JavaScript pour pouvoir utiliser ce site internet.
</noscript>
```

* [ ] **Non-blocking:** ![Moyen][medium_img] Les fichiers JavaScript sont chargés en asynchrone avec `async` ou avec l'utilisation de l'attribut `defer`.

> * 📖 [Remove Render-Blocking JavaScript (en)](https://developers.google.com/speed/docs/insights/BlockingJS)

* [ ] **Optimized and updated JS libraries:** ![Medium][medium_img] Toutes les librairies JavaScripts utilisées dans votre projets le sont par nécessité (préférer du Vanilla JS pour des fonctionnalités simples), à jour de leurs dernières versions et ne surchargent pas votre JavaScript de méthodes inutiles.

> * 📖 [You may not need jQuery (en)](http://youmightnotneedjquery.com/)
> * 📖 [Vanilla JavaScript pour construire des applications web puissantes (en)](https://plainjs.com/)

* [ ] **Modernizr:** ![Bas][low_img] Si vous avez besoin de fonctionnalités spécifiques, vous pouvez utiliser un Modernizr personnalisé pour ajouter les classes au tag `<html>`.

> * 🛠 [Personnaliser votre Modernizr](https://modernizr.com/download?setclasses)

### Tester le JavaScript

* [ ] **ESLint:** ![Haut][high_img] Pas d'erreurs détéctés par ESLint (basé sur votre configuration ou sur les règles standards).

> * 📖 [ESLint - The pluggable linting utility for JavaScript and JSX (en)](https://eslint.org/)

**[⬆ retour en haut](#table-des-matières)**

---

## Securité

### Scan et vérification de votre site web

> * [securityheaders.io (en)](https://securityheaders.io/)
> * [Observatory by Mozilla (en)](https://observatory.mozilla.org/)

### Bonnes pratiques

* [ ] **HTTPS:** ![Moyen][medium_img] HTTPS est utilisé sur chaque page et sur tous vos contenus externes (plugins, images...).

> * 🛠 [Let's Encrypt - Free SSL/TLS Certificates](https://letsencrypt.org/fr/)
> * 🛠 [Free SSL Server Test (en)](https://www.ssllabs.com/ssltest/index.html)
> * 📖 [Strict Transport Security](http://caniuse.com/#feat=stricttransportsecurity)

* [ ] **HTTP Strict Transport Security (HSTS):** ![Moyen][medium_img] L'entête HTTP est définie à 'Strict-Transport-Security'.

> * 🛠 [Check HSTS preload status and eligibility (en)](https://hstspreload.org/)
> * 📖 [HTTP Strict Transport Security Cheat Sheet - OWASP](https://www.owasp.org/index.php/HTTP_Strict_Transport_Security_Cheat_Sheet)
> * 📖 [Transport Layer Protection Cheat Sheet - OWASP](https://www.owasp.org/index.php/Transport_Layer_Protection_Cheat_Sheet)

* [ ] **Cross Site Request Forgery (CSRF):** ![High][high_img] Vous êtes sure que vos requêtes faites coté serveur sont légitimes et proviennent de votre site / app pour éviter les attaques CSRF.

> * 📖 [Cross-Site Request Forgery (CSRF) Prevention Cheat Sheet  - OWASP](https://www.owasp.org/index.php/Cross-Site_Request_Forgery_(CSRF)_Prevention_Cheat_Sheet)

* [ ] **Cross Site Scripting (XSS):** ![High][high_img] Votre page ou site est dégagé des problèmes XSS possibles.

> * 📖 [XSS (Cross Site Scripting) Prevention Cheat Sheet  - OWASP](https://www.owasp.org/index.php/XSS_(Cross_Site_Scripting)_Prevention_Cheat_Sheet)
> * 📖 [DOM based XSS Prevention Cheat Sheet  - OWASP](https://www.owasp.org/index.php/DOM_based_XSS_Prevention_Cheat_Sheet)

* [ ] **Content Type Options** ![Moyen][medium_img] Empêcher Google Chrome et Internet Explorer d'essayer de mime-sniff le type de contenu d'une réponse différente de celle déclarée par le serveur.

> * 📖 [X-Content-Type-Options - Scott Helme (en)](https://scotthelme.co.uk/hardening-your-http-response-headers/#x-content-type-options)

* [ ] **X-Frame-Options (XFO)** ![Moyen][medium_img] Protéger vos visiteurs contre les attaques par clickjacking.

> * 📖 [X-Frame-Options - Scott Helme (en)](https://scotthelme.co.uk/hardening-your-http-response-headers/#x-frame-options)
> * 📖 [RFC7034 - HTTP Header Field X-Frame-Options (en)](https://tools.ietf.org/html/rfc7034)

* [ ] **Content Security Policy** ![Moyen][medium_img] Definir comment le contenu est chargé sur votre site et d'où il est autorisé à être chargé. Cela peut aussi vous permettre de vous protéger des attaques par clickjacking.

> * 📖 [Content Security Policy - An Introduction - Scott Helme (en)](https://scotthelme.co.uk/content-security-policy-an-introduction/)
> * 📖 [CSP Cheat Sheet - Scott Helme (en)](https://scotthelme.co.uk/csp-cheat-sheet/)
> * 📖 [CSP Cheat Sheet - OWASP (en)](https://www.owasp.org/index.php/Content_Security_Policy_Cheat_Sheet)
> * 📖 [Content Security Policy Reference (en)](https://content-security-policy.com/)

**[⬆ retour en haut](#table-des-matières)**

---

## Performance

### Bonnes pratiques

- [ ] **Objectifs à atteindre:** ![Medium][medium_img] Vos pages doivents atteindre ces objectifs :
  - First Meaningful Paint en moins d'1 seconde
  - Time To Interactive en dessous de 5 secondes pour la configuration "moyenne" (Android a 200€ sur un réseau 3G avec un RTT (round-trip time) de 400ms et 400kbps de bande passante) et en dessous de 2 secondes pour les visites suivantes
  - Taille totale des fichiers critiques en dessous de 170Kb gzippé

> * 🛠 [Website Page Analysis (en)](https://tools.pingdom.com)
> * 🛠 [WebPageTest (en)](https://www.webpagetest.org/)
> * 📖 [Size Limit: Make the Web lighter (en)](https://evilmartians.com/chronicles/size-limit-make-the-web-lighter)

- [ ] **Minified:** ![Moyen][medium_img] Votre HTML est minifié.

* [ ] **Lazy loading:** ![Moyen][medium_img] Images, scripts et CSS doivent être chargé en lazy loading pour améliorer le temps de  réponse (Voir les details dans une autre section).

* [ ] **Cookie size:** Si vous utilisez des cookies, assurez vous que chaque cookie ne dépasse pas 4096 octets et qu'il n'y en ai pas plus de 20 pour votre nom de domaine.

> * 📖 [Cookie specification: RFC 6265 (en)](https://tools.ietf.org/html/rfc6265)
> * 📖 [Cookies](https://developer.mozilla.org/fr/docs/Web/HTTP/Cookies)
> * 🛠 [Browser Cookie Limits (en)](http://browsercookielimits.squawky.net/)

* [ ] **Composants tiers:** ![Moyen][medium_img] Les éléments tiers comme les iframes ou les composants basés sur des JS externes (comme les boutons de partage) sont remplacés par des composants statiques quand c'est possible, pour limiter les appels aux APIs externes et préservez l'activité de vos visiteurs confidentielle.

> * 🛠 [Simple sharing buttons generator (en)](https://simplesharingbuttons.com/)

### Préparer les requêtes à venir

> * 📖 [Expliquation des techniques suivantes](https://css-tricks.com/prefetching-preloading-prebrowsing/)

* [ ] **DNS resolution:** ![Bas][low_img] Les composants tiers chargés depuis des DNS sont résolus à l'avance pendant les temps morts en utilisant `dns-prefetch`.

```html
<link rel="dns-prefetch" href="https://example.com">
```

* [ ] **Preconnection:** ![Bas][low_img] DNS lookup, TCP handshake et la neéociation TLS avec services permettent de gagner du temps en utilisant `preconnect`.

```html
<link rel="preconnect" href="https://example.com">
```

* [ ] **Prefetching:** ![Low][low_img] Les ressources qui seront chargées bientôt dans la page (généralement les images en lazy loading) sont requêtées à l'avance durant les temps morts en utilisant `prefetch`.

```html
<link rel="prefetch" href="image.png">
```

* [ ] **Preloading:** ![Low][low_img] Les resources nécessaires à la page courante (ex: scripts placés en bas du tag `<body>`) sont chargés en avance avec `preload`.

```html
<link rel="preload" href="app.js">
```

> * 📖 [Différences entre prefetch et preload (en)](https://medium.com/reloading/preload-prefetch-and-priorities-in-chrome-776165961bbf)

### Tester la Performance

* [ ] **Google PageSpeed:** ![Haut][high_img] Toutes vos pages ont étés testées (pas seulement la page d'accueil) et ont un score au moins de 90/100.

> * 🛠 [Google PageSpeed (en)](https://developers.google.com/speed/pagespeed/insights/)
> * 🛠 [Tester votre vitesse mobile avec Google](https://www.thinkwithgoogle.com/intl/fr-fr/feature/testmysite/)
> * 🛠 [WebPagetest - Website Performance and Optimization Test (en)](https://www.webpagetest.org/)
> * 🛠 [GTmetrix - Website speed and performance optimization (en)](https://gtmetrix.com/)
> * 🛠 [Speedrank - Improve the performance of your website (en)](https://speedrank.app/)

**[⬆ retour en haut](#table-des-matières)**

---

## Accessibilité

> **Notes:** Vous pouvez regader la playlist [A11ycasts with Rob Dodson (en)](https://www.youtube.com/playlist?list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g) 📹

### Bonnes pratiques

- [ ] **Progressive enhancement:** ![Moyen][medium_img] Les fonctionnalités importantes comme la navigation et la recherche doivent pouvoir fonctionner avec le JavaScript désactivé.

> * 📖 [Activer / désactiver le JavaScript dans l'outil Chrome Developer (en)](https://www.youtube.com/watch?v=kBmvq2cE0D8)

- [ ] **Contraste des couleurs:** ![Moyen][medium_img] Le contraste des couleurs doit être au pire WCAG AA (AAA pour le mobile).

> * 🛠 [Contrast ratio](https://leaverou.github.io/contrast-ratio/)

#### Headings

* [ ] **H1:** ![Haut][high_img] Toutes les pages ont un H1 qui n'est pas le titre du site.
* [ ] **Headings:** ![Haut][high_img] Les balises Hn doivent être correctement utilisées et dans le bon ordre (H1 à H6).

> * 📹 [Why headings and landmarks are so important -- A11ycasts #18 (en)](https://www.youtube.com/watch?v=vAAzdi1xuUY&index=9&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)

### Sémantique

- [ ] **Specific HTML5 input types are used:** ![Moyen][medium_img] C'est assez important pour les périphériques mobiles de personnaliser les keypads et autres widgets pour améliorer l'ergonomie.

> * 📖 [Mobile Input Types](http://mobileinputtypes.com/)

### Formulaire

* [ ] **Label:** ![Haut][high_img] Un label est associé avec chaque élement de formulaire. Dans le cas ou un label ne peut être affiché, utiliser `aria-label` à la place.

> * 📖 [Utiliser l'attribut aria-label - MDN](https://developer.mozilla.org/fr/docs/Accessibilit%C3%A9/ARIA/Techniques_ARIA/Utiliser_l_attribut_aria-label)

### Tester l'accessibilité

* [ ] **Test des standards d'accessibilité:** ![High][high_img] Utiliser l'outil WAVE pour vous assurer de respecter les standards d'accessibilité.

> * 🛠 [Wave testing (en)](http://wave.webaim.org/)

* [ ] **Navigation par clavier:** ![Haut][high_img] Tester votre site en utilisant uniquement votre clavier dans un ordre prévisible. Tous les élements doivent être accessibles et utilisables.
* [ ] **Screen-reader:** ![Medium][medium_img] Toutes les pages ont étés testées dans un outil de lecture d'écran (VoiceOver, ChromeVox, NVDA or Lynx).
* [ ] **Focus style:** ![High][high_img] Si le focus est désactivé, il est remplacé par un état visible en CSS.

> * 📹 [Managing Focus - A11ycasts #22 (en)](https://www.youtube.com/watch?v=srLRSQg6Jgg&index=5&list=PLNYkxOF6rcICWx0C9LVWWVqvHlYJyqw7g)

**[⬆ retour en haut](#table-des-matières)**

---

## SEO

* [ ] **Google Analytics:** ![Haut][high_img] Google Analytics est installé et correctement configuré.

> * 🛠 [Google Analytics](https://analytics.google.com/analytics/web/)
> * 🛠 [GA Checker (and others) (en)](http://www.gachecker.com/)

* [ ] **Headings logic:** ![Moyen][medium_img] Le texte d'entête aide à comprendre le contenu de la page courante.

> * 🛠 [Tota11y, tab Headings (en)](http://khan.github.io/tota11y/#Try-it)

* [ ] **sitemap.xml:** ![Haut][high_img] Un sitemap.xml existe et a été envoyé à Google Search Console (historiquement Google Webmaster Tools).

> * 🛠 [Sitemap generator (en)](https://websiteseochecker.com/html-sitemap-generator/)

* [ ] **robots.txt:** ![Haut][high_img] Le robots.txt ne bloque pas l'indexation des pages.

> * 📖 [The robots.txt file (en)](https://varvy.com/robottxt.html)
> * 🛠 Tester votre robots.txt avec [Google Robots Testing Tool](https://www.google.com/webmasters/tools/robots-testing-tool)

* [ ] **Structured Data:** ![Haut][high_img] Les pages utilisant des données structurées ont étés testés et n'ont pas d'erreurs. Les données structurées aident les crawlers à comprendre le contenu de votre page.

> * 📖 [Introduction aux données structurées - Search - Google Developers](https://developers.google.com/search/docs/guides/intro-structured-data)
> * 📖 [RDFa - Linked Data in HTML (en)](https://rdfa.info/)
> * 📖 [JSON-LD (en)](https://json-ld.org/)
> * 📖 [Microdata (en)](https://www.w3.org/TR/microdata/)
> * 🛠 Tester votre page avec [Structured Data Testing Tool](https://developers.google.com/structured-data/testing-tool/)
> * 🛠 Liste complete du vocabulaire utilisé dans les données structurées. [Schema.org Full Heirarchy](http://schema.org/docs/full.html)

* [ ] **Sitemap HTML:** ![Moyen][medium_img] Un sitemap HTML est fourni et accessible via un lien dans le pied de page de votre site.

> * 📖 [Sitemap guidelines - Google Support](https://support.google.com/webmasters/answer/183668?hl=fr)

* [ ] **Pagination link tags:** ![Medium][medium_img] Ajoutez `rel="prev"` et `rel="next"` pour indiquer le contenu paginé.

> * 🛠 [Pagination (rel="prev/next") Testing Tool (en)](https://technicalseo.com/seo-tools/rel-prev-next/)

> * 📖 [Pagination guidelines - Google Support](https://support.google.com/webmasters/answer/1663744?hl=en)

```html
<!-- Example: Pagination link tags for page 2 of a paginated list -->
<link rel="prev" href="https://example.com/?page=1">
<link rel="next" href="https://example.com/?page=3">
```

**[⬆ retour en haut](#table-des-matières)**

---

## Traduction

La Checklist Front-End est aussi disponible dans d'autres langues. Merci aux traducteurs et à leur travail !

* 🇯🇵 Japanese: [miya0001/Front-End-Checklist](https://github.com/miya0001/Front-End-Checklist)
* 🇪🇸 Spanish: [eoasakura/Front-End-Checklist-ES](https://github.com/eoasakura/Front-End-Checklist-ES)
* 🇨🇳 Chinese: [JohnsenZhou/Front-End-Checklist](https://github.com/JohnsenZhou/Front-End-Checklist)
* 🇰🇷 Korean: [kesuskim/Front-End-Checklist](https://github.com/kesuskim/Front-End-Checklist)
* 🇧🇷 Portuguese: [jcezarms/Front-End-Checklist](https://github.com/jcezarms/Front-End-Checklist)
* 🇻🇳 Vietnamese: [euclid1990/Front-End-Checklist](https://github.com/euclid1990/Front-End-Checklist)
* 🇹🇼 Traditional Chinese: [EngineLin/Front-End-Checklist](https://github.com/EngineLin/Front-End-Checklist)
* 🇫🇷 French: [ynizon/Front-End-Checklist](https://github.com/ynizon/Front-End-Checklist)
* 🇷🇺 Russian: [ungear/Front-End-Checklist](https://github.com/ungear/Front-End-Checklist)
* 🇹🇷 Turkish: [eraycetinay/Front-End-Checklist](https://github.com/eraycetinay/Front-End-Checklist)
* 🇩🇪 German: [xfuture603/Front-End-Checklist](https://github.com/xFuture603/Front-End-Checklist)

---

## Le badge Front-End Checklist

Si vous voulez montrer que vous suivez les règles de la  Checklist Front-End, posez ce badge sur votre fichier README!

➔ [![Front‑End_Checklist followed](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)

```md
[![Front‑End_Checklist followed](https://img.shields.io/badge/Front‑End_Checklist-followed-brightgreen.svg)](https://github.com/thedaviddias/Front-End-Checklist/)
```

**[⬆ retour en haut](#table-des-matières)**

---

## Contribuer

**Ouvrez une demande de correction ou de suggestion pour faire une modification ou un ajout.**

### Contributeurs

Voici la liste des contributeurs sur le repo officiel Anglais.

[contributeurs](https://github.com/thedaviddias/frontendchecklist/graphs/contributors).

## Support

Si vous avez des questions ou des suggestions, n'hesitez pas à interpeller l'auteur original (en Anglais) sur Gitter ou Twitter:

* [Chat sur Gitter](https://gitter.im/Front-End-Checklist/Lobby?utm_source=share-link&utm_medium=link&utm_campaign=share-link)
* [Facebook](https://www.facebook.com/frontendchecklist/)
* [Twitter](https://twitter.com/thedaviddias)

## Auteur original

**[David Dias](https://github.com/thedaviddias/Front-End-Checklist)**

## Contributeurs

Ce projet existe grâce à toutes les personnes qui y contribuent. [[Contribuer]](.github/CONTRIBUTING.md).
<a href="https://github.com/thedaviddias/Front-End-Checklist/graphs/contributors"><img src="https://opencollective.com/front-end-checklist/contributors.svg?width=890" /></a>

## Backers

Merci à tous les backers! 🙏 [[Devenir un backer](https://opencollective.com/front-end-checklist#backer)]

<a href="https://opencollective.com/front-end-checklist#backers" target="_blank"><img src="https://opencollective.com/front-end-checklist/backers.svg?width=890"></a>

## Sponsors

Supportez ce projet en devenant un sponsor. Votre logo sera affiché ici avec un lien vers votre site web. [[Devenir un sponsor](https://opencollective.com/front-end-checklist#sponsor)]

<a href="https://opencollective.com/front-end-checklist/sponsor/0/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/0/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/1/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/1/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/2/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/2/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/3/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/3/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/4/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/4/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/5/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/5/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/6/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/6/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/7/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/7/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/8/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/8/avatar.svg"></a>
<a href="https://opencollective.com/front-end-checklist/sponsor/9/website" target="_blank"><img src="https://opencollective.com/front-end-checklist/sponsor/9/avatar.svg"></a>

## License

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

**[⬆ Retour en haut](#table-des-matières)**

[low_img]: http://res.cloudinary.com/djnyaloac/image/upload/v1508238836/level-checklist-low.png
[medium_img]: http://res.cloudinary.com/djnyaloac/image/upload/v1508238836/level-checklist-medium.png
[high_img]: http://res.cloudinary.com/djnyaloac/image/upload/v1508238836/level-checklist-high.png
