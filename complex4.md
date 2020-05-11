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



[^Gauthier2013A]: Gauthier LD, Greenstein JL, O’Rourke B, Winslow RL. An Integrated Mitochondrial ROS Production and Scavenging Model: Implications for Heart Failure. Biophysical Journal. 2013;105(12):2832-2842. doi:10.1016/j.bpj.2013.11.007. [PMC3882515](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3882515)
