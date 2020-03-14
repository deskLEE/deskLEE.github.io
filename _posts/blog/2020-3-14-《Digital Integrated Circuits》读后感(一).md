---
layout: post
title: 《Digital Integrated Circuits》读后感(一)
categories: Blog
description: The device Chapter 3
keywords: 2020, 寒假
---

Chapter 3  The device__

_1) The Diode_

a. 	built-in potential	forward bias	reverse bias	

b. 	==thermal generation of hole== and electron pairs in the depletion region  reverse currents are substantially larger than the saturation current $I_s$

c. 	Dynamic Behavior	Depletion-Region Capacitance $C_j$

$$C_j = \frac {C_{j0}} {\sqrt{ 1-V_D/\phi_0}}$$		$V_D<0$ , $|V_D|$ increases, $C_j$ decreases

d. 	Secondary Effects	breakdown voltage	avalanche breakdown not destructive

Zener breakdown	

$$\begin{cases} I_d = I_s(e^{V_D/\phi_T}-1) \\ \phi_T = \frac {KT}{q}\end{cases}$$ operating temperature	$\phi_T$ increases with $T$, $I_d$ decreases at the same time.  $I_s$ increases with $T$ 

Increasing the temperature causes the leakage current to increase.

_2) The MOSFET Transistor_

a. 	four terminal device	gate	source	drain	body	NMOS	PMOS

strong inversion	threshold voltage $V_T$

$$\begin{cases}V_T = V_{T0}+\gamma(\sqrt{|-2\phi_F+V_{SB}|}-\sqrt{|-2\phi_F|}) \\ \phi_F = -\phi_TIn(\frac{N_A}{n_i})\end{cases}$$ $\gamma$ body-effect coefficient 

b. 	$V_{GS}>V_T$ 

$x$ along the channel, the voltage is $V(x)$. gate-to-channel voltage at the point equals $V_{GS}-V(x)$. 

$$Q_i(x) = -C_{ox}[V_{GS}-V(x)-V_T]$$   $C_{ox} = \frac {\epsilon_{ox}} {t_{ox}}$ 

$$\begin{cases}I_D = {k_n}^{’}\frac{W}{L}[(V_{GS}-V_T)V_{DS}-\frac{{V_{DS}}^{2}}{2}] \\ {k_n}^{'} = \mu_nC_{ox}   \end{cases}$$ ==linear region==

c. 	$V_{GS}-V_x<V_T$ pinched off 

$$ I_D = \frac{{k_n}^{’}}{2}\frac{W}{L}[{(V_{GS}-V_T)}^{2}] $$ 

d. 	channel-length modulation 

increasing $V_{DS}$ causes the depletion region at the ==drain junction== to grow, reducing the length of effective channel.

$$I_D = {I_D}^{’}(1+\lambda V_{DS})$$ $\lambda$ channel-length modulation

long-channel transistors

e.	 velocity saturation

short-channel devices	velocity saturation effect	saturation velocity $\upsilon_{sat}$  electrical  field$\epsilon_c$

$$\upsilon_n = -\mu_n \epsilon(x)$$  velocity-saturation effects are hence less pronounced in PMOS transistors

==the delivered current is smaller than what would be normally expected==

$$I_{DSAT} = \upsilon_{sat}C_{ox}W(V_{GT}-V_{DSAT})$$ 

effect:

- $V_{DSAT}<V_{GT}$

- $I_{DSAT}$ displays a linear dependence with respect with $V_{GS}$.

f.  	$I_D-V_{DS}$ curve	subthreshold conduction 

slope factor $S$ 

_3) Dynamic Behavior_

a. 	MOS Structure Capacitances

gate capacitances $C_{g}$	lateral diffusion $x_d$ 	overlap capacitances 

$$C_{GSO}=C_{GDO}=C_{ox}x_{d}W=C_{0}W$$

b. 	channel capacitances

gate-to-channel $C_{GS}$ into three components $C_{GCS}$、$C_{GCD}$、$C_{GCB}$

$C_{GCS}=C_{GCD}=WLC_{ox}/2$

$C_{GCB} = WLC_{ox}$

c. 	junction capacitances

reverse bias  diffusion capacitance

bottom-plate junction	side-wall junction	$C_{diff} = C_{bottom}+C_{sw} = C_{j}L_SW+C_{jsw}(2L_S+W)$

d. 	source-drain resistance

$$R_{S,D}=\frac {L_{S,D}}{W}R_x+R_c$$ 	use material such as titanium or tungsten

process named silicidation

e. 	some secondary effects

- $V_T$ becomes a function of $L$,$W$,$V_{DS}$ 	short-channel	$V_{T0}$ decreases with $L$ for short-channel devices	drain-induced barrier lowering(DIBL)

  punch-through

- hot-carrier effect   ==electrons trapped in the oxide change the threesholds of NMOS devices, while decreasing the $V_T$ of PMOS transistors

f. 	Process Variations

$I_D$ connects with $V_T$,${k_n}^{’}$,$W$,$L$

considering worst-case values

_4) Technology scaling_

a. 	factor $S$ ,$U$

- full scaling: voltages and dimensions are scaled by the same factor $S$

the speed of the circuit increases in a linear fashion, while the power scales down quadratically.

- fixed-voltage scaling

comes with a major power penalty

- general scaling

dimensions and voltages are scaled independently

b. 	Berkeley FinFET dual-gated transistor

c. 	vertical transistor three-dimensional artifact


