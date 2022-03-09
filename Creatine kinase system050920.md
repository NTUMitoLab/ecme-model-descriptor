### Creatine kinase system[^vanBeek2007]

$$
\begin{aligned}
V_{CK} =C_{CK}*(V_{f}\frac{ATP\cdotp Cr}{K_{ia} K_{B}} -V_{b}\frac{ADP\cdotp PCr}{K_{ic} K_{d}} )/DEN_{CK}  \\
DEN_{CK} =1+\frac{Cr}{K_{ib}} +\frac{PCr}{K_{id}} +ATP(\frac{1}{K_{ia}} +\frac{Cr}{K_{ia} K_{b}} )+ADP(\frac{1}{K_{ic}} +\frac{PCr}{K_{id} K_{c}} +\frac{Cr}{K_{ic} K_{Ib}} )\\
J_{syn} =V_{ATPase}   \\
J_{diff,ATP} =R_{ATP}( \frac{ATP_{ims}}{V_{ims}}\ -ATP{cyt})\\
J_{diff,ADP} =R_{ADP}( ADP_{ims} -ADP)\\
J_{diff,PCr} =R_{PCr}( PCr_{ims} -PCr) \\
J_{diff,Cr} =R_{Cr}( Cr_{ims} -Cr)  \\
J_{diff,Pi} =R_{Pi}( Pi_{ims} -Pi)  \\
\end{aligned}
$$



$$
\begin{aligned}
J_{hyd} =H_{ATP(max)} \  6t/t_{cycle} \ \ \ \ \ for\ \ \ \ \ 0< t< 1/6 t_{cycle} \\

J_{hyd} =H_{ATP(max)} \  [1-6(t/t_{cycle} -1/6)]\ \ \ \ \ for\ \ \ \ \ 1/6\ t_{cycle} < t< 1/3 t_{cycle} \\

J_{hyd} =0\ \ \ \ \ for\ \ \ \ \ 1/3 t_{cycle} < t< t_{cycle} \\
\end{aligned}
$$


| Parameter      | Value                                | Units | Desc.                                                                                          |
| -------------- | ------------------------------------ | ----- | ---------------------------------------------------------------------------------------------- |
| MiCK           |                                      |       | mitochondrial creatine kinase enzyme                                                           |
| $V_{max,Mi,f}$ | 2.658E-3                             | mM/ms | maximum velocity in the forward direction (PCr production)                                     |
| $V_{max,Mi,b}$ | calculated                           | mM/ms | maximum velocity in the backward direction (ATP production); Vb/Vf = 4.199                     |
| $K_{ia, Mi}$   | 7.1532E-1                            | mM    | binary dissociation constant ATP                                                               |
| $K_{ib, Mi}$   | 2.8733E1                             | mM    | binary dissociation constant Cr                                                                |
| $K_{ic, Mi}$   | 2.017E-1                             | mM    | binary dissociation constant ADP                                                               |
| $K_{id, Mi}$   | 1.5977                               | mM    | binary dissociation constant PCr                                                               |
| $K_{b, Mi}$    | 5.209                                | mM    | ternary dissociation constant Cr                                                               |
| $K_{d, Mi}$    | 4.99E-1                              | mM    | ternary dissociation constant PCr                                                              |
| $K_{c, Mi}$    | $K_{ic, Mi}$$K_{d, Mi}$/$K_{id, Mi}$ | mM    | ternary dissociation constant ADP                                                              |
| $K_{Ib, Mi}$   | $K_{ib, Mi}$                         | mM    | ternary dissociation constant Cr from dead end complex                                         |
| $C_{CK, Mi}$   |                                      |       | mitochondrial creatine kinase activity                                                         |
|                |                                      |       |                                                                                                |
| MMCK           |                                      |       | cytosol creatine kinase enzyme  (MiCK activity is about 15% of the total CK activity in heart) |
| $V_{max,MM,f}$ | 6.996E-3                             | mM/ms | maximum velocity in the forward direction (PCr production)                                     |
| $V_{max,MM,b}$ | calculated                           | mM/ms | maximum velocity in the backward direction (ATP production)                                    |
| $K_{ia, MM}$   | 9E-1                                 | mM    | binary dissociation constant ATP                                                               |
| $K_{ib, MM}$   | 1.55E1                               | mM    | binary dissociation constant Cr                                                                |
| $K_{ic, MM}$   | 2.224E-1                             | mM    | binary dissociation constant ADP                                                               |
| $K_{id, MM}$   | 1.670                                | mM    | binary dissociation constant PCr                                                               |
| $K_{b, MM}$    | 3.49E1                               | mM    | ternary dissociation constant Cr                                                               |
| $K_{d, MM}$    | 4.73                                 | mM    | ternary dissociation constant PCr                                                              |
| $K_{c, MM}$    | $K_{ic, Mi}$$K_{d, Mi}$/$K_{id, Mi}$ | mM    | ternary dissociation constant ADP                                                              |
| $K_{Ib, MM}$   | $K_{ib, Mi}$                         | mM    | ternary dissociation constant Cr from dead end complex                                         |
| $C_{CK, MM}$   |                                      |       | cytosol creatine kinase activity                                                               |
|                |                                      |       |                                                                                                |
| Permeability   |                                      |       |                                                                                                |
| $R_{ATP}$      | 8.16                                 | Hz    | diffusional conductance ATP                                                                    |
| $R_{ADP}$      | 65.2227                              | Hz    | diffusional conductance ADP                                                                    |
| $R_{PCr}$      | 24615                                | Hz    | diffusional conductance PCr                                                                    |
| $R_{Cr}$       | 1166.7                               | Hz    | diffusional conductance Cr                                                                     |
| $R_{Pi}$       | 6.0318                               | Hz    | diffusional conductance Pi                                                                     |
| $V_{cyto}$     | 3                                    |       | Fractional volume of cytosol. Total volume 1 corresponds to $V_{mito}$=0.153mL/gww.            |
| $V_{ims}$      | 1/4                                  |       | Fractional volume of intermembrane space.                                                      |

[^vanBeek2007]: Kongas O, van Beek JHGM Creatine kinase in energy metabolic signaling in muscle Nature Precedings (2007)DOI: https://doi.org/10.1038/npre.2007.1317.1