## Luczak et al., Mitochondrial CaMKII causes metabolic reprogramming, energetic insufficiency, and dilated cardiomyopathy

### Simulation conditions

| Parameters                                      | WT   | CKmito | mtCaMKII | mtCaMKII x CKmito | Source         |
| ----------------------------------------------- | ---- | ------ | -------- | ----------------- | -------------- |
| Complex I expression/activity                   | 100% | 100%   | 45%      | 70%               | Fig. 5E and 5H |
| CKmito expression/activity                      | 100% | 120%   | 80%      | 120%              | Fig. 4E and 4F |
| cytosolic ATP hydrolysis                        | 100% | 100%   | 100%     | 100%              |                |
| TCA cycle enzyme activity (IDH, αKGDH, FH, MDH) | 100% | 100%   | 120%     | 120%              | Fig. 6B        |
| Complex II expression/activity                  | 100% | 100%   | 130%     | 130%              | Fig. 5E        |
| diastolic cytosolic calcium                     | 100% | 100%   | 120%     | 100%              | Fig. 3E        |
| peak cytosolic calcium                          | 100% | 100%   | 105%     | 100%              | Fig. 3E        |

### Model validation

The model is constructed by integrating two computational models: van Beek 2007 creatine kinase model[^van Beek 2007] and Gauthier 2013 cardiac bioenergetic model[^Gauthier2013A]. The model parameters were directly taken from these two model unless stated otherwise. The metabolite steady state levels in the control group were matched to the original model as a model validation.



## Ordinary Differential Equations[^van Beek 2007]


$$
\begin{equation}
\frac{d\left[ Ca^{2+}\right]_{mito}}{dt} =\delta _{Ca}( V_{uni} -V_{NaCa})
\end{equation}
$$

$$
\begin{equation}
\frac{d[ADP]_{mito}}{dt} =V_{ANT} -V_{ATPase} -V_{SL}
\end{equation}
$$

$$
\begin{equation}
\frac{d\Delta \Psi _{m}}{dt} =\frac{V_{He} +V_{He(SDH)} -V_{Hu} -V_{ANT} -V_{Hleak} -V_{NaCa} -V_{uni} -V_{IMAC}}{C_{mito}}
\end{equation}
$$

$$
\begin{equation}
\frac{d[NADH]_{mito}}{dt} =V_{O_{2}} +V_{IDH} +V_{KGDH} +V_{MDH} -V_{THD}
\end{equation}
$$

$$
\begin{equation}
\frac{d\left[ H^{+}\right]_{mito}}{dt} =\delta _{M}( -V_{He} -V_{He(SDH)} +V_{Hu} +V_{NaH} +V_{PiC} +V_{Hleck})
\end{equation}
$$

$$
\begin{equation}
\frac{d[Pi]_{mito}}{dt} =-V_{ATPase} +V_{PiC} -V_{SL}
\end{equation}
$$

$$
\begin{equation}
\frac{d[ISOC]}{dt} =V_{ACO} -V_{IDH} -V_{IDH_{-} NADP}
\end{equation}
$$

$$
\begin{equation}
\frac{d[\alpha KG]}{dt} =V_{IDH} +V_{IDH_{-} NADP} -V_{KGDH} +V_{ATT}
\end{equation}
$$

$$
\begin{equation}
\frac{d[SCoA]}{dt} =V_{KGDH} -V_{SL}
\end{equation}
$$

$$
\begin{equation}
\frac{d[Suc]}{dt} =V_{SL} -V_{O_{2} SDH}
\end{equation}
$$

$$
\begin{equation}
\frac{d[FUM]}{dt} =V_{o_{2} SHH} -V_{FH}
\end{equation}
$$

$$
\begin{equation}
\frac{d[MAL]}{dt} =V_{FH} -V_{MDH}
\end{equation}
$$

$$
\begin{equation}
\frac{d[OAA]}{dt} =V_{MDH} -V_{CS} -V_{AAT}
\end{equation}
$$

$$
\begin{equation}
\frac{d[NADPH]_{m}}{dt} =V_{IDH_{-} NADP} +V_{THD} -V_{GRm} -V_{TxRm}
\end{equation}
$$

$$
\begin{equation}
\frac{d\left[ O_{2}^{\bullet -}\right]_{mito}}{dt} =\operatorname{shunt}( V_{O_{2}} +V_{O_{2} SDH}) -V_{MnSOD} -V^{Tr}_{ROS}
\end{equation}
$$

$$
\begin{equation}
\frac{d\left[ O_{2}^{\bullet -}\right]_{cyto}}{dt} =\frac{v_{m}}{v_{i}} V^{Tr}_{ROS} -V_{CuZnSOD}
\end{equation}
$$

$$
\begin{equation}
\frac{d[ H_{2} O_{2}]_{mito}}{dt} =V_{MnSOD} -V_{difH_{2} O_{2}} -V_{GPXm} -V_{TxPXm}
\end{equation}
$$

$$
\begin{equation}
\frac{d[ H_{2} O_{2}]_{cyto}}{dt} =V_{CuZnSOD} +\frac{v_{m}}{v_{i}} V_{difH_{2} O_{2}} -V_{GPXi} -V_{TxPXi} -V_{CAT}
\end{equation}
$$

$$
\frac{d[GSH]_{mito}}{dt} =V_{GRm} -V_{GPXm} -V_{GRXm} +V_{GST} -V_{PSSGm}
$$

$$
\frac{d[GSH]_{cyto}}{dt} =V_{GRi} -V_{GPXi} -V_{GRXi} +\frac{v_{m}}{v_{i}} V_{GST} -V_{PSSGi}
$$

$$
\frac{d[GSSG]_{mito}}{dt} =0.5( V_{GPXm} -V_{GRm}) +V_{GRXm}
$$

$$
\frac{d[ Trx( SH)_{2}] }{dt}\ =\ V_{TrxR} \ -\ V_{TxPx}   \\ 
$$

$$
\frac{d[ Prx( SH)_{2}] }{dt}\ =\ V_{TxPx} \ -\ V_{Prx} \\
$$

$$
\frac{d[PSSG]_{mito}}{dt} =V_{PSSGm} -V_{GRXm}
$$

$$
\frac{d[PSSG]_{cyto}}{dt} =V_{PSSGi} -V_{GRXi}
$$

$$
\begin{align}
\frac{d[Q]_n}{dt} &= v_5 - v_{7,ox}- v_{7,rd} - v_1  \\
\frac{d[Q^{ \cdot -}]_n}{dt} &= v_{7,ox} + v_{7,rd} - v_{8,ox}- v_{8,rd}  \\
\frac{d[QH_2]_n}{dt} &= v_{8,ox} + v_{8,rd} + v_1 - v_2   \\
\frac{d[QH_2]_p}{dt} &= v_2 -v_3 \\
\frac{d[Q^{ \cdot -}]_p}{dt} &= v_3 - v_{10} - v_{10b} - v_{4,ox} - v_{4,rd}   \\
\frac{d[Q]_p}{dt} &= v_{10} + v_{10b} + v_{4,ox} + v_{4,rd} - v_5   \\
\frac{d[b1]}{dt} &= v_{7,ox} + v_{8,ox} - v_{4,ox}    \\
\frac{d[b2]}{dt} &= v_{4,ox} + v_{7,rd} - v_{8,rd} - v_6   \\
\frac{d[b3]}{dt} &= v_6 - v_{4,rd} + v_{7,ox} - v_{8,ox}    \\

\frac{d[FeS]_{ox}}{dt} &= v_9 - v_3      \\
\frac{d[cytc1]_{ox}}{dt} &= v_{33} - v_9   \\
\frac{d[cytc]_{ox}}{dt} &= V_e - v_{33}   \\\end{align}
$$

$$
\frac{d[ADP]_{ims}}{dt}=(-J_{syn} -J_{CK,Mi} -j_{diff,ATP} )/V_{ims}
$$

$$
\frac{d[ATP]_{ims}}{dt} =(J_{syn} -J_{CK,Mi} -j_{diff,ATP} )/V_{ims}
$$

$$
\frac{d[Cr]_{ims}}{dt}=(-J_{CK,Mi} -j_{diff,Cr} )/V_{ims}
        \\
$$

$$
\frac{d[PCr]_{ims}}{dt}=(J_{CK,Mi} -j_{diff,PCr} )/V_{ims}
$$

$$
\frac{d[PCr]_{cyt}}{dt}
=(J_{CK,MM} +J_{diff,PCr} )/V_{cyt}
$$

