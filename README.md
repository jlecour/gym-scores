# gym-scores
Un système de prise de note en compétion de gym

# Plan de route

- [ ] réseau wifi sécurisé
- [ ] serveur DHCP + DNS
- [ ] serveur, version RaspberryPi "plug & play"
- [ ] serveur, version portable du cousin
- [ ] système de redondance (app, données…)
- [ ] accès "administrateur" pour config
- [ ] accès "saisie de note"
- [ ] accès "contrôle des licences"
- [ ] accès "club"
- [ ] saisie multiple possible, avec contrôle de cohérence
- [ ] accès "responsable des juges"
- [ ] accès "responsable de compétition" (feuilles de match, licences, accès app…)
- [ ] version imprimable des palmarès
- [ ] version imprimable des feuilles de match
- [ ] prise en compte des agrès optionnels

# Idées techniques

* frontend ELM
* backend Phoenix
* stockage des notes en clé/valeur
* synchro permanente des données sur disque (possibilité de lecture par un humain)
* synchro entre une app "leader" et une "follower" pour la résilience
* traçabilité de toutes les saisies (y compris les modifications ; quand et par qui)


# Idées "métier"

## Les juges

* ils sont identifiés (y compris le juge expert)
* ils sont affectés à un ou plusieurs agrès et ne peuvent noter qu'à ces agrès ; les calculs de notes sont automatiquement gérés en fonction du nombre de juges sur un agrè.
* ils peuvent modifier l'ordre de passage
* ils voient facilement toutes les notes de leur rotation
* ils ne peuvent saisir/modifier que les notes du gymnaste en cours et doivent dévérouiller les gymnastes passés pour modifier les notes
* décider s'ils voient la note finale du gymnaste en direct ou pas
* voir s'il est pertinent leur de faire valider au juge expert les notes avant prise en compte réelle (par gymnaste, par rotation, ou pas du tout).

## Les clubs

* possibilité pour les clubs de voir le détail des notes de tous les gymnastes du club
* envisager une saisie en amont et sur place (jusqu'à un verrouillage en début de compétition) des infos sur les gymnastes : licences, engagements…

## Les gestionaires de compétition

## Les responsables de compétition

* le/la responsable des juges peux voir et modifier la note de n'importe quel juge de sa responsabilité
