

### **Ordinary Differential Equations**


$$
\begin{equation}
\frac{d\left[ Ca^{2+}\right]_{mito}}{dt} =\delta _{Ca}( V_{uni} -V_{NaCa})
\end{equation}
$$

$$
\begin{equation}
\frac{d[ADP]_{mito}}{dt} =V_{ANT} -V_{ATPase} -V_{SL}
\end{equation}
$$

$$
\begin{equation}
\frac{d\Delta \Psi _{m}}{dt} =\frac{V_{He} +V_{He(SDH)} -V_{Hu} -V_{ANT} -V_{Hleak} -V_{NaCa} -V_{uni} -V_{IMAC}}{C_{mito}}
\end{equation}
$$

$$
\begin{equation}
\frac{d[NADH]_{mito}}{dt} =V_{O_{2}} +V_{IDH} +V_{KGDH} +V_{MDH} -V_{THD}
\end{equation}
$$

$$
\begin{equation}
\frac{d\left[ H^{+}\right]_{mito}}{dt} =\delta _{M}( -V_{He} -V_{He(SDH)} +V_{Hu} +V_{NaH} +V_{PiC} +V_{Hleck})
\end{equation}
$$

$$
\begin{equation}
\frac{d[Pi]_{mito}}{dt} =-V_{ATPase} +V_{PiC} -V_{SL}
\end{equation}
$$

$$
\begin{equation}
\frac{d[ISOC]}{dt} =V_{ACO} -V_{IDH} -V_{IDH_{-} NADP}
\end{equation}
$$

$$
\begin{equation}
\frac{d[\alpha KG]}{dt} =V_{IDH} +V_{IDH_{-} NADP} -V_{KGDH} +V_{ATT}
\end{equation}
$$

$$
\begin{equation}
\frac{d[SCoA]}{dt} =V_{KGDH} -V_{SL}
\end{equation}
$$

$$
\begin{equation}
\frac{d[Suc]}{dt} =V_{SL} -V_{O_{2} SDH}
\end{equation}
$$

$$
\begin{equation}
\frac{d[FUM]}{dt} =V_{o_{2} SHH} -V_{FH}
\end{equation}
$$

$$
\begin{equation}
\frac{d[MAL]}{dt} =V_{FH} -V_{MDH}
\end{equation}
$$

$$
\begin{equation}
\frac{d[OAA]}{dt} =V_{MDH} -V_{CS} -V_{AAT}
\end{equation}
$$

$$
\begin{equation}
\frac{d[NADPH]_{m}}{dt} =V_{IDH_{-} NADP} +V_{THD} -V_{GRm} -V_{TxRm}
\end{equation}
$$

$$
\begin{equation}
\frac{d\left[ O_{2}^{\bullet -}\right]_{mito}}{dt} =\operatorname{shunt}( V_{O_{2}} +V_{O_{2} SDH}) -V_{MnSOD} -V^{Tr}_{ROS}
\end{equation}
$$

$$
\begin{equation}
\frac{d\left[ O_{2}^{\bullet -}\right]_{cyto}}{dt} =\frac{v_{m}}{v_{i}} V^{Tr}_{ROS} -V_{CuZnSOD}
\end{equation}
$$

$$
\begin{equation}
\frac{d[ H_{2} O_{2}]_{mito}}{dt} =V_{MnSOD} -V_{difH_{2} O_{2}} -V_{GPXm} -V_{TxPXm}
\end{equation}
$$

$$
\begin{equation}
\frac{d[ H_{2} O_{2}]_{cyto}}{dt} =V_{CuZnSOD} +\frac{v_{m}}{v_{i}} V_{difH_{2} O_{2}} -V_{GPXi} -V_{TxPXi} -V_{CAT}
\end{equation}
$$

$$
\frac{d[GSH]_{mito}}{dt} =V_{GRm} -V_{GPXm} -V_{GRXm} +V_{GST} -V_{PSSGm}
$$

$$
\frac{d[GSH]_{cyto}}{dt} =V_{GRi} -V_{GPXi} -V_{GRXi} +\frac{v_{m}}{v_{i}} V_{GST} -V_{PSSGi}
$$

