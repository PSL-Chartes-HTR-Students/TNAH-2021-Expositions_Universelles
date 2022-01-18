# Guide contribution

---
# Objectifs

L’objectif de ce groupe Github est de monter un projet de transcriptions XML de sources papier. La source choisie est le 
rapport d’un congrès d’ethnologie ayant eu lieu lors de l’exposition universelle de 1878. Chaque membre doit proposer et 
travailler sur un ensemble de texte issu dudit rapport. Les textes retenus doivent faire l’objet au préalable d’un 
travail de segmentation et de transcription sur le site eScriptorium, avant d’être déposés sur Github.

# 1. Organisation de la page de dépôt Github

S’agissant d’un travail collaboratif, l’emploi de Git et d’un dépôt distant sur Github s’avèrent particulièrement 
pratique pour ce type de projet.

---

**Les branches**

Afin que le travail personnel et le rendu commun n’entrent pas en conflit et que chaque membre puisse consulter le 
travail des autres membres, le dépôt Git est divisé en plusieurs branches :

- `main` : branche principale, elle est utilisée pour conserver les données dfinitives du projet (une fois que celui-ci 
est mené à bout). Le contenu définitif de chaque branche devra être basculé sur la branche main à la fin du projet. - 
`dev` : il s’agit de la branche de développement. Elle est utilisée pour tous les apports au projet qui ne concernent pas 
le travail d'une personne en particulier, ou qui concernaient tou.te.s les membres du projet. Ainsi sur cette branche se 
trouvent des fichier tel extraits.txt (contenant les références des articles retranscrits par les membres du projet), le 
compte-rendu du projet et la documentation du projet (bibliographie, informations sur les documents traités, etc.). - 
`branches personnelles` : chaque membre du projet doit créer sa branche personnelle. Dans cette dernière, les membres 
déposent les exports XML des documents qu’ils ont retranscrits. L'utilisation de branches personnelles permet à chaque 
contributeur.ice de travailler de façon autonome, sans que les retranscriptions de chacun.e ne se mélangent. La 
définition de normes (nommage des fichiers...) garantissent une homogénéité entre ces branches. A ce jour, voici les 
branches personnelles actives :
	- `branche_anahi` : la branche utilisée par Anahi
	- `branche_baudoin` : la branche utilisée par Baudoin
	- `branche_esteban` : la branche utilisée par Esteban
	- `branche_paul` : la branche utilisée par Paul
	- `branche-kelly` : la branche utilisée par Kelly

---

**Les issues** 

Les issues permettent à chaque membre de s’exprimer et de présenter aux autres ses doutes, interrogations et suggestions 
sur l’avancement du projet.

---

**Les pull requests**

Les pull requests permettent à chaque membre de récupérer un ficher du dépôt Github et d’apporter et présenter ses 
modifications sans altérer le document original. Il peut suggérer ses modifications aux autres membres afin de décider 
ensemble d’appliquer ou non ces transformations au document original.


# 2. Travail de récupération des fichiers XML de transcriptions issus de eScriptorium

eScriptorium permet le transcription automatique de document composés de caractères latins. Le site propose différents 
modèles de transcription. Les documents traités dans ce projet étant issus d’un imprimé de la fin du XIXe siècle, le 
modèle de transcription retenu est `19th century prints - HTRCatalogs Artlas`. Il faut bien sûr vérifier que la 
segmentation et la transcription des textes soumis à eScriptorium ont été correctement effectuées et qu’elles 
correspondent bien au contenu originel. Cependant, si jamais un texte présente des caractères qui ne peuvent être 
retranscrits, les éléments problématiques peuvent être ignorés ou alors être indiqués par un `0`. Une fois transcrits, 
les fichiers doivent être exportés et téléchargés au format `ALTO` avec l’option `include image` cochée. Si vous 
appliquez correctement cela, vous devez obtenir un fichier `.zip` contenant les fichiers xml et png des textes.


# 3. Dépôts des fichiers XML et PNG sur le dépôt Github

Il est demandé à chaque membre de remplir et d’indiquer dans le fichier `extraits.txt` (pour rappel, présent dans la 
branche `dev`) les références des textes transcrits et déposés sur Github en ajoutant les numéros de page et les titres des 
articles choisis.

Afin de normaliser le contenu du dépôt Github, il est nécessaire que les fichiers xml et png de chacun soient nommés de 
la manière suivante : `PRENOM-DU-MEMBRE_Debut-du-titre-de-larticle-retranscrit_page.xml` ou 
`NOM-DU-MEMBRE_Debut-du-titre-de-larticle-retranscrit_page.png`

# 4. Finalisation du travail

Quand un membre a fini son travail personnel sur sa branche personnelle, il doit rassembler ses fichiers xml et png 
dans un dossier dont le titre est `Article_Titre_de_larticle` et le déposer sur la branche main.


# Merci à tous.tes pour vos futures contributions au projet !
