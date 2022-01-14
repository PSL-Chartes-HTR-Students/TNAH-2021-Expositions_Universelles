# TRANSCRIPTIONS DU CONGRÈS INTERNATIONAL DES SCIENCES ETHNOGRAPHIQUES (PARIS, 1878)

Le **[Congrès international des sciences ethnographiques](http://cnum.cnam.fr/CGI/redir.cgi?8XAE243)** de 1878 a eu lieu 
à l'occasion de l'Exposition universelle de 1878, à Paris. Édité en 1881 par l'Imprimerie nationale, le compte rendu de 
ce congrès a été mis à disposition par le Conservatoire numérique des Arts et Métiers.


Ce compte rendu permet de revenir aux débuts souvent problématiques de plusieurs disciplines scientifiques : 
ethnographie, anthropologie, sociologie. Il témoigne également des développements de l'archéologie, des études du 
folklore et de la culture populaire française. Le congrès est organisé en 1878, l'année où est créé le premier musée 
ethnographique parisien. C'est une date clé dans le développement de l'anthropologie et des études sur la culture 
populaire; c'est pour cette raison que nous avons choisi de nous intéresser à cette édition du Congrès international des 
sciences ethnographiques.

---

# Répartition des retranscriptions

---

# Choix du modèle de transcription

Le document traité étant un imprimé de la fin du XIXe siècle, nous avons choisi d'utiliser le modèle *19th century prints 
- HTR catalogs*, développé dans le cadre du projet **[Artlas](https://artlas.huma-num.fr/fr/)**, dirigé par Béatrice 
Joyeux-Prunel en partenariat entre l'Université de Genève, le centre IMAGO (financé par Erasmus+), l'EUR Translitterae, 
le Labex TransferS et financé entre 2011 et 2016 par l'ANR.

---

# Choix du format XML

* Alto ou page, il va falloir se décider*

---

# Répartition des branches

Le projet faisant l'objet d'une collaboration entre cinq étudiant.e.s, l'utilisation de Git et d'un dépôt distant sur 
Github ont été nécessaires pour mener à bien le projet. Pour travailler à plusieurs sans entrer en conflit, tout en ayant 
accès aux travaux des autres, le dépôt Git a été divisé en 6 branches :
 - `main` : la branche principale, utilisée pour conserver les données du projet une fois que celui-ci a été mené à bout. 
Dans le déroulement du travail, cette branche n'a pas été utilisée, sauf à la toute fin du projet, ou le contenu de 
chaque branche a été basculée sur `main`. 
- `dev` : la branche de développement, utilisée pour tous les apports au projet 
qui ne concernaient pas le travail d'une personne en particulier, ou qui concernaient tou.te.s les membres du projet. 
C'est sur cette branche que se trouve le fichier `extraits.txt` (qui contient les références aux articles retranscrits) 
ainsi que le rapport et la documentation du projet.
 - Ensuite, les cinq branches personnelles des membres du projet, qui contiennent les exports XML des documents 
retranscrits. L'utilisation de branches personnelles permet à chaque contributeur.ice de travailler de façon autonome, 
sans que les retranscriptions de chacun.e ne se mélangent. La définition de normes (nommage des fichiers...) garantissent 
une homogénéité entre ces branches.
	- `branche_anahi` : la branche utilisée par Anahi
	- `branche_baudoin` : la branche utilisée par Baudoin
	- `branche_esteban` : la branche utilisée par Esteban
	- `branche_paul` : la branche utilisée par Paul
	- `kelly-eScriptorium` : la branche utilisée par Kelly

---

# Données produites

*une petite description de tous les fichiers produits à la bien, avec nom du producteur.ice, nom des fichiers, 
description des fichiers*

---

# Difficultés et problématiques particulières

**L'encodage des caractères spéciaux** 

L'utilisation de mots en écrits en alphabet non-latins dans les articles a posé un défi pour l’encodage. Le modèle 
eScriptorium 19th century prints ne reconnaît pas une partie importante des citations de langues étrangères dans les 
comptes rendus. Les mots en polonais, latin, allemand, et anglais ont été correctement reconnus par le modèle. En fait, 
le modèle les a reconnus avec un degré d’exactitude égal à celui dles mots de la langue principale du document, le 
français. Les langues non latines, par contre, n’étaient pas reconnues : ce sont le grec, le sanscrit, le russe, le 
persan, ainsi que les langues peu connues tel que le vieux-slave et l’avestique que les ethnologues ont appelés par leurs 
nom anciens, le paléoslave et le zend respectivement. Afin de transcrire ces langues, il fallait trouver l’unicode de 
chaque caractère spécial.

On a utilisé deux méthodes pour trouver l’unicode des caractères spéciaux pas capturés par le modèle. Parfois les auteurs 
ont cité un passage d’un texte connu, tel que l’*Iliade* d'Homère. Dans ce cas, on a vérifié notre transcription de la 
citation avec des encodages du texte déjà disponibles en ligne. Mais la plupart des caractères spéciaux étaient imprimés 
sans une citation. En outre les auteurs n’ont pas toujours précisé à laquelle langue les mots qu’ils ont invoqués 
appartiennent. Dans ce cas, on avait besoin de, en premier, reconnaître la langue et, ensuite, de rechercher l’unicode 
de chaque caractère.

Pour les caractères spéciaux en grec, qui constituent la majorité, notre équipe a profité de l’expertise de Paul Kervegan 
***(humhum ça fait bizarre non ?)***. En travaillant en équipe pour décoder un caractère spécial, on a relevé le fait que 
l’un des comptes rendus a écrit le lettre tau avec un caractère une graphie qui n'est plus en usage aujourd'hui. 
Malheureusement, faute d'avoir un unicode pour encoder ce caractère, on n’a pas pu garder le choix unique des auteurs. On 
l’a encodé avec la lettre moderne, τ, en privilégiant la lisibilité du mot.
 
Pour les caractères spéciaux en sanscrit, notre équipe a compté sur l’expertise de Christian Iyer. Il a relevé le fait 
que les comptes rendus de 1878 ont utilisé une fonte rare pour le sanscrit ; donc notre encodage ne ressemble pas 
toujours à l’imprimé. Heureusement, les auteurs ont souvent précisé le mot en sanscrit avec une translaidé à décoder la 
transcription d’une fonte peu commune. Ces problèmes relatifs aux choix de graphies dans l'imprimé original soulèvent des 
questions intéressantes vis-à-vis de l'entraînement d'un modèle d'OCR : est-il possible, ou pertinent, d'entraîner un 
modèle à reconnaître des graphies qui ne sont plus en usage aujourd'hui ? Est-ce qu'il vaut mieux privilégier une 
spécificité historique du document (l'utilisation de graphies propres au XIXe siècle) ou développer un modèle qui cherche 
à rendre les textes lisibles pour un public contemporain ?

Après le grec et le sanscrit dont les mots étaient le plus nombreux, nous avons encodé des mots en russe, en persan, en 
avestique, et le vieux-slave. Le vieux-slave a deux écritures, le glagolite et la cyrillique (1), et les auteurs ont 
utilisé le dernier. Sachant que le persan et l’avestique s’écrivent de droite à gauche, on a recherché caractère par 
caractère dans un dictionnaire. Les dictionnaires de persan, autrement connu comme le farsi, se trouvent 
facilement et l’encodage est normalisé. Faute d’un expert.e en farsi, on a vérifié notre encodage du mot هست en comptant 
sur la translitération « hest » est la traduction « il est » fournies par les ethnologues. Pour encoder l’avestique on a 
consulté la recherche de Jost Gippert, spécifiquement son article « The Encoding of Avestan — Problems and Solutions », 
qui nous a fourni l’unicode des trois caractères spéciaux du mot cité dans le compte rendu.

(1) André Vaillant, « L’Alphabet vieux-slave », Revue des études slaves 32, no. 1/4 (1955), 7-31.
(2) Jost Gippert, « The Encoding of Avestan — Problems and Solutions » Journal for Language Technology and Computational Linguistics 27, no. 2 (2012), 1-24.
