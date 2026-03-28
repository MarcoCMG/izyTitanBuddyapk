⚡ Titan Buddy Connect v0.5
Titan Buddy Connect est l'application compagnon ultime pour la gestion locale de votre écosystème énergétique Izypower. Elle permet de surveiller et de contrôler vos batteries Titan ainsi que vos onduleurs compatibles (Deye, Solarman) en temps réel, directement via votre réseau domestique.

🛠 Matériel Requis & Compatibilité
L'application communique exclusivement en local avec les équipements suivants :

Batterie : Izypower Titan.

Compteurs (Smartmeters) :

MR1.

Shelly Pro 3EM / Shelly 3EM.

Microonduleurs : Micro-onduleurs Deye (et compatibles Solarman).

Vous n'avez pas tout ce matériel ? Vous pouvez tout de même télécharger et lancer l'application pour explorer l'interface et découvrir les fonctionnalités. Notez simplement que sans ces appareils connectés, les données en temps réel et certaines options d'optimisation ne seront pas actives.

[!CAUTION]
Incompatibilité (temporaire): Ce système ne fonctionne pas avec le Smartmeter IA ni les Smartmeter Solarman ancien ni avec les micro onduleurs Izypower, pas pour le moment! 
[!IMPORTANT]
Le support de ces matériels est actuellement en cours de développement. Suivez les prochaines mises à jour et soyez averti dès qu'ils seront compatibles !

🚀 Fonctionnalités Principales
📊 Monitoring Temps Réel (Local)
Tableau de bord complet : Visualisez instantanément la production solaire, l'état de charge de la batterie (SOC), et la consommation de votre foyer sans dépendre d'un serveur tiers.

Flux d'énergie : Schéma dynamique montrant la circulation de l'énergie entre les panneaux PV, la batterie et le réseau.

Détails Inverteur : Monitoring précis des entrées PV (Tension, Courant, Puissance par string) pour les onduleurs Deye/Solarman.

🔔 Système d'Alertes Intelligent
Notifications de charge : Recevez une alerte dès que votre batterie atteint 100%.

Protection décharge : Configurez un seuil critique (ex: 20%) pour être averti avant la coupure.

Alarmes système : Alertes immédiates en cas de surchauffe ou d'anomalie détectée par l'onduleur.

🔍 Connectivité & Confidentialité
Scan Local Auto : Découverte automatique de vos appareils Titan et Deye sur votre réseau Wi-Fi (via les ports 8080 et 8899).

Zéro Cloud : Toutes vos données restent au sein de votre réseau local. Pas d'accès externe, pour une sécurité et une confidentialité totales.

Support Multi-Appareils : Gérez plusieurs batteries et onduleurs au sein d'une seule interface centralisée.

🌍 Expérience Utilisateur
Multilingue : Disponible en Français, Anglais, Allemand et Chinois.

Design Moderne : Interface fluide construite avec React et Shadcn UI, optimisée pour le mode sombre/clair.

Prévisions Solaires : Intégration de prévisions locales pour anticiper votre production (selon configuration).



🛠 Configuration Technique & Détection
L'application utilise un algorithme de balayage réseau pour identifier vos équipements sans intervention manuelle complexe.

🔍 Mécanisme de Scan Local
Pour que vos appareils soient détectés, assurez-vous qu'ils sont connectés au même sous-réseau (Wi-Fi ou Ethernet) que l'appareil lançant l'application. Titan Buddy Connect scanne votre plage d'adresses IP locale (ex: 192.168.1.0/24) sur les ports de communication dédiés :

Port 8080 : Interface de communication des batteries Titan.

Port 8899 : Interface de données (TCP) des micro-onduleurs Deye / Solarman.

⚙️ Conseils pour une Stabilité Optimale
IP Statiques : Il est vivement recommandé d'assigner des adresses IP fixes (Baux DHCP statiques) à votre batterie Titan et à votre micro-onduleur via l'interface de votre box/routeur. Cela évite de perdre la connexion lors d'un redémarrage du routeur.

Isolation AP (Point d'Accès) : Vérifiez que votre routeur n'isole pas les clients Wi-Fi entre eux. L'option "AP Isolation" doit être désactivée pour que l'application puisse interroger les Smartmeters (Shelly/MR1) et la batterie.

Qualité du Signal : Pour une remontée de données fluide (toutes les secondes), assurez-vous que les Smartmeters Shelly ou MR1 captent correctement votre signal Wi-Fi.
