# Ordinary Differential Equations

## Mitochondrial ions
$$
\begin{aligned}
\frac{d [Ca^{2+}]_m}{dt} &=\delta_{Ca}( J_{uni} - J_{NCLX}) \\
\frac{d [Na^+]_m}{dt} &= J_{NCLX} - J_{NaH} \\
\frac{d [H^+]_m}{dt} &= \delta_{H}( -J_{Hres} + J_{Hu} +V_{NaH} + J_{PiC} + J_{Hleak})  \\
\frac{d [Pi]_m}{dt} &= -J_{F1Fo} + J_{PiC} - J_{SL}  \\
C_{m}\frac{d \Delta \Psi_m}{dt} &= J_{Hres} - J_{Hu} - J_{ANT} - J_{Hleak} -J_{NCLX} - J_{uni} - J_{IMAC} \\
\end{aligned}
$$

## Citric acid cycle
$$
\begin{aligned}
\frac{d [ISOC]}{dt} &= J_{ACO} -J_{IDH3} -J_{IDH2}  \\
\frac{d [\alpha KG]}{dt} &= J_{IDH3} + J_{IDH2} - J_{KGDH} + J_{AAT}  \\
\frac{d[SCoA]}{dt} &= J_{KGDH} - J_{SL}  \\
\frac{d [SUC]}{dt} &= J_{SL} - J_{SDH} \\
\frac{d [FUM]}{dt} &= J_{SDH} - J_{FH}  \\
\frac{d[MAL]}{dt} &= J_{FH} - J_{MDH}  \\
\frac{d [OAA]}{dt} & = J_{MDH} - J_{CS} - J_{AAT}  \\
\frac{d [NADH]_m}{dt} &= -J_{C1} + J_{IDH} + J_{KGDH} + J_{MDH} - J_{THD}  \\
\end{aligned}
$$

## ROS transport and scavenging 
$$
\begin{aligned}
\frac{d[ [NADPH]_m}{dt} & = J_{IDH2} + J_{THD} - 0.5J_{GR,m} - J_{TxR, m}  \\
\frac{d [ O_{2}^{ \bullet -}]_{m}}{dt} &= J_{ROS,m} - J_{SOD,m} - J^{Tr}_{ROS}  \\
\frac{d [ O_{2}^{ \bullet -}]_{i}}{dt} &= \frac{V_{mito}}{V_{cyto}} J^{Tr}_{ROS} -J_{SOD,i}  \\
\frac{d [H_2O_2]_m}{dt} &= 0.5J_{SOD,m} - J_{dif,[H_2O_2]} - J_{GPX,m} -J_{TxPX,m}  \\
\frac{d[H_2O_2]_i}{dt} &= 0.5J_{SOD,i} + \frac{V_{mito}}{V_{cyto}}  J_{dif,[H_2O_2]} -J_{GPX,i} -J_{TxPX,i} - J_{CAT}  \\
\frac{d [GSH]_m}{dt} &= J_{GR,m} - J_{GPX,m} - J_{GRX,m} + J_{GST} -J_{PSSG,m}  \\
\frac{d[GSH]_i}{dt} &= J_{GR,i} - J_{GPX,i} - J_{GRX,i} + \frac{V_{mito}}{V_{cyto}} J_{GST} - J_{PSSG,i}  \\
\frac{d [GSSG]_m}{dt} &= 0.5( J_{GPX,m} -J_{GR,m}) + J_{GRX,m}  \\
\frac{d [TrxSH_2]_m}{dt} &= J_{TR,m} - J_{TPX,m}   \\ 
\frac{d [TrxSH_2]_i}{dt} &= J_{TR,i} - J_{TPX,i}   \\ 
\frac{d [PSSG]_m}{dt} &= J_{PSSG,m} - J_{GRX,m}    \\
\frac{d [PSSG]_i}{dt} &= J_{PSSG,i} - J_{GRX,i}    \\
\end{aligned}
$$

## High-energy and inorganic phosphates
$$
\begin{aligned}
\frac{d [ADP]_m}{dt} &= J_{ANT} - J_{F1Fo} - J_{SL}  \\
[ATP]_m &= \Sigma[A]_m - [ADP]_m  \\
V_{ims}\frac{d [ADP]_{ims}}{dt} &= -J_{ANT} + J_{CK}^{Mi} + J_{diff}^{ATP}  \\
[ATP]_{ims} &= \Sigma[A]_{ims} - [ADP]_{ims}  \\
V_{cyto}\frac{d[ADP]_{cyt}}{dt} &= J_{hyd} +J_{CK}^{MM} - J_{diff}^{ATP}    \\
[ATP]_{cyt} &= \Sigma[A]_{cyt} - [ADP]_{cyt}  \\
V_{ims}\frac{d[Cr]_{ims}}{dt} &= -J_{CK}^{Mi} + J_{diff}^{PCr}  \\
[PCr]_{ims} &= \Sigma[Cr]_{ims} - [Cr]_{ims}  \\
V_{cyt}\frac{d [Cr]_{cyt}}{dt} &= -J_{CK}^{MM} - J_{diff}^{PCr}  \\
[PCr]_{cyt} &= \Sigma[Cr]_{cyt} - [Cr]_{cyt}  \\
V_{ims}\frac{d [Pi]_{ims}}{dt} &= -V_{mito} J_{PiC} - J_{diff}^{Pi}  \\
V_{cyt}\frac{d [Pi]_{cyt}}{dt} &= J_{hyd} + J_{diff}^{Pi}
\end{aligned}
$$

## Q cycle
$$
\begin{aligned}
\frac{d[Q]_n}{dt} &= v_5 - v_{7,ox}- v_{7,rd} - v_1  \\
\frac{d[Q^{ \cdot -}]_n}{dt} &= v_{7,ox} + v_{7,rd} - v_{8,ox}- v_{8,rd}  \\
\frac{d[QH_2]_n}{dt} &= v_{8,ox} + v_{8,rd} + v_1 - v_2   \\
\frac{d[QH_2]_p}{dt} &= v_2 -v_3 \\
\frac{d[Q^{ \cdot -}]_p}{dt} &= v_3 - v_{10} - v_{10b} - v_{4,ox} - v_{4,rd}   \\
\frac{d[Q]_p}{dt} &= v_{10} + v_{10b} + v_{4,ox} + v_{4,rd} - v_5   \\
\frac{d[b1]}{dt} &= v_{7,ox} + v_{8,ox} - v_{4,ox}    \\
\frac{d[b2]}{dt} &= v_{4,ox} + v_{7,rd} - v_{8,rd} - v_6   \\
\frac{d[b3]}{dt} &= v_6 - v_{4,rd} + v_{7,ox} - v_{8,ox}    \\
\frac{d[b4]}{dt} &= v_{4,rd} - v_{7,rd} - v_{8,rd}   \\
\frac{d[FeS]_{ox}}{dt} &= v_9 - v_3      \\
\frac{d[cytc1]_{ox}}{dt} &= v_{33} - v_9   \\
\frac{d[cytc]_{ox}}{dt} &= V_e - v_{33}   \\
\end{aligned}
$$

## Sarcoplasmic ion channels

