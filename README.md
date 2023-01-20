# HomeAssistant

Groupe français Home Assistant : https://www.facebook.com/groups/homeassistantgroupefrance

## 🤓 Mad Geek 
Mon tableau de bord compatible avec PC, smartphone, tablette

-----

## ℹ️  INTRODUCTION

Voici ma configuration personnelle :

- Tableau de bord (lovelace UI mode) PC, mobile, tablette
- templates
- thèmes jour et nuit

Je ne suis pas un expert, je suis simplement un passionné, les codes ne sont certainement pas écrits de la meilleure façon, mais j'ai réalisé ceci avec mes petites connaissances.
J'écris tout moi-même donc soyez indulgents ! 😊

Je modifie régulièrement les détails, ou quand j'ai des nouvelles idées. 

-----

## 🚧 INSTALLATION

Ce n'est pas du 1clik ! 

Il faut quelques connaissances avant de se lancer. 
- Installer quelques intégrations hacs necessaires au bon fonctionnnement.
- Créer les bons sensor templates aussi, car je les utilise en masse et en appelle partout dans les cartes.
- Savoir ou copier coller chaque partie, que ce soit les sensor templates, le contenu du lovelace, les templates button card... 
- Modifier les entités, supprimer celles en trop etc...

Il faut adapter a sa config ! 🙂

Dashboard réalisé en 4 colonnes, grâce à "layout card" disponible sur hacs :
- l'onglet est parametré sur Type de vue : Horizontal (layout-card) / width: 350 / max_cols: 4
- une colonne "pile verticale" est imbriquée dans une carte "type: custom:layout-card" / "layout_type: masonry" / et a comme Layout options  "width: 280"


-----

## ℹ️  INTRODUCTION

### version 2023.1.2

Changements :
- corrections bugs sur les thèmes
- améliorations de la carte Courrier : optoin "relevé courrier fait" via un bouton

![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/carte_courrier.jpg)

- améliorations des cartes personnes : la jauge de la batterie affiche l'icone si en charge, le state si non en charge

![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/carte-personne.jpg)

-----

### version 2023.1.1

Changements :
- améliorations de la carte météo
- ajout de traduction sur les erreurs des aspirateurs dans le template "systeme_avertissement"

![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/popup_meteo.jpg)

-----

### 🎉 version 2023.1

