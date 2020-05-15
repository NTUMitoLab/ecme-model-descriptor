## Creatine kinase

Van Beek's model[^van Beek 2007] for both mitochondrial IMS and cytosolic compartments. 

Parameters were optimized by Hettling's work.[^Hettling2011]
$$
\ce{ATP + Cr <=>[CK] ADP + PCr}
$$

$$
\begin{align}
J_{CK} &= (V_f AB^{'} - V_b PQ) / \Delta  \\
\Delta &= 1 + A + B + P + Q + AB^{'} + P^{'}Q + PB^{''} \\
A &= \ce{[ATP]} / K_{ia}   \\
B &= \ce{[Cr]} / K_{ib}    \\
B^{'} &= \ce{[Cr]} / K_{b} \\
B^{''} &= \ce{[Cr]} / K_{Ib} \\
P &= \ce{[ADP]} / K_{ic}   \\
P^{'} &= \ce{[ADP]} / K_{c}\\
Q &= \ce{[PCr]} / K_{id}
\end{align}
$$

### Mitochondrial CK (miCK)
| Parameter | Value                                      | Unit    | Desc.                                  |
| --------- | ------------------------------------------ | ------- | -------------------------------------- |
| $K_{eq}$  | 151.95                                     | -       | Equilibrium constant for Cr production |
| $V_f$     | 0.77505                                    | mM * Hz | Maximum velocity for PCr production    |
| $V_b$     | $\frac{K_{eq}K_{ic}K_{K_d}}{K_{ia}K_b}V_f$ | mM * Hz | Maximum velocity for Cr production     |
| $K_{ia}$  | 0.75132                                    | mM      | Binary dissociation constant for ATP   |
| $K_b$     | 5.20908                                    | mM      | Ternary dissociation constant Cr       |
| $K_{ic}$  | 0.20173                                    | mM      | Binary dissociation constant ADP       |
| $K_{d}$   | 0.49951                                    | mM      | Ternary dissociation constant PCr      |
| $K_{ib}$  | 28.73344                                   | mM      | Binary dissociation constant Cr        |
| $K_{id}$  | 1.59769                                    | mM      | Binary dissociation constant PCr       |
| $K_{c}$   | $K_{ic}K_{d}/K_{id}$                       | mM      | Ternary dissociation constant ADP      |
| $K_{Ib}$  | $K_{ib}$                                   | mM      | Inhibition constant Cr                 |

### Cytosolic CK (mmCK)
| Parameter | Value                                      | Unit    | Desc.                                  |
| --------- | ------------------------------------------ | ------- | -------------------------------------- |
| $K_{eq}$  | 151.95                                     | -       | Equilibrium constant for Cr production |
| $V_f$     | 7.37307                                    | mM * Hz | Maximum velocity for PCr production    |
| $V_b$     | $\frac{K_{eq}K_{ic}K_{K_d}}{K_{ia}K_b}V_f$ | mM * Hz | Maximum velocity for Cr production     |
| $K_{ia}$  | 1.2624                                     | mM      | Binary dissociation constant for ATP   |
| $K_b$     | 16.74444                                   | mM      | Ternary dissociation constant Cr       |
| $K_{ic}$  | 0.21226                                    | mM      | Binary dissociation constant ADP       |
| $K_{d}$   | 1.66976                                    | mM      | Ternary dissociation constant PCr      |
| $K_{ib}$  | 34.50419                                   | mM      | Binary dissociation constant Cr        |
| $K_{id}$  | 4.51655                                    | mM      | Binary dissociation constant PCr       |
| $K_{c}$   | $K_{ic}K_{d}/K_{id}$                       | mM      | Ternary dissociation constant ADP      |
| $K_{Ib}$  | $K_{ib}$                                   | mM      | Inhibition constant Cr                 |

## Creatine shuttle

Positive direction is from IMS to cytosol.
$$
\begin{align}
J_{diff}^{X} &= R_{X}([X]_{ims} - [X]_{cyt})  \\
\text{For X} &\in \{ ATP,\ ADP, \ Cr, \ PCr \} 
\end{align}
$$
Since the diffusion rate is the same for ATP/ADP pair, and Cr/PCr pair, respectively. We can deduce more conservation relationships.
$$
\begin{align}
\Sigma \ce{[A]_{ims}} &= \ce{[ATP]_{ims}} + \ce{[ADP]_{ims}}  \\
\Sigma \ce{[A]_{cyt}} &= \ce{[ATP]_{cyt}} + \ce{[ADP]_{cyt}}  \\
\Sigma \ce{[Cr]_{ims}} &= \ce{[Cr]_{ims}} + \ce{[CrP]_{ims}}  \\
\Sigma \ce{[Cr]_{cyt}} &= \ce{[Cr]_{cyt}} + \ce{[CrP]_{cyt}}  \\
\end{align}
$$


| Parameter                | Value     | Unit | Desc.                                                        |
| ------------------------ | --------- | ---- | ------------------------------------------------------------ |
| $R_{ATP}$                | 23.64     | Hz   | conductance of ATP                                           |
| $R_{ADP}$                | $R_{ATP}$ | Hz   | conductance of ADP                                           |
| $R_{PCr}$                | 155       | Hz   | conductance of PCr                                           |
| $R_{Cr}$                 | $R_{PCr}$ | Hz   | conductance of Cr                                            |
| $R_{Pi}$                 | 195.63    | Hz   | conductance Pi                                               |
| $V_{cyto}$               | 3         | -    | Relative volume of cytosol. <br />Volume of 1 corresponds to $V_{mito}$=0.153mL/gww. |
| $V_{mito}$               | 1         | -    | Relative volume of mitochondrial matrix.                     |
| $V_{ims}$                | 0.25      | -    | Relative volume of intermembrane space.                      |
| $\Sigma\ce{[A]_{cyt}}$   | 5.665     | mM   | Sum of cytosolic adenylate                                   |
| $\Sigma\ce{[A]_{ims}}$   | 5.665     | mM   | Sum of intermembrane space adenylate                         |
| $\Sigma \ce{[Cr]_{cyt}}$ | 15.5      | mM   | Pool of cytosolic creatine                                   |
| $\Sigma \ce{[Cr]_{ims}}$ | 15.5      | mM   | Pool of intermembrane space creatine                         |



[^van Beek 2007]: Kongas O, van Beek JHGM Creatine kinase in energy metabolic signaling in muscle Nature Precedings (2007)DOI: https://doi.org/10.1038/npre.2007.1317.1

[^Hettling2011]: Hettling, H., & van Beek, J. H. G. M. (2011). Analyzing the functional properties of the creatine kinase system with multiscale “sloppy” modeling. PLoS Computational Biology, 7(8), e1002130.