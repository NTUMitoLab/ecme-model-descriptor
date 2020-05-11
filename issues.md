# Some issues in the model

## IMAC

The Nernst notation[^Cortassa2004] for ROS efflux may fall out of the linear range of IMAC when there is a huge difference of the concentrations of ROS between the matrix  and extra-matrix compartments. This may cause  numerical stability issues.
$$
\begin{align}
V_{tr}^{ROS} &= j \cdot g_{IMAC} \left( \Delta\Psi_m + V_T ln \left( \frac{\ce{[O2-]_m}}{\ce{[O2-]_i}} \right) \right) \\
\end{align}
$$

An alternative is to adopt Nivalas’ IMAC model[^Nivala2011] with GHK flux equation, which is singularity-free and more general.
$$
J_{IMAC} = g_{IMAC}\frac{\delta}{e^\delta -1} (e^\delta \ce{[O2-]}_m - \ce{[O2-]}_i) \\
\delta = \Delta\Psi_m / V_T
$$



# ANT

The rate equation Adenine nucleotide translocator (ANT) is reverted to that of Magnus and Keizer’s model, to respect the effect of mitochodrial membrane potential on the electrogenic transfer of free ADP and free ATP.

## Complex I

The unit of redox potentials of FMN and superoxide is V instead of mV. The fix would cause the change of equilibrium constant from ~1 to 5600, favoring superoxide formation, blocking the reverse reaction of ROS generations in complex I.

## Complex V

### Equilibrium constant

$$
\ce{ATP + H2O <=> ADP + Pi + H+} \\
K_{eq} = \frac{\ce{[Pi]}\ce{[ADP]}}{\ce{[ATP]}}
$$



The equilibrium constant for ATP hydrolysis  ($1.71 \times 10^6$ mM)  was originated from Magnus and Keiser model[^Magnus1997], which was from the Pietrobon and Caplan 6-state proton pump model[^Pietrobon1985], but it was 1000 times off ($1.71 \times 10^6$ M = $1.71 \times 10^9$ mM, @ pH = 7.4).

The reference free energy change for ATP hydrolysis with magnesium is around -29.1kJ/mol @ pH=7, T = 310K.[^Guynn1973][^Heiske2017] It corresponds to an equilibrium constant of 80074 M
$$
\ce{MgATP^2- + H2O <=> MgADP- + HPO4^2- + H+}
$$

In physiological conditions, the free energy change for the apparent equilibrium constant is -36.03kJ/mol @  pH=0, T = 310K[^Beard2005], -31.80kJ/mol @ pH=7, Mg = 1mM, T = 310K[^Guynn1973]

A table with apparent Keq's with various pH and pMg could be found in Golding's work.[^Golding1995]


### Math expression

The math expression of ATP synthassein Laura's model[^Gauthier2013A]



# Q cycle

The Q-cycle in Laura's model[^Gauthier2013A], adapted from Demin’s model[^Demin2001], allows large quantities of free semiquinones (~75%) under inhibition of the ETC, which is only relevant in very artificial conditions.  An alternativewould be make the SQ bounded to compelx III and thus limit its concentration.

# Transhydrogenase

Transhydrogenase (THD) is based on rapid equilibrium random Bi-Bi mechanism with 2 dead-end metabolites[^Kembro2013]. Bias from pmf is applied to the affinities of oxidized substrates. Thus the denominator should be 1 + A + B + P + Q + AB’ + P’Q + AQ + B’P’.



[^Pietrobon1985]: Pietrobon, D., & Caplan, S. R. (1985). Flow-force relationships for a six-state proton pump model: intrinsic uncoupling, kinetic equivalence of input and output forces, and domain of approximate linearity. *Biochemistry*, *24*(21), 5764–5776.

[^Magnus1997]: Magnus, G., & Keizer, J. (1997). Minimal model of beta-cell mitochondrial Ca2+ handling. *The American Journal of Physiology*, *273*(2 Pt 1), C717-33.

[^Guynn1973]: Guynn, R. W., & Veech, R. L. (1973). The equilibrium constants of the adenosine triphosphate hydrolysis and the adenosine triphosphate-citrate lyase reactions. The Journal of Biological Chemistry, 248(20), 6966–6972.

[^Heiske2017]: Heiske, M., Letellier, T., & Klipp, E. (2017). Comprehensive mathematical model of oxidative phosphorylation valid for physiological and pathological conditions. The FEBS Journal, 284(17), 2802–2828.

[^Beard2005]: Beard, D. A. (2005). A biophysical model of the mitochondrial respiratory system and oxidative phosphorylation. PLoS Computational Biology, 1(4), e36.

[^Golding1995]: Golding, E. M., Teague, W. E., & Dobson, G. P. (1995). Adjustment of K’ to varying pH and pMg for the creatine kinase, adenylate kinase and ATP hydrolysis equilibria permitting quantitative bioenergetic assessment. The Journal of Experimental Biology, 198(Pt 8), 1775–1782.

[^Demin2001]: Demin, O. V., Gorianin, I. I., Kholodenko, B. N., & Westerhoff, H. V. (2001). [Kinetic modeling of energy metabolism and generation of active forms of oxygen in hepatocyte mitochondria]. Molekuliarnaia Biologiia, 35(6), 1095–1104.

[^Gauthier2013A]: Gauthier, L. D., Greenstein, J. L., Cortassa, S., O’Rourke, B., & Winslow, R. L. (2013). A computational model of reactive oxygen species and redox balance in cardiac mitochondria. Biophysical Journal, 105(4), 1045–1056.

[^Kembro2013]: Kembro, J. M., Aon, M. A., Winslow, R. L., O’Rourke, B., & Cortassa, S. (2013). Integrating mitochondrial energetics, redox and ROS metabolic networks: a two-compartment model. Biophysical Journal, 104(2), 332–343.

[^Cortassa2004]: Cortassa, S., Aon, M. A., Winslow, R. L., & O’Rourke, B. (2004). A mitochondrial oscillator dependent on reactive oxygen species. Biophysical Journal, 87(3), 2060–2073.

[^Nivala2011]: Nivala, M., Korge, P., Nivala, M., Weiss, J. N., & Qu, Z. (2011). Linking flickering to waves and whole-cell oscillations in a mitochondrial network model. Biophysical Journal, 101(9), 2102–2111.