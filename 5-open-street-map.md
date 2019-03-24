# \#5 - Open Street Map

## Définition

### Signification 

**OpenStreetMap** \(OSM\) est un projet de cartographie qui a pour but de constituer une base de données géographiques libre du monde \(permettant par exemple de créer des[ cartes sous licence libre](http://www.openstreetmap.org)\). Il utilise pour cela une base de données géographique, les systèmes GPS des contributeurs, et d'autres données libres. Les données sont réutilisables selon la [licence](4-lopen-source.md#les-licences-copyleft) ODbL, et tout un chacun \(individus, collectivités, organisations, etc.\) peuvent les utiliser et surtout contribuer à leur enrichissement. La communauté œuvre d'abord par idéologie. Convaincue que les données géographiques de la planète devraient appartenir au bien commun et non aux agences qui les ont relevées pour les exploiter commercialement, elle encourage les internautes à effectuer leurs propres tracés et à les publier sous licence CC by.

### Historique 

Il a été mis en route en juillet 2004 par Steve Coast au University College de Londres. Par l'utilisation d'outils web qui permettent l'intervention et la collaboration de tout utilisateur volontaire, OpenStreetMap est une contribution à ce qui est appelé la néogéographie. Dès 2013, le millionième contributeur participant à la réalisation de la carte mondiale librement accessible et utilisable a été enregistré.

### Dans le détail

Les internautes peuvent contribuer à la création et à la numérisation de cartes. Des éditeurs permettent de réaliser en ligne des cartes en se basant sur un fond d'image satellitaire. Cependant, ces images satellitaires ne couvrent pas toujours en haute résolution l'ensemble du globe. C'est pourquoi il est possible d'introduire des données provenant de récepteurs GPS. 

Les points d'intérêt \(POI\) c'est-à-dire, toutes les mentions utiles \(noms, largeur, nature du revêtement, sens uniques, parcs, zones résidentielles et d'activités, barrières, pistes cyclables, boîtes aux lettres, cabines téléphoniques, commerces, fontaines, etc.\) sont notés, soit en les écrivant, soit en les photographiant, soit en les décrivant sur un appareil d'enregistrement audio.

Tous les modes de locomotion terrestre possibles sont utilisés : à pied, à deux-roues, à rollers, à skis, en véhicule automobile particulier, en bus, en train…

Les enregistrements de données GPS peuvent être rendus publics par l'intermédiaire du site d'OSM. Cela a pour avantage de les rendre visibles dans les outils d'édition des cartes. Cela facilite la couverture internationale : une personne séjournant dans une autre région ou un autre pays que le sien peut publier les tracés de ses parcours, à charge pour les habitants permanents de les compléter.

La carte principale est une carte routière comprenant des éléments figurés de manière plate, mais une carte du relief avec les courbes de niveaux est également disponible.

## Enjeux

### Quel lien entre OSM et les transports ?

OSM peut jouer un rôle dans le domaine des transports sous deux angles différents mais complémentaires : 

* comme **base de données** : il peut être interrogé par des calculateurs d'itinéraires pour accéder aux points d'intérêt \(POI\) renseignés par les contributeurs, 
* comme **outil de cartographie** : afin de représenter des lignes de transports publics et les arrêts desservis. Ces dernières peuvent ensuite être visualisées par n'importe quel acteur. 

### OSM et GTFS savent-ils se parler ?

Oui et non. En réalité, chaque dispositif a son intérêt, et ses limites. 

Du coté d'OSM, les données transports restent des données géographiques \(elles peuvent gérer au mieux quelques informations sur les fréquences\). Par contre, de par l'enrichissement des données réalisé par la communauté, les arrêts de bus peuvent proposer un niveau de détail très important, ce qui peut être très intéressant pour une agence pour améliorer la connaissance de son réseau du point de vue des utilisateurs. 

Du coté du [GTFS](digital-transport-4-africa-2-le-gtfs.md), les données sont assez basiques, créées dans une logique d'offre. L'objectif est ici surtout de faire correspondre des arrêts, des lignes \(et leurs coordonnées GPS\) avec des horaires \(et donc des amplitudes et fréquences\). 

Il existe plusieurs réflexions en cours visant à donner la possibilité d'utiliser les deux dispositifs pour améliorer globalement la connaissance des offres de transport : 

* \*\*\*\*[**GO\_Sync** \(General Transit Feed Specification OpenStreetMap Synchronization\) ](https://github.com/CUTR-at-USF/gtfs-osm-sync)est une application permettant de déverser tous les arrêts de bus de ses GTFS dans OpenStreetMap, ainsi que de récupérer des modifications participatives telles que des améliorations des emplacements des arrêts de bus ou l'ajout d'équipements \(bancs,  éclairages, supports à vélos\) pour les intégrer dans la base d'arrêts de bus de l'agence de transports. Lorsqu'une un nouveau GTFS est mis à jour, GO\_Sync les compare automatiquement au contenu d'OSM et guide l'utilisateur dans la fusion des modifications éventuelles apportées aux deux ensembles de données. Cet outil fonctionne donc dans une logique de synchronisation/comparaison, et ne traite que l'aspect géographique de la donnée. 
* [**OSM2GTFS**](http://github.com/grote/osm2gtfs) est un script qui permet de mixer les données de transport public d'OSM et des informations de planification externes pour créer un fichier GTFS.

  Le script extrait les données actuelles sur les réseaux de transport en commun directement à partir d'OSM via l'API Overpass. Il stocke les données dans des objets python et des caches sur le disque. Ensuite, les données sont combinées avec une autre source d'informations de planification \(horaires\) afin de créer un fichier GTFS à l'aide de la bibliothèque transitfeed. Ce script est intéressant mais reste limitatif. D'une part, il doit être re-configuré à chaque adaptation et il nécessite à chaque fois un travail chronophage sur les calendriers. Au final, il est intéressant dans deux cas : lorsque le créateur de la donnée a des connaissances en développement, et lorsque le réseau est de petite taille, et actualisé à une fréquence peu élevée. 

### Comment assurer qualité et pérennité  dans les contributions OSM transports ? 

Les offres de transports et donc les GTFS, sont en règle générale produits par les autorités de transports \(AOT\), autrement appelées "agences" aux Etats Unis, en lien avec les exploitants des réseaux. De son coté, la communauté OSM peut cartographier des offres \(lignes+arrêts\) soit : 

* lorsque ces informations n'existent pas \(pas d'autorité de transports, offre privées et/ou informelle...\),
* lorsque des informations existent mais qu'elles peuvent être complétées, enrichies par les citoyens. 

Dans le premier cas, l'enjeu majeur est d'assurer la pérennité de la communauté, seule à pouvoir créer des données. Dans le second, il s'agit d'engager une collaboration entre l'autorité de transports et la communauté OSM afin de créer des complémentarités entre leurs méthodes. 

## Parole d'acteurs

Felix Delattre, [Technical Project Manager, Humanitarian OpenStreetMap Team](https://www.linkedin.com/company/4873165/) \(Berlin\)

> **Comment définirais-tu OSM en quelques mots ?**
>
> OSM est un projet collaboratif pour créer des données géocodées utilisables librement. OSM est considéré comme la somme la plus importante de données géographiques ouvertes au monde, librement utilisables, téléchargeables, le tout gratuitement. C'est aussi une communauté globale et active de plus d'un million de contributeurs individuels. Du volontaire, au groupe organisé, en passant par les entreprises et les collectivités publiques locales comme nationales, tous peuvent collaborer et profiter de ce dispositif. 
>
> **Pourquoi le domaine des transports est-il propice à l'utilisation d'OSM ? Que permet OSM dans ce domaine bien particulier ?**

> Les données peuvent servir de base pour tous types de cartes, applications et analyses que l'on souhaiterait réaliser dans le domaine des transports publics. 
>
> OSM encourage la collaboration : les données peuvent être collectées et maintenues comme une base dynamique "crowdsourcée" ou "[community of practice](http://pilot-projects.org/blog/entry/communities-of-practice-using-systems-thinking-to-co-create-a-better-world)". OSM permet d'établir un flux de travail collectif pour la création et l'utilisation de données dans une logique de croissance locale, de transfert de connaissance et de pérennité de la communauté au niveau local. 
>
> OSM fournit des solutions technologiques, offre un écosystème intégré avec des centaines d'applications de logiciels libres pour créer des systèmes d'information voyageurs \(sur le web, sur mobile\), des outils d'analyse scientifique, de planification urbaine et des transports collectifs.
>
> Enfin, OSM permet d'être flexible. Il s'adapte aux réalités locales et fournit une plate-forme d'expérimentation autour de différentes modalités de transports publics.

> **Quels sont les principaux défis pour augmenter encore l'utilisation d'OSM dans le secteur des transports ?** 
>
> Jusqu'à présent, des projets pilotes ont été réalisés. Ils ont montré les capacités de la technologie OSM dans ce domaine. Mais en réalité, cet aspect est pour le moment très peu développé. Il y a un potentiel très important pour les entreprises, le secteur public et les agences de coopération internationale pour partager et transférer des connaissances. C'est un domaine prometteur à explorer par ces acteurs, mais qui ne peut toujours pas être considéré comme une solution exploitable. Il en va de la responsabilité d'OSM de former la communauté pour avancer sur le sujet.

> **Quels sont les projets OSM orientés transports les plus marquants selon toi à l'échelle mondiale ?**

> * [Transportr](https://transportr.app/) et osm2gtfs **:** l'application mobile de calculateur d'itinéraires TC libre, associée à osm2gtfs, permet l'intégration de données d'OSM dans l'application avec un processus optimisé, 
> * [OpenTripPlanner](https://www.opentripplanner.org/), comme système d’information voyageurs libre,  
> * [Maps.me](https://maps.me/), comme application mobile basée sur OSM, qui inclut un calcul d'itinéraires incluant les transports publics et les fréquences de métros dans les grandes villes. 
>
> En termes d'utilisation, on peut également mentionner [la ville d'Helsinki](https://www.digitransit.fi/) et son équipe qui ont utilisé, contribué et créé des outils de logiciel libre et de données ouvertes pour constituer un excellent système d'information voyageurs.

## Cas d'usage

### Managua

Au cours des deux dernières années, plus de 150 bénévoles ont investigué le réseau de transports en commun de la capitale **Managua** et de la ville voisine, Ciudad Sandino. Ils ont utilisé OpenStreetMap pour collecter de manière collaborative les informations géographiques et les données de l’ensemble du réseau de transports en commun de la ville. Au final, [ils ont créé une carte papier,](https://support.mapanica.net/) une simple carte en ligne toutes les données, et ont ouvert tous les fichiers en Open Data.

### Accra

Jungle Bus a cartographié les 320 lignes et 2550 arrêts de "Trotro" \(transport artisanal\) d'Accra \(2 millions d'hab\) en 3 temps :

* la collecte terrain : des contributeurs OSM ont pris toutes les lignes de "trotro" de l'agglomération outillés d'un GPS, 
* l'import dans OSM, 
* la création d'un fichier GTFS du réseau, désormais réutilisé par différents acteurs :
  * Transit App pour son application de calcul d'itinéraires, 
  * Kisio Digital pour son moteur de calcul d'itinéraire Navitia.io
  * TransportR qui utilise Navitia dans son appli de calcul d'itinéraire, 

## **Exercice pratique !**

### **Cartographier sur OSM**

**Ce didacticiel s'adresse à ceux qui veulent contribuer à la carte coopérative libre** [**OSM**](http://fr.wikipedia.org/wiki/OpenStreetMap).

* Deux comptes utilisateurs sont nécessaires :
  * pour cartographier, il faut [s’enregistrer ici](https://www.openstreetmap.org/create-account.html) ;
  * pour collaborer à l’édition du wiki, il faut [s’enregistrer ici](https://wiki.openstreetmap.org/wiki/Special:UserLogin).
* Les questions plus techniques et la [FAQ](https://wiki.openstreetmap.org/wiki/FR:FAQ) peuvent être trouvées sur leur propre page dans le wiki. [La page d’aide](https://wiki.openstreetmap.org/wiki/FR:Aide) regroupe les liens les plus utiles.
* Les différents termes techniques sont expliqués dans le [glossaire](https://wiki.openstreetmap.org/wiki/FR:Glossary).
* Vous pouvez joindre [la communauté](https://wiki.openstreetmap.org/wiki/FR:Beginners_Guide_1.0) ou la contacter au niveau [international](https://wiki.openstreetmap.org/wiki/Additional_Help) ou [francophone](https://wiki.openstreetmap.org/wiki/FR:Contact).

**Les cinq étapes pour faire une carte**

Suivez ces quelques étapes pour faire vos premiers pas de cartographe contributeur d’OSM :

1. [Collecter des données](https://wiki.openstreetmap.org/wiki/FR:Beginners_Guide_1.1)
2. [Téléverser des données](https://wiki.openstreetmap.org/wiki/FR:Beginners_Guide_1.2)
3. [Mettre en forme les cartes avec un éditeur](https://wiki.openstreetmap.org/wiki/FR:Beginners_Guide_1.3)
4. [Compléter et qualifier les données](https://wiki.openstreetmap.org/wiki/FR:Beginners_Guide_1.4.2)
5. [Dessiner les cartes !](https://wiki.openstreetmap.org/wiki/FR:Beginners_Guide_1.5)

### Cartographier le réseau de bus de ma ville

Une page propose un ensemble de pistes et de conseils pour cartographier le réseau de bus d’une commune en utilisant les outils de l’OSM comme Jungle Bus.

{% embed url="https://wiki.openstreetmap.org/wiki/FR:Je\_cartographie\_le\_r%C3%A9seau\_de\_bus\_de\_ma\_ville" %}

\*\*\*\*