$$
\frac{d[ADP]_{cyt}}{dt}
=(J_{hyd} +J_{CK,MM} +J_{diff,ADP} )/V_{cyt}    \\
$$

$$
\frac{d[ATP]_{cyt}}{dt}
=(-J_{hyd} -J_{CK,MM} +J_{diff,ATP} )/V_{cyt}    \\
$$

$$
\frac{d[Cr]_{cyt}}{dt}
=(-J_{CK,MM} +J_{diff,Cr} )/V_{cyt} \\
$$

$$
\frac{d[Pi]_{ims}}{dt}=(-J_{syn} -j_{diff,Pi} )/V_{ims}
$$

$$
\frac{d[Pi]_{cyt}}{dt}=(J_{hyd} +J_{diff,Pi} )/V_{cyt}
$$

$$
\frac{d[ATP]_{mito}}{dt} =-V_{ANT}+V_{ATPase} +V_{SL}
$$







## Simulation protocol 

#### The ATP hydrolysis pulse[^van Beek2007]

$$
\begin{align}


J_{hyd} =H_{ATP,max} \  6t/t_{cycle} \ \ \ \ \ for\ \ \ \ \ 0< t< \frac {t_{cycle}}{6} \\

J_{hyd} =H_{ATP,max} \  [1-6(t/t_{cycle} -1/6)]\ \ \ \ \ for\ \ \ \ \ \frac {t_{cycle}}{6}< t< \frac {t_{cycle}}{3}  \\

J_{hyd} =0\ \ \ \ \ for\ \ \ \ \ \frac {t_{cycle}}{3}  < t< t_{cycle} \\
\end{align}
$$

$H_{ATP,max}=0.003mM/sec$ 

$t_{cycle} =120ms$



#### Cytosolic calcium pulse

$$
\begin{align}
Ca_{i}=t/t_{cycle}(Ca_{i,Amp}-Ca_{i,rest})/t_{Ca,peak}+Ca_{i,rest} \ \ \ for\ \ \ 0< t<t_{Ca,peak} \\
Ca_{i}=Ca_{i,Amp}- (Ca_{i,Amp}-Ca_{i,rest})(t/t_{cycle}-t_{Ca,peak})/(t_{cycle}-t_{Ca,peak})
\ \ \ \ for \ \  t>t_{Ca,peak} \\
\end{align}
$$



Cytosolic calcium is set around 1E-4 to 3E-4mM, and the heart rate is set at 120ms/beat ($t_{cycle}=120ms$).

$t_{Ca,peak}=0.3t_{cycle}$



## Creatine kinase system[^van Beek 2007]

$$
\begin{align}
V_{CK} =C_{CK}*(V_{f}\frac{ATP\cdotp Cr}{K_{ia} K_{B}} -V_{b}\frac{ADP\cdotp PCr}{K_{ic} K_{d}} )/DEN_{CK}  \\

DEN_{CK} =1+\frac{Cr}{K_{ib}} +\frac{PCr}{K_{id}} +ATP(\frac{1}{K_{ia}} +\frac{Cr}{K_{ia} K_{b}} )+ADP(\frac{1}{K_{ic}} +\frac{PCr}{K_{id} K_{c}} +\frac{Cr}{K_{ic} K_{Ib}} )\\

J_{syn} =V_{ATPase}   \\



J_{diff,ATP} =R_{ATP}( \frac{ATP_{ims}}{V_{ims}}\ -ATP{cyt})\\

J_{diff,ADP} =R_{ADP}( ADP_{ims} -ADP)\\

J_{diff,PCr} =R_{PCr}( PCr_{ims} -PCr) \\

J_{diff,Cr} =R_{Cr}( Cr_{ims} -Cr)  \\

J_{diff,Pi} =R_{Pi}( Pi_{ims} -Pi)  \\


\end{align}
$$



$$
\begin{align}


J_{hyd} =H_{ATP(max)} \  6t/t_{cycle} \ \ \ \ \ for\ \ \ \ \ 0< t< 1/6 t_{cycle} \\

J_{hyd} =H_{ATP(max)} \  [1-6(t/t_{cycle} -1/6)]\ \ \ \ \ for\ \ \ \ \ 1/6\ t_{cycle} < t< 1/3 t_{cycle} \\

J_{hyd} =0\ \ \ \ \ for\ \ \ \ \ 1/3 t_{cycle} < t< t_{cycle} \\
\end{align}
$$


| Parameter      | Value                                | Units | Desc.                                                        |
| -------------- | ------------------------------------ | ----- | ------------------------------------------------------------ |
| MiCK           |                                      |       | mitochondrial creatine kinase enzyme                         |
| $V_{max,Mi,f}$ | 2.658E-3                             | mM/ms | maximum velocity in the forward direction (PCr production)   |
| $V_{max,Mi,b}$ | calculated                           | mM/ms | maximum velocity in the backward direction (ATP production); Vb/Vf = 4.199 |
| $K_{ia, Mi}$   | 7.1532E-1                            | mM    | binary dissociation constant ATP                             |
| $K_{ib, Mi}$   | 2.8733E1                             | mM    | binary dissociation constant Cr                              |
| $K_{ic, Mi}$   | 2.017E-1                             | mM    | binary dissociation constant ADP                             |
| $K_{id, Mi}$   | 1.5977                               | mM    | binary dissociation constant PCr                             |
| $K_{b, Mi}$    | 5.209                                | mM    | ternary dissociation constant Cr                             |
| $K_{d, Mi}$    | 4.99E-1                              | mM    | ternary dissociation constant PCr                            |
| $K_{c, Mi}$    | $K_{ic, Mi}$$K_{d, Mi}$/$K_{id, Mi}$ | mM    | ternary dissociation constant ADP                            |
| $K_{Ib, Mi}$   | $K_{ib, Mi}$                         | mM    | ternary dissociation constant Cr from dead end complex       |
| $C_{CK, Mi}$   | 1                                    |       | mitochondrial creatine kinase activity                       |
|                |                                      |       |                                                              |
| MMCK           |                                      |       | cytosol creatine kinase enzyme  (MiCK activity is about 15% of the total CK activity in heart) |
| $V_{max,MM,f}$ | 6.996E-3                             | mM/ms | maximum velocity in the forward direction (PCr production)   |
| $V_{max,MM,b}$ | calculated                           | mM/ms | maximum velocity in the backward direction (ATP production)  |
| $K_{ia, MM}$   | 9E-1                                 | mM    | binary dissociation constant ATP                             |
| $K_{ib, MM}$   | 1.55E1                               | mM    | binary dissociation constant Cr                              |
| $K_{ic, MM}$   | 2.224E-1                             | mM    | binary dissociation constant ADP                             |
| $K_{id, MM}$   | 1.670                                | mM    | binary dissociation constant PCr                             |
| $K_{b, MM}$    | 3.49E1                               | mM    | ternary dissociation constant Cr                             |
| $K_{d, MM}$    | 4.73                                 | mM    | ternary dissociation constant PCr                            |
| $K_{c, MM}$    | $K_{ic, Mi}$$K_{d, Mi}$/$K_{id, Mi}$ | mM    | ternary dissociation constant ADP                            |
| $K_{Ib, MM}$   | $K_{ib, Mi}$                         | mM    | ternary dissociation constant Cr from dead end complex       |
| $C_{CK, MM}$   | 1                                    |       | cytosol creatine kinase activity                             |
|                |                                      |       |                                                              |
| Permeability   |                                      |       |                                                              |
| $R_{ATP}$      | 8.16                                 | Hz    | diffusional conductance ATP                                  |
| $R_{ADP}$      | 65.2227                              | Hz    | diffusional conductance ADP                                  |
| $R_{PCr}$      | 24615                                | Hz    | diffusional conductance PCr                                  |
| $R_{Cr}$       | 1166.7                               | Hz    | diffusional conductance Cr                                   |
| $R_{Pi}$       | 6.0318                               | Hz    | diffusional conductance Pi                                   |
| $V_{cyto}$     | 3                                    |       | Fractional volume of cytosol. Total volume 1 corresponds to $V_{mito}$=0.153mL/gww. |
| $V_{ims}$      | 1/4                                  |       | Fractional volume of intermembrane space.                    |

[^van Beek 2007]: Kongas O, van Beek JHGM Creatine kinase in energy metabolic signaling in muscle Nature Precedings (2007)DOI: https://doi.org/10.1038/npre.2007.1317.1



## Common parameters

