<img src="https://www.univ-nantes.fr/medias/photo/logotype-nantes-u-noir-72dpi_1638965800927-png?ID_FICHE=1482184" alt="Nantes Université" width="200"/>
<img src=../pictures/LOGO_PRINCIPAL_IUT_NANTES_CMJN.png alt="IUT Nantes" width="200"/>

# Mini-projet de GPO2 d'année BUT1-Info 2025 (SAE 2.5): APPLICATION INTELLIGENTE DE SUIVI DES RÈGLES HACCP EN CUISINE COLLECTIVE

La sécurité alimentaire est une préoccupation majeure dans les cuisines collectives, où la préparation de repas pour un grand nombre de personnes nécessite une vigilance accrue. La méthode HACCP (Hazard Analysis Critical Control Point) est une approche systématique visant à identifier, évaluer et maîtriser les dangers significatifs au regard de la sécurité des aliments. Son application rigoureuse est essentielle pour prévenir les risques sanitaires et assurer la conformité aux réglementations en vigueur.

**Contexte du projet :**

Dans le cadre d'un projet de Recherche & Développement, l'objectif est de développer une application mobile intelligente qui facilite le respect et le suivi des règles HACCP dans les cuisines collectives. Cette application devra intégrer une approche multifactorielle en prenant en compte les facteurs environnementaux (température des enceintes froides, humidité, etc.), opérationnels (respect des procédures de nettoyage, traçabilité des aliments, etc.) et comportementaux (formation du personnel, respect des protocoles, etc.). Les données seront collectées à l'aide de capteurs IoT et de questionnaires intégrés à l'application, et analysées par des algorithmes prédictifs utilisant l'Intelligence Artificielle. **L'application devra offrir aux gestionnaires de cuisine un suivi adapté grâce à une prévention personnalisée et ciblée des non-conformités, favorisant ainsi une meilleure observance des protocoles HACCP.** Elle fournira également aux autorités sanitaires des indications pour un meilleur suivi et une meilleure évaluation des pratiques en vigueur.

Dans la SAE 2.5, nous allons traiter la première partie du projet en mettant en œuvre l'ensemble du contenu de la ressource R210-GPI et en produisant un cahier des charges.

Imaginons que votre équipe (**obligatoirement 4-5 personnes**) est la première équipe de l'entreprise qui va réaliser toute l'étude et qui confiera ensuite le cahier des charges à une équipe chargée de développer un prototype (il s'agit d'un projet classique pour des étudiants de 3ème année l'an prochain en SAE5 et SAE6).

## Cas d'étude

**Contexte du projet :** 

Dans le cadre d'un projet de Recherche & Développement, l'objectif est de développer une application mobile intelligente qui facilite le respect et le suivi des règles HACCP dans les cuisines collectives. Cette application devra intégrer une approche multifactorielle en prenant en compte les facteurs environnementaux (température des enceintes froides, humidité, etc.), opérationnels (respect des procédures de nettoyage, traçabilité des aliments, etc.) et comportementaux (formation du personnel, respect des protocoles, etc.). Les données seront collectées à l'aide de capteurs IoT et de questionnaires intégrés à l'application, et analysées par des algorithmes prédictifs utilisant l'Intelligence Artificielle. L'application devra offrir aux gestionnaires de cuisine un suivi adapté grâce à une prévention personnalisée et ciblée des non-conformités, favorisant ainsi une meilleure observance des protocoles HACCP. Elle fournira également aux autorités sanitaires des indications pour un meilleur suivi et une meilleure évaluation des pratiques en vigueur.


## Déroulement du travail.

Le travail à réaliser ici correspond au **WP0*, le premier workpackage du projet, celui qui correspond à la rédaction du cahier des charges et plus tard à la gestion du projet.

Vous devrez mettre en oeuvre l'ensemble des techniques vues en GPI en produisant un cahier des charges. C'est un travail réalisable en **60 heures.etudiants** (à répartir entre 4-5 étudiants et dont les 2/3 seront faites pendant des créneaux avec un enseignant).
La date de rendu est le **vendredi 13 juin 2024, à 19h**.

Votre travail sera à rendre dans gitlab, l'enseignant récupérera votre travail à cette date. Même si vous faites quelque chose ensuite, il peut choisir la version qu'il évalue. Si vous avez vraiment besoin qu'il considère une version en retard, il faudra lui demander et il y aura des pénalités (comme dans tout projet industriel, à priori 1 point par jour de retard).

Nous préférons mettre une note par équipe, mais nous aurons accès à votre travail individuel et des disparités anormales seront prises en compte. **Merci d'indiquer à la fin de votre document ce que chacun a fait avec son volume horaire**.

Vous allez utiliser les outils vues en TD (youtrack et les outils de uncloud.univ-nantes.fr : traitement de texte, tableur, diagramme, mindmap/WBS) pour faire votre étude, mais le rendu se fera dans un fichier du même type que celui que vous êtes en train de lire : au format markdown (https://support.zendesk.com/hc/fr/articles/4408846544922-Formatage-de-texte-avec-Markdown#topic_xqx_mvc_43__row_ppv_wln_1n). Il s'agit d'un langage basique pour mettre en forme du texte grâce à des caractères spéciaux (cela à l'avantage d'être du texte brut facilement versionnable avec git).

Dans les "files" du "repository", vous trouverez un dossier cahier_des_charges. S'y trouve un fichier préformé de cahier des charges, nommé *cahier_des_charges.md*. Ce sera à vous de le modifier et de le versionner dans votre propre projet gitlab une fois que vous aurez fait un fork de ce projet (comme déjà fait en TD de GPO2 : un étudiant fait le fork et ajoute les autres membres de l'équipe, le chargé de séance et M. Mottu en Maintener/Chargé de Maitnenance).

**A la fin des séances SAE** Semaine 25, le dernier créneau sera consacré à une discussion avec votre chagé de séance et M. Mottu où
- vous présenterez les résultats de votre équipe
- chacun présentera son travail personnel
- vous répondrez à des questions (des modalités vous seront données en séance).

## Contraintes ##

Il s'agit d'un projet réel de sécurité alimentaire. Vous serez jugé sur le sérieux de votre travail, sur la qualité de votre analyse et de votre proposition. Nous ne pouvons pas vous empêcher d'utiliser des LLMs, mais il est indispensable :
* de citer les parties qui auront été réalisées avec cet outil
* de vous en servir pour apporter une réelle plus-value à votre projet
* d'apporter obligatoirement votre **plus-value humaine** à ce projet
Vous pouvez l'utiliser pour résumer des contenus ou pour avoir des idées que vous développerez ensuite dans votre projet... Utilisez-le intelligemment comme appui et non pour faire le travail à votre place. Pensez toujours à bien poser le contexte et lui donner un rôle d'expert avant de lui poser des questions. 

Vous devrez dans tous les cas maitriser ce que vous écrivez ; l'exercice oral et les questions que nous vous poserons auront pour objet de vérifier cette maîtrise.

Votre état de l'art (étude de l'existant, sur l'asthme etc.) devra **obligatoirement** être sourcé, c'est-à-dire que nous devrons avoir les références que vous aurez trouvées.

La note finale sera individuelle.
