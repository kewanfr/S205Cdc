<img src="https://www.univ-nantes.fr/medias/photo/logotype-nantes-u-noir-72dpi_1638965800927-png?ID_FICHE=1482184" alt="Nantes Université" width="200"/>
<img src=../pictures/LOGO_PRINCIPAL_IUT_NANTES_CMJN.png alt="IUT Nantes" width="200"/>

# Mini-projet de SAE 2.5 d'année BUT1-Info 2025 (R210 etc.): APPLICATION INTELLIGENTE DE SUIVI DES RÈGLES HACCP EN CUISINE COLLECTIVE

La sécurité alimentaire est une préoccupation majeure dans les cuisines collectives, où la préparation de repas pour un grand nombre de personnes nécessite une vigilance accrue. La méthode HACCP (Hazard Analysis Critical Control Point) est une approche systématique visant à identifier, évaluer et maîtriser les dangers significatifs au regard de la sécurité des aliments. Son application rigoureuse est essentielle pour prévenir les risques sanitaires et assurer la conformité aux réglementations en vigueur.

**Contexte du projet :**

Dans le cadre d'un projet de Recherche & Développement, l'objectif est de développer une application mobile intelligente qui facilite le respect et le suivi des règles HACCP dans les cuisines collectives. Cette application devra intégrer une approche multifactorielle en prenant en compte les facteurs environnementaux (température des enceintes froides, humidité, etc.), opérationnels (respect des procédures de nettoyage, traçabilité des aliments, etc.) et comportementaux (formation du personnel, respect des protocoles, etc.). Les données seront collectées à l'aide de capteurs IoT et de questionnaires intégrés à l'application, et analysées par des algorithmes prédictifs utilisant l'Intelligence Artificielle. **L'application devra offrir aux gestionnaires de cuisine un suivi adapté grâce à une prévention personnalisée et ciblée des non-conformités, favorisant ainsi une meilleure observance des protocoles HACCP.** Elle fournira également aux autorités sanitaires des indications pour un meilleur suivi et une meilleure évaluation des pratiques en vigueur.

Dans la SAE 2.5, nous allons traiter la première partie du projet en mettant en œuvre l'ensemble du contenu de la ressource R210-GPI et en produisant un cahier des charges.