| Parameter               | Value   | Unit    | Desc.                                          |
| ----------------------- | ------- | ------- | ---------------------------------------------- |
| F                       | 96485   | C/mol   | Faraday constant                               |
| T                       | 310     | K       | Absolute temperature                           |
| R                       | 8.314   | J/molK  | Universal gas constant                         |
| $V_T$                   | 26.71   | mV      | Thermal voltage (=${RT}/{F}$)                  |
| $C_m$                   | 1.0     | μF/cm^2 | Plasma membrane capacitance                    |
| $C_{mito}$              | 1.812   | mM/V    | Mitochondrial inner membrane capacitance       |
| $pH_i$                  | 7       |         | Cytosolic pH                                   |
| $pH_m$                  | 7.3-7.8 |         | Mitochondrial pH                               |
| $\ce{[O2]}$             | 6       | μM      | Tissue oxygen concentration                    |
| $\ce{[Mg^2+]}_i$        | 1.0     | mM      | Cytosolic magnesium concentration              |
| $\ce{[Mg^2+]}_m$        | 0.4     | mM      | Mitochondrial magnesium concentration          |
| $$\Sigma\ce{[Pi]}_m$$   |         | mM      | Sum of mitochondrial inorganic phosphate       |
| $\Sigma{\ce{[N]}}$      | 1       | mM      | Sum of mitochondrial NAD and NADH              |
| $\Sigma\ce{[A]}_m$      |         | mM      | Sum of mitochondrial ATP and ADP  (Cm)         |
| $\Sigma\ce{[A]}_i$      |         | mM      | Sum of cytosolic ATP and ADP  (Catp)           |
| $\Sigma{\ce{[NADP]_m}}$ | 0.1     | mM      | Sum of mitochondrial NADPH plus NADP (VNADPHm) |



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



## Acid-base equilibria and binding polynomials[^Wei2011]

For both cytoplasmic and mitochondrial compartments.
$$
\begin{align}P_{ATP} &= 1 + \frac{\ce{[H^+]}}{K_{a}^{ATP}} + \frac{\ce{[Mg^2+]}}{K_{Mg}^{ATP}}  \\P_{ADP} &= 1 + \frac{\ce{[H^+]}}{K_{a}^{ADP}} + \frac{\ce{[Mg^2+]}}{K_{Mg}^{ADP}}  \\P_{Pi} &= 1 + \frac{\ce{[H^+]}}{K_{a}^{Pi}}      \\P_{SUC} &= 1 + \frac{\ce{[H^+]}}{K_{a}^{SUC}}    \\P_{H_2O} &= 1 + \frac{\ce{[H^+]}}{K_w}     \\\ce{[OH^-]} &= K_{A}^{H_2O} / \ce{[H^+]}     \\\ce{[ATP^4-]} &= \Sigma ATP / P_{ATP}   \\\ce{[ADP^3-]} &= \Sigma ADP / P_{ADP}   \\\ce{[HPO4^2-]} &= \Sigma Pi / P_{Pi}   \\\ce{[HATP^3-]} &= \ce{[ATP^4-]} \frac{\ce{[H^+]}}{K_{a}^{ATP}}  \\\ce{[HADP^2-]} &= \ce{[ADP^3-]} \frac{\ce{[H^+]}}{K_{a}^{ADP}}  \\\ce{[H2PO4-]} &= \ce{[HPO4^2-]} \frac{\ce{[H^+]}}{K_{a}^{Pi}} \\\ce{[MgATP^2-]} &= \ce{[ATP^4-]} \frac{\ce{[Mg^2+]}}{K_{Mg}^{ATP}}  \\\ce{[MgADP^-]} &= \ce{[ADP^3-]} \frac{\ce{[Mg^2+]}}{K_{Mg}^{ADP}}  \\\end{align}
$$

| Parameter       | Value | Unit | Description                                  |
| --------------- | ----- | ---- | -------------------------------------------- |
| $\delta_H$      | 1E-5  | -    | mitochondria $\ce{[H^+]}$ buffering capacity |
| $pK_{a}^{ATP}$  | 6.48  | -    | pK of ATP acid dissociation constant         |
| $pK_{a}^{ADP}$  | 6.38  | -    | pK of ADP acid dissociation constant         |
| $pK_{a}^{Pi}$   | 6.75  | -    | pKa of phosphate acid dissociation constant  |
| $pK_{Mg}^{ATP}$ | 4.19  | -    | pK of ATP magnesium dissociation constant    |
| $pK_{Mg}^{ADP}$ | 3.25  | -    | pK of ADP magnesium dissociation constant    |
| $pK_{a}^{SUC}$  | 5.2   | -    | pK of succinic acid dissociation constant    |
| $pKw$           | 14    |      | pK of water acid dissociation constant       |



## Phosphate carrier[^Wei2011]

Follows equilibrium random Bi:Bi reaction kinetics 

$$
\begin{align}
J_{PiC} &= c_{PiC}(V_fAB - V_bPQ) / \Delta  \\
A &= \ce{[HPO_4^2-]}_i / K_{pi,i} \\
P &= \ce{[HPO_4^2-]}_m / K_{pi,m} \\
Q &= \ce{[OH^-]}_i / K_{OH,i} \\
B &= \ce{[OH^-]}_m / K_{OH,m} \\
\Delta &= 1 + A + B + P + Q + AB + PQ \\
V_b &= \frac{V_fK_{pi,m}K_{OH,i}}{K_{eq}K_{pi,i}K_{OH,m}}
\end{align}
$$

| Parameter  | Value   | Unit | Desc.                                     |
| ---------- | ------- | ---- | ----------------------------------------- |
| $K_{pi,i}$ | 11.06   | mM   | Extra-matrix Pi binding constant          |
| $K_{pi,m}$ | 11.06   | mM   | Mitochondrial matrix Pi binding constant  |
| $K_{OH,i}$ | 4.08E-5 | mM   | Extra-matrix OH- binding constant         |
| $K_{OH,m}$ | 4.08E-5 | mM   | Mitochondrial matrix OH- binding constant |
| $V_f$      | 1.5     | Hz   | Forward rate                              |
| $c_{PiC}$  | 4.9     | mM   | PiC activity                              |
| $K_{eq}$   | 1       | -    | Equilibrium constant of PiC               |



## Mitochondrial Sodium-hydrogen exchanger (mNHE)[^Wei2011]

Following Smith and Crampin's model of counterpart on the plasma membrane

$$
\begin{align}
J_{NHE} &= c_{NHE} f_h \frac{β^+_1β^+_2-β^-_1β^-_2}{β^+_1 + β^+_2 + β^-_1 + β^-_2}\\
f_h &= \frac{(\ce{[H^+]}_i)^n}{(\ce{[H^+]}_i)^n + K_i^n} \\
A &= \ce{[Na^+]}_m / K_{Na}  \\
B &= \ce{[H^+]}_i / K_{H}  \\
P &= \ce{[Na^+]}_i / K_{Na}  \\
Q &= \ce{[H^+]}_m / K_{H}  \\
β^+_1 &= \frac{k_1^+ A}{1 + A + Q}  \\
β^-_1 &= \frac{k^-_1 P}{1 + P + B}   \\
β^+_2 &= \frac{k_4^+ B}{1 + P + B}  \\
β^-_2 &= \frac{k^-_4 Q}{1 + A + Q}   \\
k_4^- &= \frac{k_1^+ k_4^+}{K_{eq} k_1^-}
\end{align}
$$

| Parameter   | Value   | Unit | Desc.                           |
| ----------- | ------- | ---- | ------------------------------- |
| $c_{NHE}$   | 0.00785 | mM   | NHE concentration               |
| $K_{Na}$    | 24      | mM   | Na Dissociation constant        |
| $K_H$       | 158.5   | nM   | H Dissociation constant         |
| $K_i$       | 3.02    | nM   | Proton binding constant         |
| $n$         | 3       | -    | Hill coefficient for H+ binding |
| $k_{1}^{+}$ | 25.2    | Hz   | NHE forward rate constant       |
| $k_{1}^{-}$ | 42.9    | Hz   | NHE backward rate constant      |
| $k_{4}^{+}$ | 160     | Hz   | NHE forward rate constant       |
| $K_{eq}$    | 1       | -    | Equilibrium constant of NHE     |

## Adenine Nucleotide translocator (ANT) [^Wei2011]

