## Creatine kinase

Van Beek's model[^vanBeek2007] for both mitochondrial IMS and cytosolic compartments. 

Parameters were optimized by Hettling's work.[^Hettling2011]

`ATP + Cr = ADP + PCr`

$$
\begin{aligned}
J_{CK} &= (V_f AB^{'} - V_b PQ) / \Delta  \\
\Delta &= 1 + A + B + P + Q + AB^{'} + P^{'}Q + PB^{''} \\
A &= [ATP] / K_{ia}   \\
B &= [Cr] / K_{ib}    \\
B^{'} &= [Cr] / K_{b} \\
B^{''} &= [Cr] / K_{Ib} \\
P &= [ADP] / K_{ic}   \\
P^{'} &= [ADP] / K_{c}\\
Q &= [PCr] / K_{id}
\end{aligned}
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
\begin{aligned}
J_{diff}^{X} &= R_{X}([X]_{ims} - [X]_{cyt})  \\
\text{For X} &\in \{ ATP,\ ADP, \ Cr, \ PCr \} 
\end{aligned}
$$
Since the diffusion rate is the same for ATP/ADP pair, and Cr/PCr pair, respectively. We can deduce more conservation relationships.
$$
\begin{aligned}
\Sigma [A]_{ims} &= [ATP]_{ims} + [ADP]_{ims}  \\
\Sigma [A]_{cyt} &= [ATP]_{cyt} + [ADP]_{cyt}  \\
\Sigma [Cr]_{ims} &= [Cr]_{ims} + [CrP]_{ims}  \\
\Sigma [Cr]_{cyt} &= [Cr]_{cyt} + [CrP]_{cyt}  \\
\end{aligned}
$$


| Parameter           | Value     | Unit | Desc.                                                                                |
| ------------------- | --------- | ---- | ------------------------------------------------------------------------------------ |
| $R_{ATP}$           | 23.64     | Hz   | conductance of ATP                                                                   |
| $R_{ADP}$           | $R_{ATP}$ | Hz   | conductance of ADP                                                                   |
| $R_{PCr}$           | 155       | Hz   | conductance of PCr                                                                   |
| $R_{Cr}$            | $R_{PCr}$ | Hz   | conductance of Cr                                                                    |
| $R_{Pi}$            | 195.63    | Hz   | conductance Pi                                                                       |
| $V_{cyto}$          | 3         | -    | Relative volume of cytosol. <br />Volume of 1 corresponds to $V_{mito}$=0.153mL/gww. |
| $V_{mito}$          | 1         | -    | Relative volume of mitochondrial matrix.                                             |
| $V_{ims}$           | 0.25      | -    | Relative volume of intermembrane space.                                              |
| $\Sigma[A]_{cyt}$   | 5.665     | mM   | Sum of cytosolic adenylate                                                           |
| $\Sigma[A]_{ims}$   | 5.665     | mM   | Sum of intermembrane space adenylate                                                 |
| $\Sigma [Cr]_{cyt}$ | 15.5      | mM   | Pool of cytosolic creatine                                                           |
| $\Sigma [Cr]_{ims}$ | 15.5      | mM   | Pool of intermembrane space creatine                                                 |

## ODEs for High-energy and inorganic phosphates

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



[^vanBeek2007]: Kongas O, van Beek JHGM Creatine kinase in energy metabolic signaling in muscle Nature Precedings (2007)DOI: https://doi.org/10.1038/npre.2007.1317.1

[^Hettling2011]: Hettling, H., & van Beek, J. H. G. M. (2011). Analyzing the functional properties of the creatine kinase system with multiscale “sloppy” modeling. PLoS Computational Biology, 7(8), e1002130.