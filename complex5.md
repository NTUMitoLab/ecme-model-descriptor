## Complex V (ATP synthase) rates[^Wei2011]

$$
\begin{align}
J_{F1Fo} &= -\rho^{F1} ((100 p_a + p_{c1} v_B) v_a - (p_a + p_{c2} v_a) v_h)  / \Delta \\
J_H^{F1Fo} &= -3\rho^{F1} (100p_a(1 + v_a) - (p_a + p_b)v_h) / \Delta \\
\Delta &= (1 + p_1 v_a)v_B + (p_2 + p_3 v_a)v_h \\
v_B &= \text{exp}(3\Delta\Psi_B / V_T)   \\
v_h &= \text{exp}(3\Delta p / V_T)  \\
v_a &= \frac{K_{eq}^{'} \cdot \Sigma[ATP]_m}{ \Sigma[Pi]_m \cdot \Sigma[ADP]_m } \\
\end{align}
$$

| Parameter      | Value     | Unit | Desc.                                                        |
| -------------- | --------- | ---- | ------------------------------------------------------------ |
| $\rho_{F1}$    | 5         | mM   | Concentration of F1-Fo ATPase                                |
| $K_{eq}^{'}$   | 6.47E5    | M    | Apparent equilibrium constant for ATP hydrolysis<br />From Golding's work[^Golding1995] |
| $\Delta\Psi_B$ | 50        | mV   | Phase boundary potential                                     |
| $p_{a}$        | 1.656E-5  | Hz   | Sum of products of rate constants                            |
| $p_{b}$        | 3.373E-7  | Hz   | Sum of products of rate constants                            |
| $p_{c1}$       | 9.651E-14 | Hz   | Sum of products of rate constants                            |
| $p_{c2}$       | 4.585E-14 | Hz   | Sum of products of rate constants                            |
| $p_{1}$        | 1.346E-4  | -    | Sum of products of rate constants                            |
| $p_{2}$        | 7.739E-7  | -    | Sum of products of rate constants                            |
| $p_{3}$        | 6.65E-15  | -    | Sum of products of rate constants                            |



[^Wei2011]: Wei AC, Aon MA, O'Rourke B, Winslow RL, Cortassa S. Mitochondrial energetics, pH regulation, and ion dynamics: a computational-experimental approach. Biophys J. 2011;100(12):2894-903. [PMC3123977](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3123977/)

[^Golding1995]: Golding, E. M., Teague, W. E., & Dobson, G. P. (1995). Adjustment of K’ to varying pH and pMg for the creatine kinase, adenylate kinase and ATP hydrolysis equilibria permitting quantitative bioenergetic assessment. The Journal of Experimental Biology, 198(Pt 8), 1775–1782.