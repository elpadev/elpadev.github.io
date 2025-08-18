---
layout: post
title: Light and matter - A description based on a quantum mechanical two-level system and a classical electric field
description:
summary:
tags: [physics]
---

In the following we will describe the effect of light on matter based on a very simple two-level quantum mechanical system. In another post I will describe light classically.

Suppose we have a simple two-level quantum mechanical system with energies $$E_1$$ and $$E_2$$ and the states $$\psi_0$$ and $$\psi_1$$. Without any external influence, these two states are completely  uncoupled as there is no reason for a particle to jump from one state to the other (we assume the ground state as the initial state). This means that $$\psi_0$$ and $$\psi_1$$ are time-independent and are solutions to the time-independent Schrödinger equation:

$$
\begin{equation}
  \hat{H_0} \psi_j = E_j \psi_j
\end{equation}
$$

Now what happens when light hits matter? The two states are now coupled! Why? Because now an electron in the ground state $$\psi_0$$ can absorb energy from light (a photon) and jump to the higher energy state $$\psi_1$$!

To make the calculations a bit simpler, we want to treat light classically. In classical electrodynamics, light is basically an alternating electric field $$\vec{E}$$ and $$\vec{B}$$ field. For now we ignore the magnetic field $$\vec{B}$$.

The question of the interaction of light and matter becomes: How does an alternating external electric field $$\vec{E}$$ does change our two-level quantum mechanical system?

First, the external electric field $$\vec{E}$$ leads to a coupled two-level system because now a transition between the two states is possible. There is a general Ansatz for coupled quantum mechanical system: Describe the overall system as a linear combination of the uncoupled states.

$$
\begin{equation}
  \psi = c_1 \psi_0 + c_2 \psi_1
\end{equation}
$$

As we are dealing with an alternating electric field $$\vec{E}(t)$$, $$c_1$$ and $$c_2$$ must be time-independent. Because it can be that at a time the state $$\psi_0$$ is more "favourable" and at another time the state $$\psi_1$$.


An external electric field $$\vec{E}$$ can also lead to an induced dipole moment. Without the external field normally the dipole moment vanishes in time average because of the symmetry (imagine the probability cloud for the position of an electron around the core in $$1s$$ state in the hydrogen atom). This means that the overall energy of the system is now the sum of the energy of the unperturbed system and the dipole moment:

$$
\begin{equation}
  \hat{H} = \hat{H_0} + \hat{H}_{dipole} = \hat{H_0} - e\hat{\vec{E}} \hat{x}
\end{equation}
$$

Now has does the overall Schrödinger equation looks like? $$\psi$$ must now be time-dependent, as the field changes the position probability clouds of the electron from time to time. So we need to solve the time-dependent Schrödinger equation:

$$
\begin{equation}
  i\hbar \frac{\partial \psi}{\partial t} = (\hat{H_0} + \hat{H}_{dipole}) \psi
\end{equation}
$$

Now what do we get for $$\psi$$ after solving the Schrödinger equation? $$\psi_0$$ and $$\psi_1$$ are assumed to be known (solutions of the hydrogen atom). For $$c_1$$ and $$c_2$$ we get:

$$
\begin{equation}
  c_1 = \exp{\frac{-iE_1t}{\hbar}} \cos{\omega_{rabi} t}
\end{equation}
$$
$$
\begin{equation}
  c_2 = \exp{\frac{-iE_2t}{\hbar}} \sin{\omega_{rabi} t}
\end{equation}
$$
$$
\begin{equation}
  |c_1|^2 = \cos^2{(\omega_{rabi} t)}
\end{equation}
$$
$$
\begin{equation}
  |c_2|^2 = \sin^2{(\omega_{rabi} t)}^2
\end{equation}
$$


What does this means? As $$\psi_0$$ and $$\psi_1$$ are time-independent, the time-dependence of the overall wave function $$\psi$$ is determined by $$c_1$$ and $$c_2$$.

What this means it that the electron jumps between $$\psi_0$$ and $$\psi_1$$ with a frequency of $$2\omega_{rabi}$$ ($$1\omega_{rabi}$$ is the frequency to see the electron in the same state again). This jumping back and forth of the electron is called the <em>Rabi oscillation</em>.

The the value of $$\omega_{Rabi}$$ is:

$$
\begin{equation}
  \omega_{Rabi} = \frac{\vec{E}_0 \cdot \vec{\mu}_{01}}{\hbar}
\end{equation}
$$

$$\vec{E}_0 \cdot \vec{\mu}_{01}$$ is the energy gain that we get when the external electric field induces a dipole moment (please note that $$\omega_{Rabi}$$ depends on the time-independent $$\vec{E}_0$$, so $$\omega_{Rabi}$$ is constant and only depends on the magnitude and direction of the external electric field and not its frequency. This makes $$\omega_{Rabi}$$ somehow characteristic to the material).


Rabi oscillation
----------------

What happens when an electron jumps back and forth between two states? When it jumps to a higher energy state it absorbs energy (a photon). When is jumps back to the lower energy state it gives back the energy, it emits a photon. How many photons are emitted after the time $$t$$? Because the electron is in the ground state with a freqeuncy of $$\omega_{rabi}$$, it emits $$\omega_{rabi} \times 2\pi \times t$$ photons. What energy do the photons have?

$$
\hbar \omega_{photon} = E_2 - E_1
$$

Physicists have a name for the phenomenon that an electron emits a photon after being excited to a higher state: <em>stimulated emission</em> as it does not occur by itself and is induced by an external force.

Damping
-------

In real world we often cannot observe full Rabi oscillation, meaning we don't see emission of the photons by $$\omega_{rabi}$$. This is because electrons often lose their energy as heat before reaching a higher state. The probability of finding an electron in a higher states is given by:

$$
\begin{equation}
  |c_2|^2 \approx (\frac{\omega_{Rabi}}{2\gamma})^2
\end{equation}
$$

$$\gamma$$ is the damping constant. This means that if we want to have more electrons in higher states, we need higher $$\omega_{Rabi}$$. This can be achieved by stronger external fields.
