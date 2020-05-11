## Complex V (ATP synthase) rates[^Wei2011]

$$
\begin{align}
J_{F1Fo} &= -\rho^{F1} ((100 p_a + p_{c1} v_B) v_a - (p_a + p_{c2} v_a) v_h)  / \Delta \\
J_H^{F1Fo} &= -3\rho^{F1} (100p_a(1 + v_a) - (p_a + p_b)v_h) / \Delta \\
\Delta &= (1 + p_1 v_a)v_B + (p_2 + p_3 v_a)v_h \\
v_B &= \text{exp}(3\Delta\Psi_B / V_T)   \\
v_h &= \text{exp}(3\Delta p / V_T)  \\
v_a &= {K_{eq}^{'} \ce{[ATP^4-]}_m \over \Sigma \ce{[Pi]}_m(\ce{[ADP^3-]}_m + \ce{[HADP^2-]}_m)} \\
\end{align}
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



[^Wei2011]: Wei AC, Aon MA, O'Rourke B, Winslow RL, Cortassa S. Mitochondrial energetics, pH regulation, and ion dynamics: a computational-experimental approach. Biophys J. 2011;100(12):2894-903. [PMC3123977](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3123977/)