$$
\begin{align}
J_{ANT} &= V_{max}\frac{AB - \delta PQ}{(B + \delta^h P)(A + Q)}  \\
A &= \ce{[ATP^4-]}_m  \\
B &= \ce{[ADP^3-]}_i  \\
P &= \ce{[ATP^4-]}_i  \\
Q &= \ce{[ADP^3-]}_m  \\
\delta &= \text{exp}(-F\Delta\Psi_m / V_T)
\end{align}
$$



| Parameter | Value | Unit     | Desc.            |
| --------- | ----- | -------- | ---------------- |
| $V_{max}$ | 3.15  | mM * kHz | Maximal rate     |
| $h$       | 0.5   | -        | Fraction of dpsi |

## Mitochondrial calcium uniporter (MCU)[^Wei2011]

$$
\begin{align}
J_{uni} &= V_{max} \frac{S (1+S)^3}{(1+S)^4 + L(1 + A)^n} \frac{\delta}{e^\delta-1}  \\
S &= \ce{[Ca^2+]}_i / K_{trans}  \\
A &= \ce{[Ca^2+]}_i / K_{act}    \\
\delta &= -Z_{Ca} (\Delta\Psi_m - \Delta\Psi_0) / V_T
\end{align}
$$

| Parameter      | Value | Unit  | Desc.                              |
| -------------- | ----- | ----- | ---------------------------------- |
| $V_{max}$      | 4.46  | mM*Hz | Maximal rate                       |
| $\Delta\Psi_0$ | 91    | mV    | Offset potential                   |
| $K_{act}$      | 0.38  | μM    | Activation constant for calcium    |
| $K_{trans}$    | 19    | μM    | Dissociation constant for calcium  |
| n              | -2.8  | -     | Activation cooperativity           |
| L              | 110   | -     | Keq for conformational transitions |

## Mitochondrial sodium-calcium exchanger (NCLX)[^Wei2011]

$$
\begin{align}
J_{NCLX} &= V_{max}\text{exp}(b\Delta\Psi_m/V_T)\frac{[Ca^{2+}]_m}{[Ca^{2+}]_i} (\frac{A}{1+A})^n \frac{B}{1+B}  \\
A &= \ce{[Na^+]}_i / K_{Na}  \\
B &= \ce{[Ca^2+]}_m / K_{Ca}  \\
\end{align}
$$

| Parameter | Value | Unit  | Desc. |
| --------- | ----- | ----- | ----- |
| $V_{max}$ | 0.183 | mM*Hz |       |
| b         | 0.5   | -     |       |
| $K_{Na}$  | 9.4   | mM    |       |
| $K_{Ca}$  | 0.375 | μM    |       |
| $n$       | 3     |       |       |

## Mitochondrial proton leak

$$
J_{hleak} = g_H\Delta\Psi_m
$$

| Parameter | Value | Unit    | Desc.                                   |
| --------- | ----- | ------- | --------------------------------------- |
| $g_{H}$   | 2     | mM*Hz/V | Ionic conductance of the inner membrane |



## Mitochondrial hydrogen flux balance[^Wei2011]

$J_H$: Proton influx to mitochondrial matrix by pumps / transporters
$J_{Hn}$: Proton flux due to enzyme stoichiometry
$J_{HL}$: Proton flux due to ligand binding / unbinding
$$
\begin{aligned}
J_H &= -J_{He} - J_{HSDH} + J_{hu} + J_{NHE} + J_{PiC} + J_{Hleak}   \\
J_{Hn} &= -(J_{IDH} + J_{KGDH} + J_{MDH} - J_{F1Fo})   \\
J_{HL} &= \frac{[H^+]_m}{K_{a, ATP}P_{ATP}}\frac{d[ATP]_m}{dt} + \frac{[H^+]_m}{K_{a, ADP}P_{ADP}}\frac{d[ADP]_m}{dt} + \frac{[H^+]_m}{K_{a, Pi}P_{Pi}}\frac{d[Pi]_m}{dt} + \frac{[H^+]_m}{K_{a, SUC}P_{SUC}}\frac{d[SUC]_m}{dt}   \\
\frac{d[H^+]_m}{dt} &= δ_H(J_H - J_{Hn} - J_{HL})   \\
\end{aligned}


$$





## Complex I model[^Gauthier2013A]

Assuming single electron transfer for each cycle.

$$
\begin{align}
\nu &= \text{exp}((\Delta\Psi_m - \Delta\Psi_B) / V_T) \\
a_{12} &= k_{12} ([H^+]_m)^2 \\
a_{21} &= k_{21} \\
a_{65} &= k_{65} ([H^+]_i)^2  \\
a_{56} &= k_{56} \\
a_{61} &= k_{61} / \nu \\
a_{16} &= k_{16} \nu  \\
a_{23} &= k_{23} \sqrt{[NADH]} \\
a_{32} &= k_{32}  \\
a_{34} &= k_{34}  \\
a_{43} &= k_{43} \sqrt{[NAD^+]}  \\
a_{47} &= C1_{inhib}  \cdot K_{47} \sqrt{[Q_n][H^+]_m} \\
a_{74} &= k_{74} \\
a_{57} &=  C1_{inhib}  \cdot K_{57} \sqrt{[QH_2]} \\
a_{75} &= k_{75} \\
k_{42}^\prime &= k_{42} (1 + k_{RC}[DOX])  \\
a_{42} &= k_{42}^\prime [O_2] \\
K_{eq}^{ROS} &= \text{exp}((E_{FMN} - E_{sox}) / V_T) \\
a_{24} &= a_{42} K_{eq}^{ROS} [O_2^{ \cdot  -}]_m  \\
a_{25} &= a_{52} = 0  \\
\end{align}
$$