$$
\frac{d[GSSG]_{mito}}{dt} =0.5( V_{GPXm} -V_{GRm}) +V_{GRXm}
$$

$$
\frac{d[ Trx( SH)_{2}] }{dt}\ =\ V_{TrxR} \ -\ V_{TxPx}   \\  (\frac{d[TxR]_{mito}}{dt} =V_{TxRm} -V_{T_{x} PXm})
$$

$$
\frac{d[ Prx( SH)_{2}] }{dt}\ =\ V_{TxPx} \ -\ V_{Prx} \\
(\frac{d[TxR]_{cyto}}{dt} =V_{T\times Ri} -V_{TxPXi})
$$

$$
\frac{d[PSSG]_{mito}}{dt} =V_{PSSGm} -V_{GRXm}
$$

$$
\frac{d[PSSG]_{cyto}}{dt} =V_{PSSGi} -V_{GRXi}
$$

$$
\begin{align}
\frac{d[Q]_n}{dt} &= v_5 - v_{7,ox}- v_{7,rd} - v_1  \\
\frac{d[Q^{ \cdot -}]_n}{dt} &= v_{7,ox} + v_{7,rd} - v_{8,ox}- v_{8,rd}  \\
\frac{d[QH_2]_n}{dt} &= v_{8,ox} + v_{8,rd} + v_1 - v_2   \\
\frac{d[QH_2]_p}{dt} &= v_2 -v_3 \\
\frac{d[Q^{ \cdot -}]_p}{dt} &= v_3 - v_{10} - v_{10b} - v_{4,ox} - v_{4,rd}   \\
\frac{d[Q]_p}{dt} &= v_{10} + v_{10b} + v_{4,ox} + v_{4,rd} - v_5   \\
\frac{d[b1]}{dt} &= v_{7,ox} + v_{8,ox} - v_{4,ox}    \\
\frac{d[b2]}{dt} &= v_{4,ox} + v_{7,rd} - v_{8,rd} - v_6   \\
\frac{d[b3]}{dt} &= v_6 - v_{4,rd} + v_{7,ox} - v_{8,ox}    \\
\frac{d[b4]}{dt} &= v_{4,rd} - v_{7,rd} - v_{8,rd}   \\
\frac{d[FeS]_{ox}}{dt} &= v_9 - v_3      \\
\frac{d[cytc1]_{ox}}{dt} &= v_{33} - v_9   \\
\frac{d[cytc]_{ox}}{dt} &= V_e - v_{33}   \\\end{align}
			
$$

$$
\frac{d[ADP]_{ims}}{dt}=(-J_{syn} -J_{CK,Mi} -j_{diff,ATP} )/V_{ims}
$$

$$
\frac{d[ATP]_{ims}}{dt} =(J_{syn} -J_{CK,Mi} -j_{diff,ATP} )/V_{ims}
$$

$$
\frac{d[Cr]_{ims}}{dt}=(-J_{CK,Mi} -j_{diff,Cr} )/V_{ims}
        \\
$$

$$
\frac{d[PCr]_{ims}}{dt}=(J_{CK,Mi} -j_{diff,PCr} )/V_{ims}
$$

$$
\frac{d[PCr]_{cyt}}{dt}
=(J_{CK,MM} +J_{diff,PCr} )/V_{cyt}
$$

$$
\frac{d[ADP]_{cyt}}{dt}
=(J_{hyd} +J_{CK,MM} +J_{diff,ADP} )/V_{cyt}    \\
$$

$$
\frac{d[ATP]_{cyt}}{dt}
=(-J_{hyd} -J_{CK,MM} +J_{diff,ATP} )/V_{cyt}    \\
$$

$$
\frac{d[Cr]_{cyt}}{dt}
=(-J_{CK,MM} +J_{diff,Cr} )/V_{cyt} \\
$$

$$
\frac{d[Pi]_{ims}}{dt}=(-J_{syn} -j_{diff,Pi} )/V_{ims}
$$

$$
\frac{d[Pi]_{cyt}}{dt}=(J_{hyd} +J_{diff,Pi} )/V_{cyt}
$$

$$
\frac{d[ATP]_{mito}}{dt} =-V_{ANT}+V_{ATPase} +V_{SL}
$$