Imaginons que votre équipe (**obligatoirement 4-5 personnes**) est la première équipe de l'entreprise qui va réaliser toute l'étude et qui confiera ensuite le cahier des charges à une équipe chargée de développer un prototype (il s'agit d'un projet classique pour des étudiants de 3ème année l'an prochain en SAE5 et SAE6).

## Cas d'étude

**Contexte du projet :** 

Dans le cadre d'un projet de Recherche & Développement, l'objectif est de développer une application mobile intelligente qui facilite le respect et le suivi des règles HACCP dans les cuisines collectives. Cette application devra intégrer une approche multifactorielle en prenant en compte les facteurs environnementaux (température des enceintes froides, humidité, etc.), opérationnels (respect des procédures de nettoyage, traçabilité des aliments, etc.) et comportementaux (formation du personnel, respect des protocoles, etc.). Les données seront collectées à l'aide de capteurs IoT et de questionnaires intégrés à l'application, et analysées par des algorithmes prédictifs utilisant l'Intelligence Artificielle. L'application devra offrir aux gestionnaires de cuisine un suivi adapté grâce à une prévention personnalisée et ciblée des non-conformités, favorisant ainsi une meilleure observance des protocoles HACCP. Elle fournira également aux autorités sanitaires des indications pour un meilleur suivi et une meilleure évaluation des pratiques en vigueur.

**Description du projet :**

Ce projet se concrétisera sous la forme d'une application mobile qui devra :

Collecter des données :

* Environnementales : à l'aide de capteurs (par exemple, des dispositifs placés dans les chambres froides) pour mesurer la température, l'humidité, etc. 
* Opérationnelles : à l'aide de capteurs et de dispositifs connectés pour mesurer le respect des procédures de nettoyage, la traçabilité des aliments (via des étiquettes RFID ou des codes-barres), etc.
* Comportementales : à l'aide de questionnaires sur l'application pour collecter des données sur les pratiques du personnel, leur formation, leur respect des protocoles, etc.

À partir de ces données, l'application devra :

* Fournir un tableau de bord à la demande aux gestionnaires de la cuisine sur l'état de conformité aux règles HACCP (températures des enceintes froides, respect des procédures de nettoyage, traçabilité des aliments, etc.).
* À partir d'algorithmes d'apprentissage, établir un profil de risque de non-conformité et prévenir en amont les responsables de la cuisine.
* Alerter les responsables en cas de rupture de protocole (non-respect des procédures de nettoyage, par exemple).
* Fournir des informations et des rappels sur les bonnes pratiques d'hygiène et de sécurité alimentaire.
* Envoyer les données pertinentes aux autorités sanitaires compétentes, conformément aux réglementations en vigueur.
* Garantir le respect des règles édictées par le RGPD sur les données de santé et de sécurité alimentaire.

Cette application est un cas d'IA embarquée sur une application mobile. Plusieurs solutions sont néanmoins possibles : pas de serveurs du tout, un serveur au niveau de l’établissement, un serveur chez le prestataire. Dans tous les cas, il faut envisager : confidentialité, sécurité et respect de la règlementation nationale et européenne. Ce projet relève directement de la conception d'un dispositif de suivi des normes sanitaires. En ce sens, il doit répondre à un nombre conséquent de règles (dont le RGPD sur les données de santé) sur les dispositifs de sécurité alimentaire.

Données à collecter obligatoirement :

Vous aurez à collecter plusieurs données importantes au moyen de capteurs. En voici une première liste, que vous pourrez potentiellement compléter :

* Température des enceintes froides (réfrigérateurs, congélateurs) 
* Humidité des locaux 
* Respect des procédures de nettoyage (via des capteurs de présence ou des systèmes de validation)
* Traçabilité des aliments (via des étiquettes RFID ou des codes-barres)
* Formation et pratiques du personnel (via des questionnaires intégrés)

Réglementation HACCP et hygiène alimentaire :

* Règlement (CE) n° 852/2004 du Parlement européen et du Conseil du 29 avril 2004 relatif à l'hygiène des denrées alimentaires : https://eur-lex.europa.eu/legal-content/FR/TXT/?uri=CELEX%3A32004R0852
* Règlement (CE) n° 178/2002 du 28 janvier 2002 établissant les principes généraux de la législation alimentaire : https://eur-lex.europa.eu/legal-content/FR/TXT/?uri=CELEX%3A32002R0178
* Règles d'hygiène dans la restauration et les commerces alimentaires : https://entreprendre.service-public.fr/vosdroits/F32189
* Les principales règles d'hygiène en restauration collective : https://opti-marche.com/blog/les-principales-regles-dhygiene-en-restauration-collective/
* La restauration collective et la méthode HACCP : https://www.wikiterritorial.cnfpt.fr/xwiki/bin/view/vitrine/La%20restauration%20collective%20et%20la%20m%C3%A9thode%20HACCP/

Applications et outils pour la gestion HACCP :

* Traqfood : https://www.traqfood.com/fr/
* HACCP Facile : https://www.haccp-facile.com/
* Eezytrace : https://www.eezytrace.com/
* Wektoo : https://www.wektoo.com/wek-haccp
* Hygie HACCP : https://hygiesolution.com/telecharger-application-haccp-hygie/
* eEAT : https://eeat-haccp.io/

Autres ressources :

1. https://www.qualineo.io/post/haccp-ehpad-contre-risques-intoxications-alimentaires
2.	https://www.nelinkia.com/blog/normes/methode-haccp-restauration-collective.html
3.	https://octopus-haccp.com/normes-haccp-tout-ce-qui-et-a-savoir-sur-les-regles-dhygiene/
4.	https://impactance.fr/formations/item/143-la-methode-haccp-en-ehpad-connaitre-et-maitriser-les-dangers-alimentaires.html
5.	https://eeat-haccp.io/haccp-secteur/restauration-collective/guide-restauration-collective
6.	https://octopus-haccp.com/lhaccp-en-restauration-collective/
7.	https://agriculture.gouv.fr/restauration-quelles-obligations-en-matiere-de-formation-lhygiene-alimentaire
8.	https://agriculture.gouv.fr/guides-de-bonnes-pratiques-dhygiene-gbph
9.	https://documentation.ehesp.fr/doc_num.php?explnum_id=6875
10.	https://entreprendre.service-public.fr/vosdroits/F32189
11.	https://www.cdg76.fr/wp-content/uploads/2023/06/guide-restauration-collective-V2-2023.pdf
12.	https://www.has-sante.fr/upload/docs/application/pdf/2018-10/fiche-repere_haccp.pdf
13.	https://www.cdg60.com/wp-content/uploads/2021/04/fiche_pratique_cdg60_-_hygiene_alimentaire_-_010414_0.pdf
14.	https://octopus-haccp.com/liaison-froide-liaison-chaude/
15.	https://opti-marche.com/blog/guides-de-bonnes-pratiques-dhygiene-gbph-en-restauration-collective-pourquoi-et-comment-les-utiliser/
16.	https://www.eezytrace.com/solution-par-secteur/haccp-ehpad---restauration-securite-alimentaire-eezytrace
17.	https://www.innovorder.com/blog/haccp-restauration-collective
18.	https://www.referentiel-restauration-collective.fr/plan-maitrise-sanitaire/



## Déroulement du travail.

Le travail à réaliser ici correspond au **WP0*, le premier workpackage du projet, celui qui correspond à la rédaction du cahier des charges et plus tard à la gestion du projet.

Vous devrez mettre en oeuvre l'ensemble des techniques vues en R210 - GPI en produisant un cahier des charges. C'est un travail réalisable en **60 heures.etudiants** (à répartir entre 4-5 étudiants et dont les 2/3 seront faites pendant des créneaux avec un enseignant).
La date de rendu est le **vendredi 13 juin 2024, à 19h**.

Votre travail ne sera pas à rendre explicitement, il s'agira juste d'un dépot gitlab qui sera à utiliser pour le travail en continue, selon les bonnes pratiques de génie logiciel. L'enseignant récupérera votre travail à cette date. Même si vous faites quelque chose ensuite, il peut choisir la version qu'il évalue. Si vous avez vraiment besoin qu'il considère une version en retard, il faudra lui demander et il y aura des pénalités (comme dans tout projet industriel, à priori 1 point par jour de retard).

Vous allez utiliser les outils vues en TD (youtrack et les outils de uncloud.univ-nantes.fr : traitement de texte, tableur, diagramme, mindmap/WBS) pour faire votre étude, mais le rendu se fera dans un fichier du même type que celui que vous êtes en train de lire : au format markdown (https://support.zendesk.com/hc/fr/articles/4408846544922-Formatage-de-texte-avec-Markdown#topic_xqx_mvc_43__row_ppv_wln_1n). Il s'agit d'un langage basique pour mettre en forme du texte grâce à des caractères spéciaux (cela à l'avantage d'être du texte brut facilement versionnable avec git).

Dans les "files" du "repository", vous trouverez un dossier cahier_des_charges. S'y trouve un fichier préformé de cahier des charges, nommé *cahier_des_charges.md*. Ce sera à vous de le modifier et de le versionner dans votre propre projet gitlab une fois que vous aurez fait un fork de ce projet (comme déjà fait en TD de GPO2 : un étudiant fait le fork et ajoute les autres membres de l'équipe, le chargé de séance et M. Mottu en Maintener/Chargé de Maitnenance).

**A la fin des séances SAE2.5** Semaine 24, le dernier créneau sera consacré à une discussion avec un chargé de séance (M. Aimé ou M. El Mamouni) et M. Mottu où
- vous présenterez les résultats de votre équipe
- chacun présentera son travail personnel
- vous répondrez à des questions (des modalités vous seront données en séance).

Nous préférons mettre une note par équipe, mais nous aurons accès à votre travail individuel et nous vous questionnerons individuellement : des disparités anormales seront prises en compte. **Merci d'indiquer à la fin de votre document ce que chacun a fait avec son volume horaire**.

## Contraintes ##

Il s'agit d'un projet réel de sécurité alimentaire. Vous serez jugé sur le sérieux de votre travail, sur la qualité de votre analyse et de votre proposition. Nous ne pouvons pas vous empêcher d'utiliser des LLMs, mais il est indispensable :
* de citer les parties qui auront été réalisées avec cet outil
* de vous en servir pour apporter une réelle plus-value à votre projet
* d'apporter obligatoirement votre **plus-value humaine** à ce projet
Vous pouvez l'utiliser pour résumer des contenus ou pour avoir des idées que vous développerez ensuite dans votre projet... Utilisez-le intelligemment comme appui et non pour faire le travail à votre place. Pensez toujours à bien poser le contexte et lui donner un rôle d'expert avant de lui poser des questions. 

Vous devrez dans tous les cas maitriser ce que vous écrivez ; l'exercice oral et les questions que nous vous poserons auront pour objet de vérifier cette maîtrise.

Votre état de l'art (étude de l'existant, sur l'asthme etc.) devra **obligatoirement** être sourcé, c'est-à-dire que nous devrons avoir les références que vous aurez trouvées.

