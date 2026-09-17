## 1. Unités et dimensions

On ne peut additionner/comparer des grandeurs que si elles ont la même dimension (ex : on peut additionner des longueurs entre elles, mais pas une longueur avec une masse).

**Tableau des dimensions des grandeurs usuelles** (M = masse, L = longueur, T = temps) :

| Grandeur          | Unité | Dimension |
| ----------------- | ----- | --------- |
| Vitesse           | m.s⁻¹ | L.T⁻¹     |
| Accélération      | m.s⁻² | L.T⁻²     |
| Force (Newton)    | N     | M.L.T⁻²   |
| Travail (Joule)   | J     | M.L².T⁻²  |
| Puissance (Watt)  | W     | M.L².T⁻³  |
| Pression (Pascal) | Pa    | M.L⁻¹.T⁻² |

### Application : démonstration dimensionnelle — courbure d'une aile

Schéma : poutre encastrée (aile), avec flèche $U_2$ à l'extrémité libre. Équation de départ :
$$\dfrac{d^2 U_2}{dx^2} = \dfrac{M_{fB}}{E \cdot I / 6 \cdot x_3}$$


où $M_{fB}$ est un moment fléchissant, $E$ le module de Young, $I$ un moment d'inertie.

Vérification par analyse dimensionnelle (telle que présente sur la photo) :

- $\dfrac{d^2U_2}{dx^2}$ → dimension $L^{-1}$
- $M_{fB}$ → dimension $M.L^{-1}.T^{-2}$
- $\dfrac{M.L^2.T^{-2}}{M.L^{-1}.T^{-2}} = L^{-1}$ (encadré, résultat mis en évidence)


---

## 2. Atmosphère normalisée

**Conversion Kelvin <-> Celsius (température absolue) :**

$$n°C = n°K + 273{,}15$$

**Repère dans la tropopause** (couche où volent les avions de ligne) :

- Température extérieure : **−56,5 °C**
- Altitude : **11 km**
- Pression : **0,22 × 10⁵ Pa**

---

## 3. Modèle du gaz parfait

$$p \cdot V = n \cdot R \cdot T_{K}°$$

**Tableau des paramètres d'état** (tel que noté sur la photo) :

| Nature      | Grandeur           | Type         |
| ----------- | ------------------ | ------------ |
| Pression    | $p$ en Pa          | **intensif** |
| Volume      | Vol en m³          | —            |
| Température | $T°K$              | **intensif** |
| Masse       | $m$, en mol / kmol | —            |

**Mole / Kilomole :**

|              | Nombre de molécules     | Masse exprimée en |
| ------------ | ----------------------- | ----------------- |
| **Mole**     | $6{,}02 \times 10^{23}$ | grammes (g)       |
| **Kilomole** | $6{,}02 \times 10^{26}$ | kilogrammes (kg)  |


**Valeur de R** (selon l'unité de $n$) :

- $R = 8{,}31\ \text{J}.\text{mol}^{-1}.\text{K}^{-1}$
- soit $R = 8{,}31 \times 10^{3}\ \text{J}.\text{kmol}^{-1}.\text{K}^{-1}$ si on raisonne en kilomoles

**Correction de Van der Waals** (gaz réel, mentionnée dans les notes manuscrites sans développement) :

$$\left(p + \dfrac{a}{V^2}\right)(V - b) = n \cdot R \cdot T°_K$$

*(équation notée mais non expliquée en cours — à demander/creuser si besoin, $a$ et $b$ sont des constantes propres à chaque gaz qui corrigent respectivement les interactions moléculaires et le volume propre des molécules)*

**Point à noter :** avec $p$, $V$, $T$ liés par $pV = nRT$, sur les 3 variables seules 2 sont réellement indépendantes (la troisième se déduit des deux autres).

### Chaleur volumique (Cp, Cv)

$$C_v = \dfrac{\text{Joule}}{\text{kilomole} \cdot °K} \quad \text{(à volume constant)}$$
$$C_p = \dfrac{\text{Joule}}{\text{kilomole} \cdot °K} \quad \text{(à pression constante)}$$

$$C_p - C_v = R$$

---

## 4. Le son

- **Son** = discontinuité de pression qui se propage
- **Vitesse ≠ célérité** (à ne pas confondre)
- **Énergie proportionnelle à $p^2$**

**Niveau sonore en décibels :**

$$dB = 10\log_{10}\left(\left(\frac{\Delta p}{10^{-5}}\right)^{2}\right) = 20\log_{10}\left(\frac{\Delta p}{10^{-5}}\right)$$

**Rappel — propriété des logarithmes utilisée :**

$$\log(a \times b) = \log(a) + \log(b)$$

Exemple numérique donné en cours : $100 = 10^2 \Rightarrow \log_{10}(100) = 2$
soit en thermes générale : ${}x = 10^y \implies \log_{10}(x)=y{}$