$$
\begin{align}
e_{1} &=
a_{21} \cdot a_{32} \cdot a_{42} \cdot a_{56} \cdot a_{61} \cdot a_{74} +
a_{21} \cdot a_{32} \cdot a_{42} \cdot a_{56} \cdot a_{61} \cdot a_{75} +
a_{21} \cdot a_{32} \cdot a_{42} \cdot a_{57} \cdot a_{61} \cdot a_{74}  \\ &+
a_{21} \cdot a_{32} \cdot a_{42} \cdot a_{57} \cdot a_{65} \cdot a_{74} +
a_{21} \cdot a_{32} \cdot a_{43} \cdot a_{56} \cdot a_{61} \cdot a_{74} +
a_{21} \cdot a_{32} \cdot a_{43} \cdot a_{56} \cdot a_{61} \cdot a_{75}  \\ &+
a_{21} \cdot a_{32} \cdot a_{43} \cdot a_{57} \cdot a_{61} \cdot a_{74} +
a_{21} \cdot a_{32} \cdot a_{43} \cdot a_{57} \cdot a_{65} \cdot a_{74} +
a_{21} \cdot a_{32} \cdot a_{47} \cdot a_{56} \cdot a_{61} \cdot a_{75}  \\ &+
a_{21} \cdot a_{34} \cdot a_{42} \cdot a_{56} \cdot a_{61} \cdot a_{74} +
a_{21} \cdot a_{34} \cdot a_{42} \cdot a_{56} \cdot a_{61} \cdot a_{75} +
a_{21} \cdot a_{34} \cdot a_{42} \cdot a_{57} \cdot a_{61} \cdot a_{74}  \\ &+
a_{21} \cdot a_{34} \cdot a_{42} \cdot a_{57} \cdot a_{65} \cdot a_{74} +
a_{21} \cdot a_{34} \cdot a_{47} \cdot a_{56} \cdot a_{61} \cdot a_{75} +
a_{23} \cdot a_{34} \cdot a_{47} \cdot a_{56} \cdot a_{61} \cdot a_{75}  \\ &+
a_{24} \cdot a_{32} \cdot a_{47} \cdot a_{56} \cdot a_{61} \cdot a_{75} +
a_{24} \cdot a_{34} \cdot a_{47} \cdot a_{56} \cdot a_{61} \cdot a_{75}  \\
e_{2} &=
a_{12} \cdot a_{32} \cdot a_{42} \cdot a_{56} \cdot a_{61} \cdot a_{74}  +
a_{12} \cdot a_{32} \cdot a_{42} \cdot a_{56} \cdot a_{61} \cdot a_{75}  +
a_{12} \cdot a_{32} \cdot a_{42} \cdot a_{57} \cdot a_{61} \cdot a_{74}  \\ &+
a_{12} \cdot a_{32} \cdot a_{42} \cdot a_{57} \cdot a_{65} \cdot a_{74}  +
a_{12} \cdot a_{32} \cdot a_{43} \cdot a_{56} \cdot a_{61} \cdot a_{74}  +
a_{12} \cdot a_{32} \cdot a_{43} \cdot a_{56} \cdot a_{61} \cdot a_{75}  \\ &+
a_{12} \cdot a_{32} \cdot a_{43} \cdot a_{57} \cdot a_{61} \cdot a_{74}  +
a_{12} \cdot a_{32} \cdot a_{43} \cdot a_{57} \cdot a_{65} \cdot a_{74}  +
a_{12} \cdot a_{32} \cdot a_{47} \cdot a_{56} \cdot a_{61} \cdot a_{75}  \\ &+
a_{12} \cdot a_{34} \cdot a_{42} \cdot a_{56} \cdot a_{61} \cdot a_{74}  +
a_{12} \cdot a_{34} \cdot a_{42} \cdot a_{56} \cdot a_{61} \cdot a_{75}  +
a_{12} \cdot a_{34} \cdot a_{42} \cdot a_{57} \cdot a_{61} \cdot a_{74}  \\ &+
a_{12} \cdot a_{34} \cdot a_{42} \cdot a_{57} \cdot a_{65} \cdot a_{74}  +
a_{12} \cdot a_{34} \cdot a_{47} \cdot a_{56} \cdot a_{61} \cdot a_{75}  +
a_{16} \cdot a_{32} \cdot a_{42} \cdot a_{57} \cdot a_{65} \cdot a_{74}  \\ &+
a_{16} \cdot a_{32} \cdot a_{43} \cdot a_{57} \cdot a_{65} \cdot a_{74}  +
a_{16} \cdot a_{34} \cdot a_{42} \cdot a_{57} \cdot a_{65} \cdot a_{74}  \\
e_{3} &=
a_{12} \cdot a_{23} \cdot a_{42} \cdot a_{56} \cdot a_{61} \cdot a_{74}   +
a_{12} \cdot a_{23} \cdot a_{42} \cdot a_{56} \cdot a_{61} \cdot a_{75}   +
a_{12} \cdot a_{23} \cdot a_{42} \cdot a_{57} \cdot a_{61} \cdot a_{74}   \\ &+
a_{12} \cdot a_{23} \cdot a_{42} \cdot a_{57} \cdot a_{65} \cdot a_{74}   +
a_{12} \cdot a_{23} \cdot a_{43} \cdot a_{56} \cdot a_{61} \cdot a_{74}   +
a_{12} \cdot a_{23} \cdot a_{43} \cdot a_{56} \cdot a_{61} \cdot a_{75}   \\ &+
a_{12} \cdot a_{23} \cdot a_{43} \cdot a_{57} \cdot a_{61} \cdot a_{74}   +
a_{12} \cdot a_{23} \cdot a_{43} \cdot a_{57} \cdot a_{65} \cdot a_{74}   +
a_{12} \cdot a_{23} \cdot a_{47} \cdot a_{56} \cdot a_{61} \cdot a_{75}   \\ &+
a_{12} \cdot a_{24} \cdot a_{43} \cdot a_{56} \cdot a_{61} \cdot a_{74}   +
a_{12} \cdot a_{24} \cdot a_{43} \cdot a_{56} \cdot a_{61} \cdot a_{75}   +
a_{12} \cdot a_{24} \cdot a_{43} \cdot a_{57} \cdot a_{61} \cdot a_{74}   \\ &+
a_{12} \cdot a_{24} \cdot a_{43} \cdot a_{57} \cdot a_{65} \cdot a_{74}   +
a_{16} \cdot a_{21} \cdot a_{43} \cdot a_{57} \cdot a_{65} \cdot a_{74}   +
a_{16} \cdot a_{23} \cdot a_{42} \cdot a_{57} \cdot a_{65} \cdot a_{74}   \\ &+
a_{16} \cdot a_{23} \cdot a_{43} \cdot a_{57} \cdot a_{65} \cdot a_{74}   +
a_{16} \cdot a_{24} \cdot a_{43} \cdot a_{57} \cdot a_{65} \cdot a_{74}   \\
e_{4} &=
a_{12} \cdot a_{23} \cdot a_{34} \cdot a_{56} \cdot a_{61} \cdot a_{74}   +
a_{12} \cdot a_{23} \cdot a_{34} \cdot a_{56} \cdot a_{61} \cdot a_{75}   +
a_{12} \cdot a_{23} \cdot a_{34} \cdot a_{57} \cdot a_{61} \cdot a_{74}   \\ &+
a_{12} \cdot a_{23} \cdot a_{34} \cdot a_{57} \cdot a_{65} \cdot a_{74}   +
a_{12} \cdot a_{24} \cdot a_{32} \cdot a_{56} \cdot a_{61} \cdot a_{74}   +
a_{12} \cdot a_{24} \cdot a_{32} \cdot a_{56} \cdot a_{61} \cdot a_{75}   \\ &+
a_{12} \cdot a_{24} \cdot a_{32} \cdot a_{57} \cdot a_{61} \cdot a_{74}   +
a_{12} \cdot a_{24} \cdot a_{32} \cdot a_{57} \cdot a_{65} \cdot a_{74}   +
a_{12} \cdot a_{24} \cdot a_{34} \cdot a_{56} \cdot a_{61} \cdot a_{74}   \\ &+
a_{12} \cdot a_{24} \cdot a_{34} \cdot a_{56} \cdot a_{61} \cdot a_{75}   +
a_{12} \cdot a_{24} \cdot a_{34} \cdot a_{57} \cdot a_{61} \cdot a_{74}   +
a_{12} \cdot a_{24} \cdot a_{34} \cdot a_{57} \cdot a_{65} \cdot a_{74}   \\ &+
a_{16} \cdot a_{21} \cdot a_{32} \cdot a_{57} \cdot a_{65} \cdot a_{74}   +
a_{16} \cdot a_{21} \cdot a_{34} \cdot a_{57} \cdot a_{65} \cdot a_{74}   +
a_{16} \cdot a_{23} \cdot a_{34} \cdot a_{57} \cdot a_{65} \cdot a_{74}   \\ &+
a_{16} \cdot a_{24} \cdot a_{32} \cdot a_{57} \cdot a_{65} \cdot a_{74}   +
a_{16} \cdot a_{24} \cdot a_{34} \cdot a_{57} \cdot a_{65} \cdot a_{74}   \\
e_{5} &=  
a_{12} \cdot a_{23} \cdot a_{34} \cdot a_{47} \cdot a_{61} \cdot a_{75}   +
a_{12} \cdot a_{23} \cdot a_{34} \cdot a_{47} \cdot a_{65} \cdot a_{75}   +
a_{12} \cdot a_{24} \cdot a_{32} \cdot a_{47} \cdot a_{61} \cdot a_{75}   \\ &+
a_{12} \cdot a_{24} \cdot a_{32} \cdot a_{47} \cdot a_{65} \cdot a_{75}   +
a_{12} \cdot a_{24} \cdot a_{34} \cdot a_{47} \cdot a_{61} \cdot a_{75}   +
a_{12} \cdot a_{24} \cdot a_{34} \cdot a_{47} \cdot a_{65} \cdot a_{75}   \\ &+
a_{16} \cdot a_{21} \cdot a_{32} \cdot a_{42} \cdot a_{65} \cdot a_{74}   +
a_{16} \cdot a_{21} \cdot a_{32} \cdot a_{42} \cdot a_{65} \cdot a_{75}   +
a_{16} \cdot a_{21} \cdot a_{32} \cdot a_{43} \cdot a_{65} \cdot a_{74}   \\ &+
a_{16} \cdot a_{21} \cdot a_{32} \cdot a_{43} \cdot a_{65} \cdot a_{75}   +
a_{16} \cdot a_{21} \cdot a_{32} \cdot a_{47} \cdot a_{65} \cdot a_{75}   +
a_{16} \cdot a_{21} \cdot a_{34} \cdot a_{42} \cdot a_{65} \cdot a_{74}   \\ &+
a_{16} \cdot a_{21} \cdot a_{34} \cdot a_{42} \cdot a_{65} \cdot a_{75}   +
a_{16} \cdot a_{21} \cdot a_{34} \cdot a_{47} \cdot a_{65} \cdot a_{75}   +
a_{16} \cdot a_{23} \cdot a_{34} \cdot a_{47} \cdot a_{65} \cdot a_{75}   \\ &+
a_{16} \cdot a_{24} \cdot a_{32} \cdot a_{47} \cdot a_{65} \cdot a_{75}   +
a_{16} \cdot a_{24} \cdot a_{34} \cdot a_{47} \cdot a_{65} \cdot a_{75}   \\
e_{6} &=  
a_{12} \cdot a_{23} \cdot a_{34} \cdot a_{47} \cdot a_{56} \cdot a_{75} +
a_{12} \cdot a_{24} \cdot a_{32} \cdot a_{47} \cdot a_{56} \cdot a_{75}   +
a_{12} \cdot a_{24} \cdot a_{34} \cdot a_{47} \cdot a_{56} \cdot a_{75}   \\ &+
a_{16} \cdot a_{21} \cdot a_{32} \cdot a_{42} \cdot a_{56} \cdot a_{74}   +
a_{16} \cdot a_{21} \cdot a_{32} \cdot a_{42} \cdot a_{56} \cdot a_{75}   +
a_{16} \cdot a_{21} \cdot a_{32} \cdot a_{42} \cdot a_{57} \cdot a_{74}   \\ &+
a_{16} \cdot a_{21} \cdot a_{32} \cdot a_{43} \cdot a_{56} \cdot a_{74}   +
a_{16} \cdot a_{21} \cdot a_{32} \cdot a_{43} \cdot a_{56} \cdot a_{75}   +
a_{16} \cdot a_{21} \cdot a_{32} \cdot a_{43} \cdot a_{57} \cdot a_{74}   \\ &+
a_{16} \cdot a_{21} \cdot a_{32} \cdot a_{47} \cdot a_{56} \cdot a_{75}   +
a_{16} \cdot a_{21} \cdot a_{34} \cdot a_{42} \cdot a_{56} \cdot a_{74}   +
a_{16} \cdot a_{21} \cdot a_{34} \cdot a_{42} \cdot a_{56} \cdot a_{75}   \\ &+
a_{16} \cdot a_{21} \cdot a_{34} \cdot a_{42} \cdot a_{57} \cdot a_{74}   +
a_{16} \cdot a_{21} \cdot a_{34} \cdot a_{47} \cdot a_{56} \cdot a_{75}   +
a_{16} \cdot a_{23} \cdot a_{34} \cdot a_{47} \cdot a_{56} \cdot a_{75}   \\ &+
a_{16} \cdot a_{24} \cdot a_{32} \cdot a_{47} \cdot a_{56} \cdot a_{75}   +
a_{16} \cdot a_{24} \cdot a_{34} \cdot a_{47} \cdot a_{56} \cdot a_{75}   \\
e_{7} &=  
a_{12} \cdot a_{23} \cdot a_{34} \cdot a_{47} \cdot a_{56} \cdot a_{61} +
a_{12} \cdot a_{23} \cdot a_{34} \cdot a_{47} \cdot a_{57} \cdot a_{61}   +
a_{12} \cdot a_{23} \cdot a_{34} \cdot a_{47} \cdot a_{57} \cdot a_{65}   \\ &+
a_{12} \cdot a_{24} \cdot a_{32} \cdot a_{47} \cdot a_{56} \cdot a_{61}   +
a_{12} \cdot a_{24} \cdot a_{32} \cdot a_{47} \cdot a_{57} \cdot a_{61}   +
a_{12} \cdot a_{24} \cdot a_{32} \cdot a_{47} \cdot a_{57} \cdot a_{65}   \\ &+
a_{12} \cdot a_{24} \cdot a_{34} \cdot a_{47} \cdot a_{56} \cdot a_{61}   +
a_{12} \cdot a_{24} \cdot a_{34} \cdot a_{47} \cdot a_{57} \cdot a_{61}   +
a_{12} \cdot a_{24} \cdot a_{34} \cdot a_{47} \cdot a_{57} \cdot a_{65}   \\ &+
a_{16} \cdot a_{21} \cdot a_{32} \cdot a_{42} \cdot a_{57} \cdot a_{65}   +
a_{16} \cdot a_{21} \cdot a_{32} \cdot a_{43} \cdot a_{57} \cdot a_{65}   +
a_{16} \cdot a_{21} \cdot a_{32} \cdot a_{47} \cdot a_{57} \cdot a_{65}   \\ &+
a_{16} \cdot a_{21}choco  \cdot a_{34} \cdot a_{42} \cdot a_{57} \cdot a_{65}   +
a_{16} \cdot a_{21} \cdot a_{34} \cdot a_{47} \cdot a_{57} \cdot a_{65}   +
a_{16} \cdot a_{23} \cdot a_{34} \cdot a_{47} \cdot a_{57} \cdot a_{65}   \\ &+
a_{16} \cdot a_{24} \cdot a_{32} \cdot a_{47} \cdot a_{57} \cdot a_{65}   +
a_{16} \cdot a_{24} \cdot a_{34} \cdot a_{47} \cdot a_{57} \cdot a_{65}   \\
\end{align}
$$

