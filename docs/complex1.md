

## Complex I model[^Gauthier2013A]

Assuming single electron transfer for each cycle.

$$
\begin{aligned}
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
k_{42}^\prime &= k_{42} \\
a_{42} &= k_{42}^\prime [O_2] \\
K_{eq}^{ROS} &= \text{exp}((E_{FMN} - E_{sox}) / V_T) \\
a_{24} &= a_{42} K_{eq}^{ROS} [O_2^{ \cdot  -}]_m  \\
a_{25} &= a_{52} = 0  \\
\end{aligned}
$$

$$
\begin{aligned}
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
\end{aligned}
$$

$$
\begin{aligned}
Δ &= e_{1} + e_{2} + e_{3} + e_{4} + e_{5} + e_{6} + e_{7}  \\
\rho_{C1}^\prime &= \rho_{C1}  \cdot mt_{prot} / \Delta  \\
J_{Hres}^{C1} &= 2\rho_{C1}^\prime (e_{6}a_{61} - e_{1}a_{16}) \\
J_{Q}^{C1} &= 0.5\rho_{C1}^\prime (e_{4}a_{47} - e_{7}a_{74}) \\
J_{NADH}^{C1} &= 0.5\rho_{C1}^\prime (e_{3}a_{34} - e_{4}a_{43}) \\
J_{ROS}^{C1} &= \rho_{C1}^\prime (e_{4}a_{42} - e_{2}a_{24})  \\
\end{aligned}
$$


#### Parameters

| Parameter      | Value     | Units       | Desc.                                        |
| -------------- | --------- | ----------- | -------------------------------------------- |
| $\rho_{C1}$    | 8.849     | mM          | Concentration of complex I<br />(Adjustable) |
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
| $E_{FMN}$      | -375      | mV          | Midpoint potential of flavin mononucleotide  |
| $E_{sox}$      | -150      | mV          | Midpoint potential of superoxide             |

[^Gauthier2013A]: Gauthier LD, Greenstein JL, O’Rourke B, Winslow RL. An Integrated Mitochondrial ROS Production and Scavenging Model: Implications for Heart Failure. Biophysical Journal. 2013;105(12):2832-2842. doi:10.1016/j.bpj.2013.11.007. [PMC3882515](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3882515)
