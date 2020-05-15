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

| Parameter | Value | Units   | Desc.                                |
| --------- | ----- | ------- | ------------------------------------ |
| $V_{SDH}$ | 4.167 | mM * Hz | Maximum rate of SDH                  |
| $K_i$     | 0.150 | mM      | Inhibition constant for oxaloacetate |
| $K_m$     | 0.6   | -       | Michaelis constant for CoQ           |



[^Gauthier2013A]: Gauthier LD, Greenstein JL, O’Rourke B, Winslow RL. An Integrated Mitochondrial ROS Production and Scavenging Model: Implications for Heart Failure. Biophysical Journal. 2013;105(12):2832-2842. doi:10.1016/j.bpj.2013.11.007. [PMC3882515](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3882515)
