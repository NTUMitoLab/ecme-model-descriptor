## TCA cycle rates[^Wei2011]

### Citrate synthase (CS)


$$
\begin{align}
J_{CS} &= \frac{k_{cat} E_T AB}{(1+A)(1+B)}  \\
A &= \ce{[AcCoA]} / K_m^{AcCoA} \\
B &= \ce{[OAA]} / K_m^{OAA}
\end{align}
$$

| Parameter        | Value   | Unit | Description                         |
| :--------------- | ------- | ---- | ----------------------------------- |
| $k_{cat}$        | 0.23523 | Hz   | Catalytic constant                  |
| $E_T$            | 400     | μM   | Enzyme concentration of CS          |
| $K_m^{AcCoA}$    | 12.6    | μM   | Michaelis constant for AcCoA        |
| $K_m^{OAA}$      | 0.64    | μM   | Michaelis constant for OAA          |
| $\ce{[AcCoA]}$   | 1000    | μM   | Acetyl CoA concentration            |
| $k_{cat}$ (cell) | 0.15891 | Hz   | Catalytic constant (cellular model) |

### Aconitase (ACO)

$$
\begin{align}
J_{ACO} &= k_f ([CIT] - [ISOC] / K_{eq})  \\
\ [CIT] &= \Sigma_{CAC} - [ISOC] - [\alpha KG]-[SCoA] - [SUC] - [FUM] - [MAL] - [OAA]
\end{align}
$$

| Parameter      | Value    | Unit | Description                            |
| -------------- | -------- | ---- | -------------------------------------- |
| $k_f$          | 0.11688  | Hz   | Forward rate constant of ACO           |
| $K_{eq}$       | 2.22     | -    | Equilibrium constant of ACO            |
| $\Sigma_{CAC}$ | 1300     | μM   | Sum of TCA cycle intermediates         |
| $k_f$ (cell)   | 0.078959 | Hz   | Forward rate constant (cellular model) |

### Isocitrate dehydrogenase, NADH-producing (IDH3)

$$
\begin{align}
J_{IDH3} &= \frac{k_{cat} E_T AB}{f_H AB + f_i B + f_a A + f_a f_i} \\
f_H & = 1 + \frac{[H^+]_m}{K_{H1}} + \frac{K_{H2}}{[H^+]_m}  \\
A &= [NAD] / K_{NAD} \\
B &= ([ISOC] / K_{ISOC})^n  \\
f_a &= \frac{K_A}{K_A + [ADP]_m} \frac{K_{CA}}{K_{CA} + [Ca^{2+}]_m}  \\
f_i &= 1 + \frac{[NADH]}{K_{NADH}}  \\
\end{align}
$$

| Parameter        | Value | Unit | Description                       |
| ---------------- | ----- | ---- | --------------------------------- |
| $k_{cat}$        | 11.88 | kHz  | Rate constant of IDH3             |
| $E_T$            | 109   | μM   | Concentration of IDH3             |
| $K_{H1}$         | 1E-9  | M    | Ionization constant of IDH3       |
| $K_{H2}$         | 9E-7  | M    | Ionization constant of IDH3       |
| $K_{NAD}$        | 923   | μM   | Michaelis constant for NAD        |
| $K_{ISOC}$       | 1520  | μM   | Michaelis constant for isocitrate |
| $n$              | 2     | -    | Cooperativity for isocitrate      |
| $K_A$            | 620   | μM   | Activation constant by ADP        |
| $K_{CA}$         | 0.5   | μM   | Activation constant for calcium   |
| $K_{NADH}$       | 190   | μM   | Inhibition constant by NADH       |
| $k_{cat}$ (cell) | 535   | Hz   | Rate constant (cellular model)    |

### Alpha-ketoglutarate dehydrogenase (KGDH)

$$
\begin{align}
J_{KGDH} &= \frac{k_{cat} E_T AB}{f_H AB + f_a (A + B)} \\
f_H & = 1 + \frac{[H^+]_m}{K_{H1}} + \frac{K_{H2}}{[H^+]_m}  \\
A &= [NAD] / K_{NAD} \\
B &= ([\alpha KG] / K_{AKG})^n  \\
f_a &= \frac{K_{MG}}{K_{MG} + [Mg^{2+}]_m} \frac{K_{CA}}{K_{CA} + [Ca^{2+}]_m}  \\
\end{align}
$$