Changements :
- modifications des thèmes
- nouvelle carte Activité (https://github.com/herveaurel/HomeAssistant#la-carte-activité)
- nouvelle carte Météo 
- modifications des boutons en bas des cartes
- sous vues pieces : jauges pour les capteurs
- sous vues pieces : réorganisation de la page
- nombreux templates button card modifiés (sidebar,  carte_bouton,  carte_bouton_state, carte_personne_prenom)

-----

### version 2023.0.2

Changements :
- modifications du graphique Apex electricté
- modifications des codes couleurs des sous-boutons dans les cartes
- modifications des thèmes
- modifications du state home dans la carte Personne

-----

### version 2023.0.1

Changements :
- correction des state du moniteur d'air 
- correction de fautes d'othographe sur le moniteur d'air 
- modifications des graphiques electricté et gaz 
- modifications des cartes jauges dans les sous vues des pièces 
- modifications des boutons d'ambiances dans les sous vues des pièces 
- modifications des cartes light dans l'onglet "lumières"
- modifications de la rangées de modes, au dessus de la carte Activité 
- modifications de l'onglet "surveillance système" 
- ajouts de cartes Mini-Graph dans l'onglet "Températures" 
- modifications de l'onglet "batteries" 

-----

### 🥳 Complètement revisité pour cette nouvelle version 2023 : 

- Réécriture des templates button card  
- Modifications des sensor templates  
- Modifications des cartes  
- Nouvelles cartes  
- Nouveauté : les sous-vues ! (adieu les popup de Browser Mod) 
- Nouveaux thèmes
- Utilisation des jauges HATC-GAUGE-CARD, développées par mon ami André Fortuna Gouveia, dont voici le github : https://github.com/tagcashdev/hatc-gauge-card

Et beaucoup d'autres changements ! 🤪
Le tout harmonisé grâce aux templates button card.

D'autres modifications viendront dans les prochaines mises à jour... 😇

-----

## 🎨 THEMES

### Theme Mad Night
![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/dashboard_night.jpg)

### Theme Mad Geek
![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/dashboard_clear.jpg)

### Theme avec l'alarme
![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/dashboard_alarm.jpg)

### Smartphone
![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/dashboard_smartphone.png)

-----

## La carte Activité

![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/carte_activite.jpg)![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/carte_activite2.jpg)![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/carte_activite3.jpg)

🎉 Nouveautés :
- Un tap sue les jauges dirige vers les sous vues associées. 
- Un tap sur le bouton Adguard, switche automtiquemznt le ON/OFF
- Un tap sur l'un des bouton de mise à jour, fait apparaitre / disparaitre le detail en dessous

Afin de choisir les informations qui apparraissent dans la carte acticité : En haut à droite, un bouton ouvrant une sous-vue pour quelques réglages via un simple clic !
Il est possible de choisir son thème, et de choisir ce qui sera affiché dans les informations dynamiques de la partie "Activité". 
Pour cela, créer simplement des input.boolean, comme par exemple : 
- input_boolean.sidecar_show_mode
- input_boolean.sidecar_show_porte
- input_boolean.sidecar_show_mouvement 
etc...

Il est également possible de créer une automatisation, basée par exemple sur l'état de l'alarme ou des présences, pour que les informations varient. En effet, peut-être pas besoin que tout soit affiché quand je suis à la maison, je peux consulter les autres cartes, mais quand je ne suis pas à la maison je veux voir toutes les informations rapidement... 😉

![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/popup_reglages.jpg)

Désormais l'icone d'une pièce prend la couleur réelle, ainsi qu'un dégradé de la couleur réelle pour la pastille et le fond de la carte : 

![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/piece.jpg)

- Badge automatique avec icone de la zone, ou absence d'une personne

![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/badge-personne.jpg)

- Popup de confirmation sur le tap action de certains boutons afin d'éviter des erreurs de manipulations

![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/confirmation.jpg)

-----
## 😎 ONGLETS ET SOUS-VUES

### Tableau de bord avec peu d'onglets...grace aux sous-vues ! J'en ai 30, voici des exemples : 
![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/popup_1.jpg) ![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/popup_2.jpg) ![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/popup_alarme.jpg) ![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/popup_4.jpg) 
![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/popup_5.jpg) ![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/popup_6.jpg) 
![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/popup_7.jpg) ![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/popup_8.jpg)


---------------------

## 🖥️ SETUP 

- Raspberry 4 + SSD
- Clé USB Sonoff Zigbee 3.0
- Dongle Bluetooth Sena Parani UD100
- Box Internet Orange Livebox 4
- 2 cubes Tenda Nova MW6 parametrés en pont 

J'utilise Alexa en vocal, et HomeKit sur l'Apple Watch

## 🔧 Mes appareils 

Zigbee
- Capteurs portes : Xiaomi et Aqara
- Capteurs mouvements : Xiaomi et Aqara
- Capteurs vibration : Xiaomi et Aqara
- Eclairage : ampoule Hue, ampoule GLEDOPTO, ampoules Trust International B.V, ampoules JunYu, ampoules INNR, ampoule TZ3000_keabpigv, bandeau led LEDVANCE
- Prises : Xiaomi, Osram
- Sirène Heiman
- Interrupteurs : bouton Wireless Switch Xiaomi 
- Thermometre rond à écran Orvibo
- Cube Aqara
- Moniteur de qualité de l'air Aqara
- Détecteur de fuite Aqara
- Capteur température Aqara
- Guide de rideau Aqara
- Tête thermostatique de radiateur Aqara
- Sirène Zigbee Frient
- Clavier Zigbee Frient

Bluetooth
- capteurs plantes Xiaomi 
- thermometres ronds à ecran Xiaomi 

Wifi
- Eclairage : ampoules couleurs, lampes de bureau, et bandeau led couleur Yeelight
- Sonnette Arlo Video Doorbell
- TV LG
- Alexa : Fire TV, Fire Cube, Echos Dot et Show 
- Imprimante Canon 
- Ruban led Sonoff intérieur 
- Lave-vaisselle Siemens 
- Aspirateurs : Roborock S50 et S6
- Interrupteur Shelly
- Caméra Aqara Hub G3
- Caméra Aqara Hub G2H Pro


Mes modules :

![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/modules.jpg)

Mes intégrations :

![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/integrations.jpg)

Mes intégrations  hacs:

![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/integrations_hacs.jpg)
![alt text](https://github.com/herveaurel/HomeAssistant/blob/main/Captures/integrations_hacs2.jpg)

---------------------

## ⭐️ VIP 

Si vous aimez , likez 🌟 mon repo !

Si vous souhaitez m'offrir une petite bière 🍺 ou un café ☕️ , dire merci 🙏 , me soutenir ❤️‍🩹, ou m'encourager 💪🏼, et devenir VIP ⭐️ pour une aide personnalisée par message privé :  https://www.paypal.com/paypalme/aaherve
Merci ! 