$$
\begin{align}
Δ &= e_{1} + e_{2} + e_{3} + e_{4} + e_{5} + e_{6} + e_{7}  \\
\rho_{C1}^\prime &= \rho_{C1}  \cdot mt_{prot} / \Delta  \\
J_{Hres}^{C1} &= 2\rho_{C1}^\prime (e_{6}a_{61} - e_{1}a_{16}) \\
J_{Q}^{C1} &= 0.5\rho_{C1}^\prime (e_{4}a_{47} - e_{7}a_{74}) \\
J_{NADH}^{C1} &= 0.5\rho_{C1}^\prime (e_{3}a_{34} - e_{4}a_{43}) \\
J_{ROS}^{C1} &= \rho_{C1}^\prime (e_{4}a_{42} - e_{2}a_{24})  \\
\end{align}
$$


#### Parameters

| Parameter      | Value     | Units       | Desc.                                        |
| -------------- | --------- | ----------- | -------------------------------------------- |
| $\rho_{C1}$    | 8849      | μ           | Concentration of complex I<br />(Adjustable) |
| $\Delta\Psi_B$ | 50        | mV          | Phase boundary potential                     |
| $k_{12}$       | 6.3396E11 | Hz/mM^2     |                                              |
| $k_{21}$       | 5         | Hz          |                                              |
| $k_{56}$       | 100       | Hz          |                                              |
| $k_{65}$       | 2.5119E13 | Hz/mM^2     |                                              |
| $k_{61}$       | 1E7       | Hz          |                                              |
| $k_{16}$       | 130       | Hz          |                                              |
| $k_{23}$       | 3886.7    | Hz/mM^{1/2} |                                              |
| $k_{32}$       | 9.1295E6  | Hz          |                                              |
| $k_{34}$       | 639.1364  | Hz          |                                              |
| $k_{43}$       | 3.2882    | Hz/mM^{1/2} |                                              |
| $k_{47}$       | 1.5962E7  | Hz/mM       |                                              |
| $k_{74}$       | 65.2227   | Hz          |                                              |
| $k_{75}$       | 24615     | Hz          |                                              |
| $k_{57}$       | 1166.7    | Hz/mM^{1/2} |                                              |
| $k_{42}$       | 6.0318    | Hz/mM       |                                              |
| $E_{FMN}$      | -0.375    | V           | Midpoint potential of flavin mononucleotide  |
| $E_{sox}$      | -0.15     | V           | Midpoint potential of superoxide             |



## Complex II (Succinate dehydrogenase)[^Gauthier2013A]



$$
\begin{align}
f_Q &= \frac{[Q]_n}{[Q]_n + [QH_2]_n}  \\
f_{OAA} &= \frac{K_i}{[OAA] + K_i} \\
f_{SUC} &= 0.085 \sqrt{[SUC] / [FUM]} \\
J_{SDH} &= V_{SDH} C2_{inhib} f_{SUC} f_{OAA} \frac{f_Q}{f_Q + K_m}  \\
J_{c2} &= J_{SDH} \\
\end{align}
$$

| Parameter | Value | Units | Desc.                                |
| --------- | ----- | ----- | ------------------------------------ |
| $V_{SDH}$ | 4.167 | mMHz  | Maximum rate of SDH                  |
| $K_i$     | 0.150 | mM    | Inhibition constant for oxaloacetate |
| $K_m$     | 0.6   | -     | Michaelis constant for CoQ           |



## Complex III[^Gauthier2013A]

