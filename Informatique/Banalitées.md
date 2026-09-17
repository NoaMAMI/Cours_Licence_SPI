# Usages de l'informatique
- Recherches documentaire / information 
- Traitement de l'information
	- Collect d'information
	- Traitement de l'information
	- Mise en forme des données
- IHM
- Automatisation
- Developpement
	- Conception
	- Architecture
	- Scripting
![[Pasted image 20260915161321.png]]

Bus ISA, se pose sur le bus principal de la Carte mère. gen 1 (8 bit) ou gen 2 (16 bit), 4.77MHz. **Configuration Manuel**

**ROM (Read-Only Memory)**
- Programmée une seule fois, à la fabrication (masque gravé en usine).
- Impossible à modifier ensuite, même en partie.
- Très bon marché en gros volumes, mais rigide : toute erreur ou évolution oblige à refabriquer les puces.
- Usage typique : anciens firmwares figés, BIOS très basiques, jeux vidéo en cartouche.

**PROM (Programmable ROM)**
- Vierge à la sortie d'usine, puis programmable **une seule fois** par l'utilisateur (souvent via une tension élevée qui « grille » des fusibles internes).
- Une fois programmée, elle se comporte comme une ROM classique : plus aucune modification possible.
- Intérêt : flexibilité pour le fabricant/développeur (pas besoin de refaire un masque), mais aucune flexibilité après programmation.

**EEPROM (Electrically Erasable PROM)**
- Reprogrammable **électriquement**, plusieurs fois (typiquement des dizaines de milliers de cycles).
- Effacement et écriture possibles octet par octet, sans sortir la puce du circuit.
- Plus lente à écrire que de la RAM, et plus chère à fabriquer que ROM/PROM.
- Usage typique : stockage de paramètres de configuration, calibration, petites données persistantes (BIOS moderne, microcontrôleurs).
