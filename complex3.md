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




[^Gauthier2013A]: Gauthier LD, Greenstein JL, O’Rourke B, Winslow RL. An Integrated Mitochondrial ROS Production and Scavenging Model: Implications for Heart Failure. Biophysical Journal. 2013;105(12):2832-2842. doi:10.1016/j.bpj.2013.11.007. [PMC](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3882515)