$$
\begin{align}
f_{hi} & = [H^+]_{i}  / 10^{-7}M   \\
v_{1} &= v_{Q}^{C1} + v_{Q}^{C2}   \\
v_2 &= k_d([QH_2]_{n} - [QH_2]_{p})  \\
k_{3} &= k_{03}K_{eq3}f_{hi} \\
k_{-3} &= k_{03} \\
v_{3} &= k_3[QH_2]_{p} [FeS]_{ox} - k_{-3}[Q^{ \cdot  -}]_{p} [FeS]_{rd}  \\
k_{4, ox} &= k_{04}K_{eq4, ox} \text{exp}(-\alpha\delta_1\Delta\Psi_m / V_T) \\
k_{4, rd} &= k_{04}K_{eq4, rd} \text{exp}(-\alpha\delta_1\Delta\Psi_m / V_T) \\
k_{-4, ox} &= k_{04} \text{exp}(\alpha(1-\delta_1)\Delta\Psi_m / V_T)  \\
k_{-4, rd} &= k_{04} \text{exp}(\alpha(1-\delta_1)\Delta\Psi_m / V_T)  \\
v_{4, ox} &= k_{4, ox}[Q^{ \cdot -}]_{p} [b1] - k_{-4, ox}[Q]_{p} [b2]  \\
v_{4, rd} &= k_{4, rd}[Q^{ \cdot -}]_{p} [b3] - k_{-4, rd}[Q]_{p} [b4]  \\
v_{5} &= k_d([Q]_{p} - [Q]_{n})  \\
k_{6} &= K_{06}K_{eq6}\text{exp}(-\beta\delta_2\Delta\Psi_m / V_T) \\
k_{-6} &= k_{06} \text{exp}(\beta(1-\delta_2)\Delta\Psi_m / V_T)  \\
v_{6} &= k_{6} [b2] - k_{-6} [b3]  \\
k_{7, ox} &= k_{07, ox}K_{eq7, ox}\text{exp}(-\gamma\delta_3\Delta\Psi_m / V_T) \\
k_{7, rd} &= k_{07, rd}K_{eq7, rd}\text{exp}(-\gamma\delta_3\Delta\Psi_m / V_T) \\
k_{-7, ox} &= k_{07, ox} \text{exp}(\gamma(1-\delta_3)\Delta\Psi_m / V_T)  \\
k_{-7, rd} &= k_{07, rd} \text{exp}(\gamma(1-\delta_3)\Delta\Psi_m / V_T)  \\
v_{7, ox} &= (k_{7, ox}[Q]_{n}[b3] - k_{-7, ox}[Q^{ \cdot  -}]_{n}[b1])C3_{inhib} \\
v_{7, rd} &= (k_{7, rd}[Q]_{n}[b4] - k_{-7, rd}[Q^{ \cdot  -}]_{n}[b2])C3_{inhib} \\
f_{hm} & = [H^+]_{m}   / 10^{-7}M  \\
k_{8, ox} &= k_{08, ox}K_{eq8, ox}\text{exp}(-\gamma\delta_3\Delta\Psi_m / V_T)(f_{hm})^2  \\
k_{8, rd} &= k_{08,rd}K_{eq8, rd}\text{exp}(-\gamma\delta_3\Delta\Psi_m / V_T)(f_{hm})^2  \\
k_{-8, ox} &= k_{08, ox} \text{exp}(\gamma(1-\delta_3)\Delta\Psi_m / V_T)  \\
k_{-8, rd} &= k_{08, rd} \text{exp}(\gamma(1-\delta_3)\Delta\Psi_m / V_T)  \\
v_{8, ox} &= (k_{8, ox}[Q^{ \cdot  -}]_{n}[b3] - k_{-8, ox}[QH_2]_{n}[b1])C3_{inhib} \\
v_{8, rd} &= (k_{8, rd}[Q^{ \cdot  -}]_{n}[b4] - k_{-8, rd}[QH_2]_{n}[b2])C3_{inhib} \\
k_9 &= k_{09}K_{eq9}  \\
k_{-9} &= k_{09} \\
v_{9} &= k_{9}[FeS]_{rd}[cytc1]_{ox} - k_{-9}[FeS]_{ox}[cytc1]_{rd}\\
k_{10} &= k_{010}K_{eq10}  \\
k_{-10} &= k_{010} \\
v_{10} &= k_{10}[Q^{ \cdot  -}]_p[O_2] - k_{-10}[Q]_p[O_2^{ \cdot -}]  \\
v_{10b} &= v_{10}  \\
v_{33} &= k_{33}(K_{eq}[cytc1]_{rd}[cytc]_{ox} - [cytc]_{rd}[cytc1]_{ox})  \\
\rho_{C3}^\prime &= \rho_{C3} \cdot mt_{prot}  \\
\rho_{C4}^\prime &= \rho_{C4} \cdot mt_{prot}  \\
FeS_{rd} &= \rho_{C3}^\prime - FeS_{ox} \\
cytc1_{rd} &= \rho_{C3}^\prime - cytc1_{ox}  \\
cytc_{rd} &= \rho_{C4}^\prime - cytc_{ox}  \\
 [b4] &= \rho_{C3}^\prime - [b1] - [b2] - [b3]  \\
 [QH_2]_p &= \Sigma[Q] - [Q]_n - [Q]_p - [QH_2]_n - [Q^{ \cdot  -}]_p - [Q^{ \cdot  -}]_n  \\
J_{hRes}^{C3} &= 2v_{3}     \\
J_{ROS, m}^{C3} &= v_{10}   \\
J_{ROS, i}^{C3} &= v_{10b}  \\
\end{align}
$$

ODE System in the Q cycle:

$$
\begin{align}
\frac{d[Q]_n}{dt} &= v_5 - v_{7,ox}- v_{7,rd} - v_1  \\
\frac{d[Q^{ \cdot -}]_n}{dt} &= v_{7,ox} + v_{7,rd} - v_{8,ox}- v_{8,rd}  \\
\frac{d[QH_2]_n}{dt} &= v_{8,ox} + v_{8,rd} + v_1 - v_2   \\
\frac{d[QH_2]_p}{dt} &= v_2 -v_3 \\
\frac{d[Q^{ \cdot -}]_p}{dt} &= v_3 - v_{10} - v_{10b} - v_{4,ox} - v_{4,rd}   \\
\frac{d[Q]_p}{dt} &= v_{10} + v_{10b} + v_{4,ox} + v_{4,rd} - v_5   \\
\frac{d[b1]}{dt} &= v_{7,ox} + v_{8,ox} - v_{4,ox}    \\
\frac{d[b2]}{dt} &= v_{4,ox} + v_{7,rd} - v_{8,rd} - v_6   \\
\frac{d[b3]}{dt} &= v_6 - v_{4,rd} + v_{7,ox} - v_{8,ox}    \\
\frac{d[b4]}{dt} &= v_{4,rd} - v_{7,rd} - v_{8,rd}   \\
\frac{d[FeS]_{ox}}{dt} &= v_9 - v_3      \\
\frac{d[cytc1]_{ox}}{dt} &= v_{33} - v_9   \\
\frac{d[cytc]_{ox}}{dt} &= V_e - v_{33}   \\
\end{align}
$$

#### Parameters

