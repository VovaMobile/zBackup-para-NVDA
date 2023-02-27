# Manuel de zBackup pour NVDA.

zBackup nous permettra de faire des copies de sauvegarde de la partition contenant le système d'exploitation.

Cela signifie que le disque ou la partition contenant l'installation de Windows peut être enregistré pour être restauré.

zBackup peut faire des copies de sauvegarde en chaud sans la nécessité d'arrêter les applications ou d'arrêter de faire ce que nous faisons.

[Cette extension est basée sur l'application Drive Snapshot.](http://www.drivesnapshot.de/en/index.htm)

zBackup vient simplifier les actions communes et nécessaires afin que nous puissions  faire  une copie de sauvegarde et la restaurer sans avoir besoin d'aide ou d'outils externes, tels que WinPE.

En plus de faire des copies de sauvegarde, nous pouvons restaurer les dites copies, les assembler comme unités virtuelles, et tout cela est accessible.

zBackup est basé sur Drive Snapshot, il utilise donc une application externe à NVDA. Cette application pèse moins de 500 Ko et sera téléchargée à partir de la page officielle lorsque nous démarrons l'extension pour la première fois. Dans chaque mise à jour de l'extension de zBackup, l'application sera téléchargée à partir de sa page pour avoir toujours  la dernière version.

Drive SnapShot n'est pas une application gratuite et a ses limites. L'application peut être utilisée pendant 30 jours dans son intégralité, mais au-delà  de cette période la seule chose qui ne nous permettra pas est de continuer à faire des copies de sauvegarde, bien que nous pouvons  les restaurer et les monter.

Sur la page de l'application, nous pouvons acheter Drive SnapShot pour 39 euros dans sa licence la plus basic, suffisamment pour un usage personnel.

Si nous achetons la licence, nous devons garder à l'esprit que nous devons l'avoir sous la main et bien  enregistré, car chaque fois que nous mettons à jour zBackup, lors d'un téléchargement d'une version mise à jour de l'application, nous devrons l'enregistrer pour avoir une durée illimitée.

## *** Informations très importantes ***

zBackup a été testé dans différents environnements et situations avec d'excellents résultats. Cependant, dans le monde de l'informatique, tout peut se produire, et il peut y avoir des bogues, il s'agit donc d'une extension seulement conseillé aux personnes possédant une connaissance suffisante pour pouvoir sortir d'une mauvaise restauration du système. Cela signifie savoir démarrer par un autre moyen afin de récupérer les informations, installez le système d'exploitation et, finalement être capable d'avoir Windows à nouveau si quelque chose s'est mal passé.

Lorsque vous utilisez l'extension, l'utilisateur est la seule personne responsable des résultats, en excluant à l'auteur de l'application et de l'extension de tout problème pouvant être produit par une mauvaise restauration, une copie de sauvegarde défectueuse, une perte de données partielle ou complète, et finalement, le résultat final de l'utilisation dudit paquet.

## *** Avertissement pour une bonne utilisation ***

zBackup intègre des protections pour éviter de faire des erreurs, telles que la restauration de la même partition de Windows, utiliser des symboles non autorisés dans les noms des copies, la protection du manque d'espace, etc. Cependant, plusieurs considérations doivent être prises en compte.

Les copies de sauvegarde ne peuvent être restaurées qu'à partir d'une partition ou d'un disque différent de Windows. Les copies peuvent également être restaurées à partir de supports externes, mais nous devrons prendre en considération la vitesse de lecture de ces  supports. Un support lent peut causer des problèmes lors de la restauration, il est donc recommandé d'utiliser des disques externes SSD ou une méthode de stockage USB de haute vitesse de type C.

Nous devons garder à l'esprit que si nous effectuons une copie de sauvegarde en mode non sécurisé du BIOS, nous pouvons restaurer cette copie pendant que nous sommes en ce mode. Si nous changeons en mode sécurisé, la copie effectuée en mode non sécurisé ne peut plus être restaurée. Chaque copie doit être restaurée avec le matériel correspondant et la configuration matérielle correspondante.

De même, il est conseillé de ne pas utiliser zBackup pour faire des copies de sauvegarde des disques protégés avec BitLocker.

zBackup a été testé sous Windows 10 et 11, mais elle est valide dans Windows 7 et 8 selon la documentation de l'application.

Il est recommandé que le répertoire où nous gardons des copies de sauvegarde ne contiennent pas d'espaces.

zBackup ne peut pas être utilisé depuis des copies portables de NVDA.

## Interface de zBackup

zBackup vise à avoir peu d'options et d'être claire, donc à tout moment, cela nous donnera des messages d'information de ce qui va à se faire  et les étapes à suivre.

Depuis l'écran principal, nous pouvons faire une copie de sauvegarde.

Pour lancer l'écran principal, il est nécessaire d'ajouter un geste de commande allant dans le menu NVDA / Préférences / Gestes de commandes / Catégorie zBackup.

Une fois ouverte, nous tomberons dans un champ en lecture seule qui contiendra le répertoire où nous enregistrons la copie de sauvegarde. Si nous faisons Tabulation   nous tomberons sur  le bouton "Sélectionner un répertoire", ce qui nous permettra de sélectionner le répertoire.

Les copies de sauvegarde seront enregistrées dans des sous-dossiers dans ce répertoire. Il est recommandé que ce dossier ne contiennent pas d'espaces.

Si nous faisons Tabulation à nouveau nous tomberons sur un champ d'édition appelé "Nom pour la copie de sauvegarde". Sur ce champ nous mettrons le nom d'identification de notre copie de sauvegarde.

Sur ce champ, les espaces ou les caractères non autorisés  sont pas permis par Windows dans les dossiers et les fichiers. Ces caractères sont les suivants, compris entre les guillemet triple:

"""\ / : * ? » < > |"""

Ce nom d'identification servira à nommer le sous-dossier et les différents fichiers de la copie de sauvegarde.

Si nous continuons à tabuler, nous tomberons sur une zone de liste déroulante où nous pouvons choisir la taille de chaque fichier à partir de la copie de sauvegarde. Nous pouvons sélectionner 500 Mo à 10 Go.

Cela signifie que en faisons la copie de sauvegarde, les fichiers résultants auront cette taille. Pour donner un exemple: si notre partition Windows a une taille d'environ 60 Go, la copie résultante aura une taille totale d'environ 20 à 30 Go. Si nous choisissons que les fichiers résultants soit de 10 Go, il créera environ 3 fichiers.

Si nous faisons Tabulation à nouveau, nous allons tomber sur le bouton "Démarrer la copie de sauvegarde". Si toutes les données sont bien remplies et que les conditions d'espace et d'emplacement, sont remplies, cela nous donnera la possibilité de démarrer  la copie de sauvegarde, indiquant qu'elle ce fera à tout moment.

Si nous faisons Tabulation à nouveau, nous allons tomber sur le bouton "Menu". Si nous appuyons  sur lui, un menu contextuel sera déployé avec les options suivantes:

* Restaurer la copie de sauvegarde: Avec cette option, nous pouvons restaurer une copie de sauvegarde. Nous serons averti avec des messages. Il est important de garder à l'esprit que, une fois atteint  le point de choisir  l'image à restaurer et l'accepter, le processus ne revient plus en arrière et le système sera restauré.

* Monter un disque virtuel d'une copie de sauvegarde: Avec cette option, nous aurons la possibilité de choisir une unité libre de notre ordinateur et de monter virtuellement une copie. C'est bien au cas où nous avons quelque chose de spécifique que nous voulons récupérer d'une copie et que nous ne voulons pas la restaurer complètement.

* Démonter des unités virtuelles: Cette option démontera toutes les unités virtuelles que nous avons montées avec zBackup. Il n'est pas possible de choisir une par une. Cette option sera exécutée de manière satisfaisante même si nous n'avons pas une de montée.

* Exécutez l'application Drive Snapshot: Avec cette option, nous lancerons Drive Snapshot et nous pouvons utiliser l'application dans son mode d'interface graphique. Nous pouvons également l'enregistrer avec le numéro de série, si vous avez acquis une licence.

Toutes les  contrôles ont des raccourcis clavier, qui sont annoncés selon que nous parcourons l'interface.

## Autres

Lors de la copie de sauvegarde, il est nécessaire que la partition de disque ou de destination soit la taille de la partition système. Si la partition système a 60 Go, il est nécessaire de disposer de 60 Go libres sur la de destination, bien que la copie occupe la moitié ou moins. Ceci est pour la sécurité.

Il est conseillé d'avoir un support de démarrage au cas où quelque chose s'est mal passé. Un WinPE et un Drive Snapshot est recommandé dans ce support. De cette façon, nous pourrions récupérer depuis la copie de sauvegarde le système.

zBackup a été testé sous Windows sans modifier. Les bonnes performances ne sont pas garanties dans certaines versions  de Windows modifiées qui circulent sur Internet.

J'avertit à nouveau que zBackup ne doit pas être utilisé si vous n'avez pas la connaissance pour pouvoir sortir d'une mauvaise restauration.

## Problèmes trouvés

L'extension a été testée sur plusieurs ordinateurs avec différents matériels et configurations, ainsi que sur des machines virtuelles.

Lorsqu'il démarre afin de restaurer, nous pouvons avoir comme quelque chose d'indicatif que les ventilateurs de l'ordinateur tournent et s'arrêtent lorsque la restauration se termine. De même, si nous avons des écouteurs branchés, avec des cliquetis dans les écouteurs, nous pouvons détecter les redémarrages.

En mode sécurisé, parfois, une fois la copie de sauvegarde restaurée, le système ne démarre pas et reste sur le logo du fabricant.

Dans ces cas, il est opportun d'attendre quelques minutes et d'éteindre l'ordinateur.

La prochaine fois que nous démarrons, Windows nous demandera si nous voulons vérifier le disque ou il commencera cette vérification pour lui-même, ce qui nous donnera un écran inaccessible qui nous indique que nous essayons une autre option pour récupérer ou éteindre l'ordinateur.

Si nous appuyons sur Entrée, il s'éteindra. La prochaine fois que nous démarrons l'ordinateur, il démarrera sous Windows.

C'est la protection du mode sécurisé, qui joue finement, mais en réalité, la restauration a été faite correctement.

De même, parfois démarre sous Windows, Et quand nous démarrons déjà la session, une notification indique que nous devons redémarrer pour réparer les erreurs. Si nous redémarrons et attendons quelques secondes, nous reviendrons sur Windows, sans aucun problème.

Pendant les tests, cela s'est passé une fois, en une minorité de fois. Cependant, cela peut arriver, alors vous devriez savoir ce qui est fait. L'avis d'avoir un autre moyen de récupération est toujours valable au cas où, et il faut comprendre qu'il y a des centaines de machines, de configurations et peut-être ce qui fonctionne dans une, ne le fait pas dans une autre.

De nos jours, nous avons généralement une application de reconnaissance OCR sur nos mobiles. Il est fortement recommandé de l'utiliser pour savoir ce qui se passe sur des écrans pas accessibles.

Comme il a été rappelé précédemment, l'auteur de l'application et de l'extension sont exemptés de toute responsabilité pour tout problème causé par l'extension ou le programme.