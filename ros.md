# Reactive oxygen species (ROS) scavenging and transport



## Catalase (CAT)[^Cortassa2004]

Includes inhibition by high levels of hydrogen peroxide

$$
\begin{align}
V_{CAT} &= 2k_1E_T\ce{[H2O2]}_i \cdot e^{-fr\ce{[H2O2]}_i} \\
\end{align}
$$

| Parameter | Value | Unit  | Desc.                                  |
| --------- | ----- | ----- | -------------------------------------- |
| $k_1$     | 17000 | mM*Hz | Rate constant                          |
| $E_{T}$   | 1     | nM    | Extra-matrix concentration of catalase |
| $fr$      | 0.05  | 1/mM  | Hydrogen peroxide inhibition factor    |

## Superoxide dismutase (SOD) [^Cortassa2004]

Based on McADAM, 1976 model, for both cytosolic and mitochondrial compartments.

$$
\begin{align}
J_{SOD} &= {2k_5E_Tf_{sox}(k_1 + k_3^\prime) \over k_5(2 k_1 + k_3^\prime) + k_3^\prime f_{sox}}   \\
k_3^\prime &= k_3 (1 + \frac{\ce{[H2O2]}}{K_{H_2O_2}})  \\
f_{sox} &= k_1^{SOD} \ce{[O2^-]} \\
\end{align}
$$

| Parameter | Value   | Unit  | Desc.                                  |
| --------- | ------- | ----- | -------------------------------------- |
| $k_1$     | 1200000 | Hz/mM | Rate constant for EA -> EB             |
| $k_3$     | 24000   | Hz/mM | Rate constant for EB -> EC             |
| $k_5$     | 0.24    | Hz    | Rate constant for EC -> EA             |
| $K_{i}$   | 0.5     | mM    | Inhibition constant for H2O2           |
| $E_{T,i}$ | 0.0003  | mM    | Concentration of Cu,ZnSOD (cytosolic)  |
| $E_{T,m}$ | 0.00024 | mM    | Concentration of MnSOD (mitochondrial) |

## Glutathione (GSH) systems[^Cortassa2004]

### Glutathione peroxidase (GPX)

Dalziel type Ping-pong mechanism, for both cytosolic and mitochondrial compartments.
$$
\begin{align}
J_{GPX} &= \frac{E_T}{A + B}      \\
A &= \frac{\Phi_1}{\ce{[H2O2]} }  \\
B & = \frac{\Phi_2}{\ce{[GSH]} }  \\
\end{align}
$$

| Parameter | Value  | Unit | Desc.                       |
| --------- | ------ | ---- | --------------------------- |
| $E_{T,i}$ | 50     | nM   | GPX content (cytosolic)     |
| $E_{T,m}$ | 50     | nM   | GPX content (mitochondrial) |
| $\Phi_1$  | 5E-6   | mM*s | Dalziel coefficient         |
| $\Phi_2$  | 7.5-E4 | mM*s | Dalziel coefficient         |



### Glutathione reductase (GR)

Michaelis-Menten kinetics, for both cytosolic and mitochondrial compartments.


$$
\begin{align}
J_{GR} &= k_1E_T\frac{A}{1+A}\frac{B}{1 + B} \\
A &= \frac{\ce{[GSSG]}}{K_{GSSG}}  \\
B &= \frac{\ce{[NADPH]}}{K_{NADPH}}  \\
\end{align}
$$

| Parameter   | Value | Unit | Desc.                        |
| ----------- | ----- | ---- | ---------------------------- |
| $E_{T,i}$   | 9E-4  | mM   | GR content (cytosolic)       |
| $E_{T,m}$   | 9E-4  | mM   | GR content (mitochondrial)   |
| $k_1$       | 2.5   | Hz   | Catalytic constant of GR     |
| $K_{GSSG}$  | 0.06  | mM   | Michaelis constant for GSSG  |
| $K_{NADPH}$ | 0.015 | mM   | Michaelis constant for NADPH |

### Glutaredoxin system[^Kembro2013]