| Parameter        | Value | Unit | Description                    |
| ---------------- | ----- | ---- | ------------------------------ |
| $k_{cat}$        | 13.2  | Hz   | Rate constant of KGDH          |
| $E_T$            | 500   | μM   | Concentration of KGDH          |
| $K_{H1}$         | 4E-8  | M    | Ionization constant of KGDH    |
| $K_{H2}$         | 7E-8  | M    | Ionization constant of KGDH    |
| $K_{NAD}$        | 38700 | μM   | Michaelis constant for NAD     |
| $K_{AKG}$        | 30000 | μM   | Michaelis constant for αKG     |
| $n$              | 1.2   | -    | Hill coefficient for αKG       |
| $K_{MG}$         | 30.8  | μM   | Activation constant for Mg     |
| $K_{CA}$         | 0.15  | μM   | Activation constant for Ca     |
| $k_{cat}$ (cell) | 17.9  | Hz   | Rate constant (cellular model) |

### Succinate-CoA ligase (SL)

$$
\begin{align}
J_{SL} &= k_f ([SCoA][ADP]_m[Pi]_m - [SUC][ATP]_m[CoA]/K_{eq}^{app}) \\
K_{eq}^{app} &= K_{eq} \frac{P_{SUC}P_{ATP}}{P_{Pi}P_{ADP}}
\end{align}
$$

| Parameter    | Value  | Unit    | Description                            |
| ------------ | ------ | ------- | -------------------------------------- |
| $k_f$        | 0.028  | μM * Hz | Forward rate constant of SL            |
| $K_{eq}$     | 3.115  | -       | Equilibrium constant of SL             |
| [CoA]        | 20     | μM      | Coenzyme A concentration               |
| $k_f$ (cell) | 0.0284 | μM * Hz | Forward rate constant (cellular model) |

### Succinate dehydrogenase (SDH)

See electron transport chain.

### Fumarate hydratase (FH)

$$
J_{FH} = k_f ([FUM] - [MAL] / K_{eq})
$$

| Parameter    | Value | Unit | Description                            |
| ------------ | ----- | ---- | -------------------------------------- |
| $k_f$        | 8.3   | Hz   | Forward rate constant                  |
| $K_{eq}$     | 1.0   | -    | Equilibrium constant                   |
| $k_f$ (cell) | 8.4   | Hz   | Forward rate constant (cellular model) |

### Malate dehydrogenase (MDH)

$$
\begin{align}
J_{MDH} &= \frac{k_{cat} E_T AB f_a f_i}{(1+A)(1+B)}  \\
A &= \frac{[MAL]}{K_{MAL}}\frac{K_{OAA}}{K_{OAA} + [OAA]}  \\
B &= [NAD] / K_{NAD}  \\
f_a &= k_{offset} + \left( 1 + \frac{[H^+]_m}{K_{H1}} (1 + \frac{[H^+]_m}{K_{H2}})    \right)^{-1}  \\
f_i &= \left( 1 + \frac{K_{H3}}{[H^+]_m} (1 + \frac{K_{H4}}{[H^+]_m})    \right)^{2}  \\
\end{align}
$$

| Parameter        | Value    | Units | Description                          |
| ---------------- | -------- | ----- | ------------------------------------ |
| $k_{cat}$        | 124.2    | Hz    | Rate constant                        |
| $E_T$            | 154      | μM    |                                      |
| $K_{H1}$         | 1.131E-8 | M     | Ionization constant                  |
| $K_{H2}$         | 2.67E-2  | M     | Ionization constant                  |
| $K_{H3}$         | 6.68E-12 | M     | Ionization constant                  |
| $K_{H4}$         | 5.62E-9  | M     | Ionization constant                  |
| $k_{offset}$     | 0.0399   |       | Offset of MDH pH activation factor   |
| $K_{NAD}$        | 224.4    | μM    | Michaelis constant for NAD           |
| $K_{MAL}$        | 1493     | μM    | Michaelis constant for malate        |
| $K_{OAA}$        | 31       | μM    | Inhibition constant for oxaloacetate |
| $k_{cat}$ (cell) | 125.9    | Hz    | Rate constant for cellular model     |

### Aspartate aminotransferase (AAT)

$$
J_{AAT} = k_f [OAA][GLU] \frac{k_{ASP}K_{eq}}{k_{ASP}K_{eq} + k_f[\alpha KG]}
$$

| Parameter    | Value  | Units | Description                            |
| ------------ | ------ | ----- | -------------------------------------- |
| $k_f$        | 21.4   | Hz    | Forward rate constant                  |
| $k_{ASP}$    | 0.0015 | Hz    | Rate constant of aspartate consumption |
| $K_{eq}$     | 6.6    |       | Equilibrium constant                   |
| [GLU]        | 30000  | μM    | Glutamate concentration                |
| $k_f$ (cell) | 21.7   | Hz    | Forward rate constant (cellular model) |







[^Wei2011]: Wei AC, Aon MA, O'Rourke B, Winslow RL, Cortassa S. Mitochondrial energetics, pH regulation, and ion dynamics: a computational-experimental approach. Biophys J. 2011;100(12):2894-903. [PMC3123977](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3123977/)
