# PBS (Product Breakdown Structure)
```mermaid
flowchart LR
    CENTRAL[Central inertiel Prototype]
    MECA[Mecanique]
    LOG[Logiciel]
    ELEC[Electrique]
	GYRO[Bloc gyroscopes]
	ACCEL[Bloc accéléromètres]
	ALIM[alimentation]
	CART[Carte élèctronique]
	CALC[Module de calcule]
	INTER[Interface avion]
	BOIT[Boîtier]

    CENTRAL --- MECA
    CENTRAL --- LOG
    CENTRAL --- ELEC
	MECA --- GYRO
	MECA --- ACCEL
	ELEC --- ALIM
	ELEC --- CART
	LOG --- CALC
	LOG --- INTER
	MECA --- BOIT
```

# WBS (Work Breakdown Structure)

```mermaid
flowchart LR
    CI[Projet CI / Centrale inertielle]

    CI0[CI.0 Management]
    CI1[CI.1 Conception système]
    CI2[CI.2 Réalisation sous-système mécanique]
    CI3[CI.3 Réalisation sous-système électrique]
    CI4[CI.4 Réalisation sous-système logiciel]
    CI5[CI.5 Intégration & qualification]

    CI --- CI0
    CI --- CI1
    CI --- CI2
    CI --- CI3
    CI --- CI4
    CI --- CI5

    CI01[CI.0.1 Gestion de Projet]
    CI02[CI.0.2 Assurer la qualité projet]
    CI0 --- CI01
    CI0 --- CI02

    CI21[CI.2.1 Concevoir en détail la mécanique]
    CI22[CI.2.2 Fabriquer le boîtier]
    CI23[CI.2.3 Acheter le bloc gyroscopes]
    CI24[CI.2.4 Acheter le bloc accéléromètres]
    CI25[CI.2.5 Assembler la mécanique]
    CI2 --- CI21
    CI2 --- CI22
    CI2 --- CI23
    CI2 --- CI24
    CI2 --- CI25

    CI31[CI.3.1 Concevoir la partie électrique]
    CI32[CI.3.2 Réaliser la carte électronique]
    CI33[CI.3.3 Acheter l'alimentation]
    CI3 --- CI31
    CI3 --- CI32
    CI3 --- CI33

    CI41[CI.4.1 Concevoir en détail le logiciel]
    CI42[CI.4.2 Coder et tester unitairement le logiciel]
    CI4 --- CI41
    CI4 --- CI42

    CI51[CI.5.1 Préparer les plans de test V&V]
    CI52[CI.5.2 Intégrer le produit]
    CI53[CI.5.3 Qualifier le produit]
    CI5 --- CI51
    CI5 --- CI52
    CI5 --- CI53
```
# Diagramme de flux
```mermaid
flowchart TB
    CODIR([CR de décision / CODIR projets])
    CI1[CI.1 Conception système]
    SPEC([Spécif. prototype / approuvée])
    CODIR --> CI1 --> SPEC

    CI21[CI.2.1 Concevoir la mécanique]
    DCM([Dossier conception méca approuvé])
    SPEC --> CI21 --> DCM
    CI22[CI.2.2 Fabriquer le boîtier]
    CI23[CI.2.3 Acheter le bloc gyroscopes]
    CI24[CI.2.4 Acheter le bloc accéléromètres]
    DCM --> CI22
    DCM --> CI23
    DCM --> CI24
    BOIT([Boîtier fabriqué])
    GYRO([Bloc gyros réceptionné])
    ACC([Bloc accéléros réceptionné])
    CI22 --> BOIT
    CI23 --> GYRO
    CI24 --> ACC
    CI25[CI.2.5 Assembler la mécanique]
    BOIT --> CI25
    GYRO --> CI25
    ACC --> CI25
    MECA([Sous-système méca assemblé])
    CI25 --> MECA

    CI31[CI.3.1 Concevoir la partie électrique]
    DCE([Dossier conception électrique approuvé])
    SPEC --> CI31 --> DCE
    CI32[CI.3.2 Réaliser la carte électronique]
    CI33[CI.3.3 Acheter l'alimentation]
    DCE --> CI32
    DCE --> CI33
    CARTE([Carte électronique réceptionnée])
    ALIM([Alimentation réceptionnée])
    CI32 --> CARTE
    CI33 --> ALIM

    CI41[CI.4.1 Concevoir en détail le logiciel]
    DCL([Conceptions détaillées logiciel approuvées])
    SPEC --> CI41 --> DCL
    CI42[CI.4.2 Coder et tester unitairement le logiciel]
    LOG([Logiciel testé])
    DCL --> CI42 --> LOG

    CI51[CI.5.1 Préparer les plans de test V&V]
    VV([Plans et moyens de test V&V approuvés])
    SPEC --> CI51 --> VV
    CI52[CI.5.2 Intégrer le produit]
    MECA --> CI52
    CARTE --> CI52
    ALIM --> CI52
    LOG --> CI52
    VV --> CI52
    CRI([CR d'intégration])
    CI52 --> CRI
    CI53[CI.5.3 Qualifier le produit]
    CRI --> CI53
    CIC([Centrale inertielle certifiée])
    CI53 --> CIC

```
# RAM (Responsibility Assignment Matrix)

| Code WBS | Activité                                 | Chef de projet | Ingénieur qualité | Ingénieur dév. | Technicien dév. | Directeur de projet |
| -------- | ---------------------------------------- | :------------: | :---------------: | :------------: | :-------------: | :-----------------: |
| CI.0.1   | Gérer le projet                          |       R        |                   |                |                 |          A          |
| CI.0.2   | Assurer la qualité projet                |                |         R         |                |                 |          A          |
| CI.1     | Conception système                       |                |                   |       R        |                 |          A          |
| CI.2.1   | Concevoir en détail la mécanique         |                |                   |       R        |                 |                     |
| CI.2.2   | Fabriquer le boîtier                     |                |                   |       R        |        P        |                     |
| CI.2.3   | Acheter le bloc gyroscopes               |       R        |                   |       A        |                 |                     |
| CI.2.4   | Acheter le bloc accéléromètres           |       R        |                   |       A        |                 |                     |
| CI.2.5   | Assembler la mécanique                   |                |                   |       R        |        P        |                     |
| CI.3.1   | Concevoir la partie électrique           |                |                   |       R        |        P        |                     |
| CI.3.2   | Réaliser la carte électronique           |       R        |                   |       A        |                 |                     |
| CI.3.3   | Acheter l'alimentation                   |       R        |                   |       A        |                 |                     |
| CI.4.1   | Concevoir en détail le logiciel          |                |                   |       R        |                 |                     |
| CI.4.2   | Coder et tester unitairement le logiciel |                |                   |       R        |        P        |                     |
| CI.5.1   | Préparer les plans de test V&V           |                |                   |       R        |                 |                     |
| CI.5.2   | Intégrer le produit                      |                |                   |       R        |        P        |                     |
| CI.5.3   | Qualifier le produit                     |                |                   |       R        |        P        |          A          |