| Parameter    | Value    | Unit  | Desc.                                                     |
| ------------ | -------- | ----- | --------------------------------------------------------- |
| $k_{03}$     | 1,666.63 | Hz/mM | Reverse rate constant for reaction 3                      |
| $K_{eq3}$    | 0.6877   | -     | Equilibrium constant for reaction 3                       |
| $k_{04}$     | 60.67    | Hz/mM | Reverse rate constant for reaction 4                      |
| $K_{eq4,ox}$ | 129.9853 | -     | Equilibrium constant for reaction 4 <br />(bH oxidized)   |
| $K_{eq4,rd}$ | 13.7484  | -     | Equilibrium constant for reaction 4 <br />(bH reduced)    |
| $\delta_1$   | 0.5      | -     |                                                           |
| $\alpha$     | 0.2497   | -     |                                                           |
| $k_d$        | 22000    | Hz    | Rate of diffusion across the membrane <br />for Q and QH2 |
| $k_{06}$     | 166.67   | Hz/mM | Reverse rate constant for reaction 6                      |
| $K_{eq6}$    | 9.4596   | -     | Equilibrium constant for reaction 6                       |
| $\delta_2$   | 0.5      | -     |                                                           |
| $\beta$      | 0.5006   | -     |                                                           |
| $k_{07,ox}$  | 13.33    | Hz/mM | Reverse rate constant for reaction 7 <br />(bL oxidized)  |
| $K_{eq7,ox}$ | 3.0748   | -     | Equilibrium constant for reaction 7 <br />(bL oxidized)   |
| $k_{07,rd}$  | 1.667    | Hz/mM | Reverse rate constant for reaction 7 <br />(bL reduced)   |
| $K_{eq7,rd}$ | 29.0714  | -     | Equilibrium constant for reaction 7 <br />(bL reduced)    |
| $\delta_3$   | 0.5      | -     |                                                           |
| $\gamma$     | 0.2497   | -     | $\alpha + \beta + \gamma = 1$                             |
| $k_{08,ox}$  | 83.33    | Hz/mM | Reverse rate constant for reaction 8 <br />(bL oxidized)  |
| $K_{eq8,ox}$ | 129.9853 | -     | Equilibrium constant for reaction 8 <br />(bL oxidized)   |
| $k_{08,rd}$  | 8.333    | Hz/mM | Reverse rate constant for reaction 8 <br />(bL reduced)   |
| $K_{eq8,rd}$ | 9.4596   | -     | Equilibrium constant for reaction 8 <br />(bL reduced)    |
| $k_{09}$     | 833      | Hz/mM | Reverse rate constant for reaction 9                      |
| $K_{eq9}$    | 0.2697   | -     | Equilibrium constant for reaction 9                       |
| $k_{010}$    | 0.8333   | Hz/mM | Reverse rate constant for reaction 10                     |
| $K_{eq10}$   | 1.4541   | -     | Equilibrium constant for reaction 10                      |
| $k_{33}$     | 2469.13  | Hz/mM | Reverse rate constant for reaction 33                     |
| $K_{eq33}$   | 2.1145   | -     | Equilibrium constant for reaction 33                      |
| $\rho_{C3}$  | 0.325    | mM    | Total complex III protein                                 |



## Complex IV[^Gauthier2013A]

$$
\begin{align}
f_{H_{m}} &= \text{exp}(-\delta_5\Delta\Psi_m / V_T) ([H^+]_m /10^{-7}M) \\
f_{H_{i}} &= \text{exp}((1-\delta_5)\Delta\Psi_m / V_T) ([H^+]_i /10^{-7}M)  \\
f_{C_{rd}} &= [cytc]_{rd} \\
f_{C_{ox}} &= \text{exp}((1-\delta_5)\Delta\Psi_m / V_T) [cytc]_{ox} \\
a_{12} &= k_{34} f_{C_{rd}}^3 f_{H_{m}}^4  \\
a_{14} &= k_{-37} f_{H_{i}}   \\
a_{21} &= k_{-34} f_{C_{ox}}^3 f_{H_{i}}  \\
a_{23} &= k_{35} [O_2] C4_{inhib}  \\
a_{34} &= k_{36} f_{C_{rd}} f_{H_{m}}^3  \\
a_{41} &= k_{37} f_{H_{m}}  \\
a_{43} &= k_{-36} f_{C_{ox}} f_{H_{i}}^2 \\
e_1 &= a_{21}a_{41}a_{34} + a_{41}a_{34}a_{23}  \\
e_2 &= a_{12}a_{41}a_{34}  \\
e_3 &= a_{23}a_{12}a_{41} + a_{43}a_{14}a_{21} + a_{23}a_{43}a_{12} + a_{23}a_{43}a_{14}  \\
e_4 &= a_{14}a_{34}a_{21} + a_{34}a_{23}a_{12} + a_{34}a_{23}a_{14}  \\
\Delta &= e_1 + e_2 + e_3+ e_4  \\
Y &= e_1 / \Delta  \\
Yr &= e_2 / \Delta  \\
YO &= e_3 / \Delta  \\
YOH &= e_4 / \Delta  \\
v_{34} &= \rho_{C4}^\prime (Y  \cdot a_{12} - Yr  \cdot a_{21})  \\
v_{35} &= \rho_{C4}^\prime Yr  \cdot a_{23}  \\
v_{36} &= \rho_{C4}^\prime (YO  \cdot a_{34} - YOH  \cdot a_{43})  \\
v_{37} &= \rho_{C4}^\prime (YOH  \cdot a_{41} - Y  \cdot a_{14})  \\
V_e &= 3v_{34} + v_{35}  \\
J_{hRes}^{C4}  &= v_{34} + 2v_{36} + v_{37}  \\
J_{O_2} &= v_{35}  \\
J_{hRes} &= J_{hRes}^{C1} + J_{hRes}^{C3} + J_{hRes}^{C4} \\
\rho_{C4}^\prime &= \rho_{C4} \cdot mt_{prot}
\end{align}
$$

| Parameter     | Value     | Unit    | Desc.                    |
| ------------- | --------- | ------- | ------------------------ |
| $\Sigma cytc$ | 0.325     | mM      | Cytochrome c pool        |
| $\rho_{C4}$   | 0.325     | mM      | Complex IV concentration |
| $k_{34}$      | 2.9445E10 | Hz/mM^3 | @ pH = 7                 |
| $k_{-34}$     | 290.03    | Hz/mM^3 | @ pH = 7                 |
| $k_{35}$      | 45000     | Hz/mM   |                          |
| $k_{36}$      | 4.826E11  | Hz/mM   | @ pH = 7                 |
| $k_{-36}$     | 4.826     | Hz/mM   | @ pH = 7                 |
| $k_{37}$      | 1.7245E8  | Hz      | @ pH = 7                 |
| $k_{-37}$     | 17.542    | Hz      | @ pH = 7                 |





## Complex V (ATP synthase) rates[^Wei2011]

$$
\begin{align}J_{F1Fo} &= -\rho^{F1} ((100 p_a + p_{c1} v_B) v_a - (p_a + p_{c2} v_a) v_h)  / \Delta \\J_H^{F1Fo} &= -3\rho^{F1} (100p_a(1 + v_a) - (p_a + p_b)v_h) / \Delta \\\Delta &= (1 + p_1 v_a)v_B + (p_2 + p_3 v_a)v_h \\v_B &= \text{exp}(3\Delta\Psi_B / V_T)   \\v_h &= \text{exp}(3\Delta p / V_T)  \\v_a &= {K_{eq}^{'} \ce{[ATP^4-]}_m \over \Sigma \ce{[Pi]}_m(\ce{[ADP^3-]}_m + \ce{[HADP^2-]}_m)} \\\end{align}
$$

| Parameter      | Value     | Unit | Desc.                                            |
| -------------- | --------- | ---- | ------------------------------------------------ |
| $\rho_{F1}$    | 5         | mM   | Concentration of F1-Fo ATPase                    |
| $K_{eq}^{'}$   | 4.1175E6  | M    | Apparent equilibrium constant for ATP hydrolysis |
| $\Delta\Psi_B$ | 50        | mV   | Phase boundary potential                         |
| $p_{a}$        | 1.656E-5  | Hz   |                                                  |
| $p_{b}$        | 3.373E-7  | Hz   |                                                  |
| $p_{c1}$       | 9.651E-14 | Hz   |                                                  |
| $p_{c2}$       | 4.585E-14 | Hz   |                                                  |
| $p_{1}$        | 1.346E-4  | -    |                                                  |
| $p_{2}$        | 7.739E-7  | -    |                                                  |
| $p_{3}$        | 6.65E-15  | -    |                                                  |



## Reactive oxygen species (ROS) scavenging and transport



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





[^Cortassa2004]: Cortassa S, Aon MA, Winslow RL, O'Rourke B. A mitochondrial oscillator dependent on reactive oxygen species. Biophys J. 2004;87(3):2060-73. [PMC1304608](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1304608/)

[^Kembro2013]: Kembro JM, Aon MA, Winslow RL, O'Rourke B, Cortassa S. Integrating mitochondrial energetics, redox and ROS metabolic networks: a two-compartment model. Biophys J. 2013;104(2):332-43. [PMC3552263](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3552263/)



[^Wei2011]: Wei AC, Aon MA, O'Rourke B, Winslow RL, Cortassa S. Mitochondrial energetics, pH regulation, and ion dynamics: a computational-experimental approach. Biophys J. 2011;100(12):2894-903. [PMC3123977](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3123977/)



[^Gauthier2013A]: Gauthier LD, Greenstein JL, O’Rourke B, Winslow RL. An Integrated Mitochondrial ROS Production and Scavenging Model: Implications for Heart Failure. Biophysical Journal. 2013;105(12):2832-2842. doi:10.1016/j.bpj.2013.11.007. [PMC3882515]



[^van Beek 2007]: Kongas O, van Beek JHGM Creatine kinase in energy metabolic signaling in muscle Nature Precedings (2007)DOI: https://doi.org/10.1038/npre.2007.1317.1