Disabled in the cellular model.
$$
\begin{align}
J_{GRX} &= V_{max}BC  \\
B &= \frac{\ce{[PSSG]}}{\ce{[PSSG]} + K_{PSSG}}  \\
C &= \frac{A \ce{\Sigma[Grx]}}{A \ce{\Sigma[Grx]} + K_m}   \\
A &= \frac{K_{eq}\ce{[GSH]}^2}{K_{eq}\ce{[GSH]}^2 + \ce{[GSSG]}}
\end{align}
$$

| Parameter          | Value   | Unit  | Desc.                                                        |
| ------------------ | ------- | ----- | ------------------------------------------------------------ |
| $V_{max, i}$       | 3.6E-4  | mM*Hz | Extra-matrix glutaredoxin reaction rate                      |
| $V_{max, m}$       | 3.6E-4  | mM*Hz | Mitochondrial glutaredoxin reaction rate                     |
| $K_{eq}$           | 1.37E-3 | 1/mM  | Equilibrium constant of glutaredoxin                         |
| $K_m$              | 0.01    | mM    | Michaelis constant for GSH of GRX                            |
| $K_{PSSG}$         | 0.0005  | mM    | Michaelis constant for glutathionylated <br />protein of glutaredoxin |
| $\ce{\Sigma[Grx]}$ | 0.002   | mM    | Glutaredoxin concentration                                   |
| $V_{max, i}$       | 0       |       | Cellular model                                               |
| $V_{max, i}$       | 0       |       | Cellular model                                               |

### Glutathionylated protein[^Kembro2013]

Disabled in the cellular model.
$$
\begin{align}
J_{PSSG} &= k_1 E_T (\Sigma\ce{[PSSG]} - \ce{[PSSG]})AB  \\
A &= \frac{\ce{[GSH]}}{\ce{[GSH]} + K_m}  \\
B &= \frac{K_{act}}{\ce{[H2O2]} + K_{act}}
\end{align}
$$

| Parameter           | Value | Unit | Desc.                                                        |
| ------------------- | ----- | ---- | ------------------------------------------------------------ |
| $k_1$               | 640   | Hz   | Rate constant of protein glutathionylation                   |
| $E_T$               | 8E-4  |      | Concentration of proteins that <br />can become glutathionylated |
| $\Sigma\ce{[PSSG]}$ | 1E-3  | mM   | Total PSSG                                                   |
| $K_m$               | 0.75  | mM   | Michaelis constant of GSH                                    |
| $K_{act}$           | 1E-3  | mM   | Activation constant of H2O2                                  |
| $k_{1}$             | 0     |      | Cellular model                                               |

### Glutathione transport[^Kembro2013]

Disabled in the cellular model.
$$
J_{GST} = c_{GST}\frac{\ce{[GSH]}_i-\ce{[GSH]}_m}{\ce{[GSH]}_i + k_{0.5}}
$$

| Parameter | Value  | Unit    | Desc.                                    |
| --------- | ------ | ------- | ---------------------------------------- |
| $c_{GST}$ | 1.5E-5 | mM * Hz | Rate constant of glutathione transporter |
| $k_{0.5}$ | 2.6    | mM      | Transport association constant of GSH    |
| $c_{GST}$ | 0      |         | Cellular model                           |

### Conservation relationship of glutathione

for both cytosolic and mitochondrial compartments.
$$
\Sigma \ce{[GSH]} = \ce{[GSH]} + 2 \ce{[GSSG]}
$$

| Parameter      | Value | Unit | Desc.                  |
| -------------- | ----- | ---- | ---------------------- |
| $\ce{[GSH]}_i$ |       | mM   | Cytosolic GSH pool     |
| $\ce{[GSH]}_m$ |       | mM   | Mitochondrial GSH pool |



## Thioredoxin system[^Kembro2013]

### Peroxiredoxin (TPX)

Dalziel type Ping-pong mechanism, for both cytosolic and mitochondrial compartments.
$$
\begin{align}
J_{GPX} &= \frac{E_T}{A + B}      \\
A &= \frac{\Phi_1}{\ce{[H2O2]} }  \\
B & = \frac{\Phi_2}{\ce{[TrxSH2]} }  \\
\end{align}
$$

