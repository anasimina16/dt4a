# \#4 - Le GTFS

## Définition

### Signification

GTFS signifie General Transit Feed Specification \(spécification générale pour les flux relatifs aux transports en commun\). C'est un standard informatique permettant de communiquer des horaires de **transports en commun** et les informations géographiques associées \(topographie d'un réseau : emplacement des arrêts, tracé des lignes\). 

On produit un fichier GTFS pour partager les informations à propos des transports en commun à des développeurs, qui ensuite viennent intégrer ces informations dans leurs applications. Les flux GTFS peuvent être utilisés pour alimenter des **calculateurs d'itinéraires,** des éditeurs d'horaires et diverses applications.

### Historique

Le GTFS a été conçu par Bibiana McHugh, responsable des systèmes d'information chez TriMet, l'autorité organisatrice des transports urbains de [**Portland**](https://fr.wikipedia.org/wiki/Portland_%28Oregon%29) \(Oregon\). En 2005, de retour de voyage, elle était frustrée de ne pouvoir accéder aux informations relatives au transport en commun via MapQuest et donc être incapable de planifier un itinéraire en bus aussi simplement qu'en voiture. Elle a donc envoyé des demandes de renseignements à Mapquest, Yahoo! et Google, leur demandant s'il était prévu d’incorporer des données TC dans leurs services de cartographie et si TriMet pourrait s’associer à cette entreprise. Sur les trois, **seul Google a répondu**. 

En fait, l’ingénieur Google Chris Harrelson utilisait déjà 20% de son temps à interfacer les données du transport en commun pour Google Maps \(ce qui donnera naissance plus tard à Google Transit\). Voila comment TriMet a travaillé avec Google pour préparer le jeu de données de Portland dans un format qui fonctionnerait pour Google Maps. C'était donc un standard « tiré par les utilisateurs des TC » et non pas pas une instance de normalisation. C'était une première. Une première compliquée, car les techniciens ont rapidement compris qu'il était très difficile de lier les éléments temporels et spatiaux, et qu'il faudrait créer une base de données relationnelle pour gérer cela. 

**Google Transit a été lancé le 7 décembre 2005.** La première année, TriMet était la seule agence disponible sur Google Maps. En septembre 2006, [cinq autres villes ont](https://translate.googleusercontent.com/translate_c?depth=1&rurl=translate.google.fr&sl=en&sp=nmt4&tl=fr&u=http://googleblog.blogspot.com/2006/09/happy-trails-with-google-transit.html&xid=17259,15700021,15700186,15700191,15700248&usg=ALkJrhhp6DNu6cPdoWYkaobzCxITlGhhXw) été intégrées : Eugene \(OR\), Honolulu \(HI\), Pittsburgh \(PA\), Seattle \(WA\) et Tampa \(FL\). Aujourd'hui, on décompterait plus de 500 agences utilisant le GTFS à travers le monde. 

### Composition

Un flux GTFS se compose de **plusieurs fichiers texte** \(6 obligatoires et 7 optionnels\) rassemblés dans un fichier ZIP. Chaque fichier modélise un aspect spécifique des informations de transports en commun : arrêts, itinéraires, trajets et autres informations liées aux horaires. Les détails de chaque fichier sont définis dans la [référence GTFS](https://developers.google.com/transit/gtfs/reference/?hl=fr). Vous trouverez un modèle de flux dans les [exemples GTFS](https://developers.google.com/transit/gtfs/examples/?hl=fr). 

### Le temps réel

Fournir aux utilisateurs des mises à jour en temps réel \(départs, arrivées, incidents...\) sur les transports en commun améliore de façon significative le confort d'utilisation du service. Par exemple, si un retard est annoncé, l'usager peut retarder le départ de son domicile. Voilà pourquoi, au delà de GTFS statiques, a progressivement été développée le **standard GTFS-realtime**. C'est une spécification de flux permettant aux agences de transports en commun de fournir aux développeurs d'applications des mises à jour en temps réel sur leur flotte. Il s'agit d'une extension de GTFS. La spécification est éditée sous la [licence Apache 2.0](http://www.apache.org/licenses/LICENSE-2.0.html).

## Enjeux

### Pourquoi choisir le GTFS ?

Le standard GTFS offre un format simple, permettant de décrire les éléments essentiels d’une offre de transport principalement en vue d’une diffusion sur Google Maps ou d’une réutilisation par les développeurs d’applications connexes. Il est très approprié pour des **besoins simples d’information** voyageur comme des applications smartphones. Aujourd'hui, c’est le format le plus utilisé pour des publications **OpenData** en transport.

### Ce standard n'existe que pour les transports en commun ?

Une réflexion, portée notamment par la North Americain Bikeshare Association, vise à promouvoir la création d'un standard "**GBFS**". Elle est soutenue par des propriétaires et des exploitants de systèmes de vélos en libre-service, tant publics que privés, des développeurs d'applications et des fournisseurs de technologies. GBFS est conçue comme une spécification pour les données en temps réel. Elle est plutôt orientée "usagers". Le détail des réflexions est disponible sur Github [ici](https://github.com/NABSA/gbfs/blob/master/gbfs.md).

Un second standard semble également émerger avec la montée en puissance des micromobilités, il s'agit du **MDS** : Mobility Data Specification. Il est quant à lui plutôt orienté "agences" ou "AOT". Le détail des réflexions est disponible sur Github [ici.](https://github.com/CityOfLosAngeles/mobility-data-specification)

### Quelles améliorations prévues ? 

Le GTFS est loin d'être parfait, et de nombreux acteurs du transport travaillent à son amélioration au quotidien. Notons par exemple l'initiative du Rocky Mountain Institute, qui incube le projet **MobilityData**. Son objectif est à l'échelle mondiale d'améliorer les données horaires des transport en commun, en temps réel. Sa feuille de route est la suivante : 

* Gérer un communauté autour du GTFS, 
* Rendre le GTFS plus clair notamment via un [guide des meilleures pratiques](https://gtfs.org/best-practices/?depth=1&rurl=translate.google.fr&sl=en&sp=nmt4&tl=fr&u=https://gtfs.org/best-practices/&xid=17259,15700021,15700186,15700191,15700248&usg=ALkJrhiZfJQ4erl3gWdlIYQWT8GA_oyMpA),
* Ajouter des fonctionnalités à GTFS pour décrire davantage de services et fonctionnalités :
  * Transport à la demande \[[GTFS-flex](https://translate.googleusercontent.com/translate_c?depth=1&rurl=translate.google.fr&sl=en&sp=nmt4&tl=fr&u=http://bit.ly/gtfs-drt&xid=17259,15700021,15700186,15700191,15700248&usg=ALkJrhi73KZdNESXMCQJ_rXr_TOD_z0Vyw)\]
  * Modifications de service imprévues, telles que des détours ou des navettes de remplacement. \[[GTFS-ServiceChanges](https://translate.googleusercontent.com/translate_c?depth=1&rurl=translate.google.fr&sl=en&sp=nmt4&tl=fr&u=http://bit.ly/gtfs-service-changes&xid=17259,15700021,15700186,15700191,15700248&usg=ALkJrhg7nwJLd-1J8Y9_8TZJDI184j6y_Q)\]
  * Caractéristiques des véhicules et des points d'arrêts pour les PMR \[[GTFS et véhicules GTFS](https://translate.googleusercontent.com/translate_c?depth=1&rurl=translate.google.fr&sl=en&sp=nmt4&tl=fr&u=http://bit.ly/gtfs-vehicles&xid=17259,15700021,15700186,15700191,15700248&usg=ALkJrhi03ikE9sCD5CX48YGljUcs7BLSwQ)\]
  * Structures tarifaires,
  * Lignes, services, et noms d'opérateurs \(branding\)
* Faciliter la recherche sur les données de transports, notamment:
  *  Avantages de l'information en temps réel
  *  Bibliothèques de données de transports et outils
  *  Pratiques de données à travers le monde

### Quel lien avec le Netex ? 

**NeTEx est une norme européenne**, basée sur le modèle de référence Transmodel, élaborée \(par des pros, pour des pros!\) dans le but **d’échanger** de façon formalisée des données de transport couvrant tous les domaines : topologie, gestion des lieux d’arrêt, information voyageur, gestion des équipements, tarification, planning. Elle est composée de 3 parties :

* format d’échange des éléments topologiques
* format d’échange des horaires
* format d’échange des informations tarifaires

Les parties 1 et 2 sont le cœur de NeTEx et décrivent **de façon détaillée** les éléments topologiques du réseau et les services associés comme les services disponibles aux arrêts et les éléments d’accessibilité. **Très complète**, la norme NeTEx est principalement utilisée par les professionnels du transport pour l’échange de données à travers différents systèmes d’information : systèmes d’information voyageur multimodal, systèmes billettiques, systèmes d’aide à l’exploitation, etc.

## Cas d'usage

Le GTFS est approximativement utilisé par 500 "agences" dans le monde. Une liste, qui se veut exhaustive est disponible ici : 

{% embed url="http://transitfeeds.com/feeds" %}

## Parole d'acteur

_Leo Frachet a été durant près de 5 ans "Public Transit Data Specialist" chez Transit, une application d'information voyageurs dont le siège est basé à Montréal. Il est désormais_ [_T_](https://www.linkedin.com/company/20826/)_echnical Co-Director, MobilityData au Rocky Mountain Institute._

> **Pourquoi le GTFS est aujourd'hui le format/standard le plus utilisé dans le monde ?** 
>
> A la base, le GTFS a été créé pour être utilisé de manière très simple dans un planificateur de trajets, Google Maps. C'était donc très attirant pour les différentes agences de transports américaines, là ou a été créé ce standard. Le format du GTFS est simple, et un fichier peut être écrit à la main pour une petite agence, il est très tolérant pour les producteurs. Voila pourquoi il a connu un succès important et un développement très rapide à l'échelle américaine puis mondiale \(il est difficile de dire dans combien de villes exactement\).

> **Le  GTFS répond-il à tous les besoins, est-il suffisamment complet ?** 
>
> Le GTFS répond aux besoins de Google Maps, car il a été pensé pour le planificateur de trajets. Il est particulièrement adapté à des offres simples, comme par exemple les transports informels, ou les offres de bus monomodales. Mais pour aller plus loin, des réflexions sont en cours pour améliorer la description des lieux \(sous terrain, entrée de métro...\), les transports à la demande, les modifications de dernier moment \(situation d'urgence, remplacement d'une rame, suppression d'un train...\) et enfin la tarification. Par ailleurs, de nombreuses agences  sont structurées, utilisent majoritairement le GTFS et sont motivées pour répondre à des besoins nouveaux. 
>
> **Et l'intermodalité ?** 
>
> On parle beaucoup en ce moment du GBFS, qui permet d'améliorer la gestion des données issues des vélos, vélos en libre service, mais aussi services en libre service en règle générale. Le MDS, développé à Los Angeles permettrait quand à lui d'améliorer la remontée de données depuis les offres en free floating vers les agences. Ces deux standards sont inspirés du GTFS dans leur écriture, et viennent le compléter dans une optique multi/intermodale. L'idée à terme serait de créer des passerelles entre GBFS, GTFS, MDS...

> **Quels sont les principaux défis de ce standard ?**

> Continuer à être amélioré progressivement, sur de nombreux aspects. Pour cela, l'accès gratuit et facilité aux spécifications est une chance. D'ailleurs, cela permet à de très nombreux étudiants, en GIS notamment, de pouvoir réaliser des tests et de la R/D gratuitement.
>
> Une autre chance pour le GTFS, au delà de son caractère gratuit et ouvert, il permet de faire supporter la charge du calcul au consommateur de données. Le producteur n'a qu'à fournir la donnée, mais les algorithmes sont gérés par l'intégrateur et le fournisseur de l'application. C'est un élément très important et crucial pour l'exploitation au quotidien des planificateurs, notamment par des petites agences.

> **En Afrique ?** 
>
> Des réflexions sont lancées pour améliorer la prise en charge du transport informel, notamment sur les temps d'attente \(quand par exemple les véhicules sont remplis, et que l'on doit en attendre un ou plusieurs autres\). Une extension qui permettrait de modéliser cela est à l'étude.

## DigitalTransport4Africa

Pourquoi mettre en avant le GTFS dans le cadre du projet DigitalTransport4Africa ? 

Tout d'abord, pour le caractère **universel** de ce standard. Le projet DigitalTransport4Africa veut promouvoir une vision des transports à grande échelle, qui dépasse les frontières d’un pays, et bientôt pourquoi pas d’un continent. Ainsi, il devient primordial de travailler sur un standard international, connu dans de nombreux pays. 

Pour sa **simplicité** d’utilisation. Le GTFS est un standard à la base mis au point par une agence de transports et un industriel \(Google\). Il a donc été créé dans un objectif de simplicité, d’uniformisation et de partage. Cela en fait un format parfait pour améliorer les informations concernant les transports en commun dans le cadre de notre projet, d’autant plus pour des systèmes de transports « informels ». 

Enfin, le GTFS étant le plus répandu dans le monde entier, de **nombreux outils** \(notamment en Open Source\) ont été développés afin de créer, analyser, modifier, publier des fichiers GTFS. Ces outils peuvent être mis à disposition de différentes agences / autorités de transports ou encore d’exploitants de réseaux de transports. 

## Exercice pratique ! 

De nombreux tutoriaux expliquent comment créer puis publier des GTFS. Nous avons repris l'exemple de \#Datactivist. L'équipe a produit un tutoriel [dans le cadre du projet **Data Transport Mali**](http://doc.digitaltransport.io/data-transport-mali-GTFS/Valider%20et%20corriger%20les%20donn%C3%A9es/contexte/le-projet-data-transport-mali-a-la-source-de-la-documentation.html), et s'appuie ainsi sur un exemple réel qui a suivi cette méthodologie. Il a vocation à être amélioré au fil de l'évolution des projets qui suivent cette méthodologie. Il est publié sous licence CC0 \([Creative Commons Zéro](https://creativecommons.org/publicdomain/zero/1.0/deed.fr)\). Le guide est consultable sur le site [doc.digitaltransport.io/data-transport-mali-GTFS](http://doc.digitaltransport.io/data-transport-mali-GTFS/). Vous trouverez le jeu de données GTFS de Data Transport Mali créé lors de la formation sur [ce dépôt](https://git.digitaltransport4africa.org/places/mali).

Et pour vous aider encore un peu plus dans la création de votre GTFS, la World Bank a mis à disposition un répertoire[ des plus importants outils. ](https://github.com/WorldBank-Transport/GTFS-Training-Materials/wiki/Link-repository-for-international-GTFS-training-materials)