| Parameter | Value | Unit   | Desc.                       |
| --------- | ----- | ------ | --------------------------- |
| $E_{T,i}$ | 100   | μM     | GPX content (cytosolic)     |
| $E_{T,m}$ | 3     | μM     | GPX content (mitochondrial) |
| $\Phi_1$  | 3.83  | mM * s | Dalziel coefficient         |
| $\Phi_2$  | 1.85  | mM * s | Dalziel coefficient         |


### Thioredoxin reductase (TR)

Michaelis-Menten kinetics, for both cytosolic and mitochondrial compartments.


$$
\begin{align}
J_{TR} &= k_1E_T\frac{A}{1+A}\frac{B}{1 + B} \\
A &= \frac{\ce{[TrxSS]}}{K_{TrxSS}}  \\
B &= \frac{\ce{[NADPH]}}{K_{NADPH}}  \\
\end{align}
$$

| Parameter   | Value | Unit | Desc.                        |
| ----------- | ----- | ---- | ---------------------------- |
| $E_{T,i}$   | 0.35  | μM   | TR content (cytosolic)       |
| $E_{T,m}$   | 0.35  | μM   | TR content (mitochondrial)   |
| $k_1$       | 22.75 | Hz   | Catalytic constant of GR     |
| $K_{TrxSS}$ | 35    | μM   | Michaelis constant for GSSG  |
| $K_{NADPH}$ | 65    | μM   | Michaelis constant for NADPH |

### Conservation relationship of thioredoxin 

For both cytosolic and mitochondrial compartments.
$$
\ce{[TrxSS]} = \Sigma\ce{[Trx]} - \ce{[TrxSH2]}
$$

| Parameter        | Value | Unit | Desc.                           |
| ---------------- | ----- | ---- | ------------------------------- |
| $\ce{[TrxSS]}_i$ | 25    | μM   | Sum of cytosolic thioreoxin     |
| $\ce{[TrxSS]}_m$ | 50    | μM   | Sum of mitochondrial thioreoxin |



## Inner mitochondrial anion channel[^Cortassa2004]

$$
\begin{align}
g_{IMAC} &= \left( a + b \frac{\ce{[O2-]_i}}{\ce{[O2-]_i} + K_{CC}} \right) \left( G_L + \frac{G_{max}}{1 + e^{κ(\Delta\Psi_m^b + \Delta\Psi_m)}} \right) \\
V_{IMAC} &= g_{IMAC}\Delta\Psi_m \\
V_{tr}^{ROS} &= j \cdot g_{IMAC} \left( \Delta\Psi_m + V_T ln \left( \frac{\ce{[O2-]_m}}{\ce{[O2-]_i}} \right) \right) \\
\end{align}
$$
| Parameter        | Value  | Unit         | Desc.                                 |
| ---------------- | ------ | ------------ | ------------------------------------- |
| a                | 0.001  | -            | Basal IMAC conductance                |
| b                | 10000  | -            | Activation factor by $\ce{[O2-]_i}$   |
| $K_{CC}$         | 10     | μM           | Activation constant by $\ce{[O2-]_i}$ |
| $G_L$            | 0.035  | μM * Hz / mV | Integral conductance for IMAC         |
| $G_{max}$        | 3.9085 | μM * Hz / mV | Leak conductance of IMAC              |
| $\kappa$         | 0.07   | 1/mV         | Steepness factor                      |
| $\Delta\Psi_m^b$ | 4      | mV           | Potential at half saturation          |
| j                | 0.1    | -            | Fraction of IMAC conductance          |



## Hydrogen peroxide transfer[^Kembro2013]

Simple diffusion.

$$
J_{diff}^{H_2O_2} = c_{diff}([\ce{H2O2}]_m - [\ce{H2O2}]_i)
$$

| Parameter  | Value | Unit | Desc.                     |
| ---------- | ----- | ---- | ------------------------- |
| $c_{diff}$ | 0.2   | Hz   | Diffusion rate across IMM |

## Conservation of NADPH

$$
\Sigma{\ce{[NADP]_m}} = \ce{[NADP+]_m} + \ce{[NADPH]_m}
$$



## NADPH-producing isocitrate dehydrogenase (IDH2)[^Kembro2013]

$$
\begin{align}
J_{IDH2} &= f_H \frac{V_f AB - V_b PQ}{(1 + A + P)(1 + B + Q)} \\
A &= \ce{[ISOC]} / K_{m, ISOC}  \\
B &= (\ce{[NADP]}_m + K_{i,NADP}) / K_{m, NADP}  \\
P &= \ce{[\alpha KG]}/ K_{m,\alpha KG}  \\
Q &= \ce{[NADPH]}_m / K_{m, NADPH}      \\
f_H &= \frac{K_H}{K_H + \ce{[H^+]}_m}   \\
\end{align}
$$

| Parameter         | Value | Unit  | Desc.                             |
| ----------------- | ----- | ----- | --------------------------------- |
| $K_{H}$           | 500   | μM    | Dissociation constant for H       |
| $K_{m, ISOC}$     | 3.9   | μM    | Michaelis constant for isocitrate |
| $K_{m, NADP}$     | 6.7   | μM    | Michaelis constant for NADP       |
| $K_{i,NADP}$      | 0.002 | μM    | Inhibition constant for NADP      |
| $K_{m, NADPH}$    | 12    | μM    | Michaelis constant for NADPH      |
| $K_{m,\alpha KG}$ | 510   | μM    | Michaelis constant for αKG        |
| $V_f$             | 87    | μM*Hz | Maximal forward rate of IDH2      |
| $V_b$             | 5.45  | μM*Hz | Maximal backward rate of IDH2     |



## Transhydrogenase (THD)[^Kembro2013]

$$
\begin{align}
J_{THD} &= (V_fAB^{'} - V_bP^{'}Q) / \Delta  \\
\Delta &= 1 + A + B + P + Q + AQ + B^{'}P^{'} + AB^{'} + P^{'}Q \\
A &= \ce{[NADH]} / K_{m,NADH}   \\
B &= \ce{[NADP]}_m / K_{m,NADP}   \\
B^{'} &= B \cdot \text{exp}(x(d-1) \Delta p / V_T) \\
P &= \ce{[NAD]} / K_{m,NAD}  \\
P^{'} &= P  \cdot \text{exp}(xd \Delta p / V_T)  \\
Q &= \ce{[NADPH]_m} / K_{m,NADPH} \\
V_f &= E_T k_a  \\
V_b &= V_f \frac{K_{m,NADP} K_{m,NADH}}{K_{m,NAD} K_{m,NADPH}^{THD} K_{eq}^{App}}  \\
\end{align}
$$

| Parameter      | Value   | Unit | Desc.                         |
| -------------- | ------- | ---- | ----------------------------- |
| $K_{m,NADPH}$  | 20      | μM   | Michaelis constant for NADPH  |
| $K_{m,NADH}$   | 10      | μM   | Michaelis constant for NADH   |
| $K_{m,NAD}$    | 125     | μM   | Michaelis constant for NAD    |
| $K_{m,NADP}$   | 17      | μM   | Michaelis constant for NADP   |
| $E_{T}$        | 0.01187 | μM   | Concentration of THD          |
| $k_{a}$        | 1174.74 | Hz   | Forward catalytic constant    |
| $K_{eq}^{App}$ | 1       | -    | Apparent equilibrium constant |



[^Cortassa2004]:Cortassa S, Aon MA, Winslow RL, O'Rourke B. A mitochondrial oscillator dependent on reactive oxygen species. Biophys J. 2004;87(3):2060-73. [PMC1304608](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1304608/)

[^Kembro2013]:Kembro JM, Aon MA, Winslow RL, O'Rourke B, Cortassa S. Integrating mitochondrial energetics, redox and ROS metabolic networks: a two-compartment model. Biophys J. 2013;104(2):332-43. [PMC3552263](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3552263/)
