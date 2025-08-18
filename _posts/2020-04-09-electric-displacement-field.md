---
layout: post
title: The electric flux density (displacement field)
description:
summary:
tags: [physics, classical_electrodynamics]
---

There are some things that have caused a lot of confusion for me when I did electrodynamics, a lot of them spawn when matter comes into play. One of those things is the <em>electric displacement</em>.

In electrodynamics, <em>electric field strength</em>, <em>electric flux</em>, <em>electric flux density</em>, <em>magnetic field strength</em>, <em>magnetic flux</em>, and <em>magnetic flux density</em> are different things.

Consider a **fixed** positive charge somewhere in vacuum. It exerts a force on whatever charge we put into space. How do we know? We know this because we can measure an acceleration of the newly introduced charge. To be able to describe this force independent of how much charge we add to the space, we normalise this force and call it <em>electric field strength</em> $$\vec{E}$$:

$$
\begin{equation}
\vec{E} = \frac{\vec{F}}{e}
\end{equation}
$$

The direction of force $$\vec{F}$$ and thus of electric field strength $$\vec{E}$$ is defined from the postive charge to the negative charge.

Now what happens when we put matter somewhere into our space? It depends whether you have a conductor or a non-conductor. Conductors have free charges, non-conductors have fixed charges.

When we put a conductor in a space with an electric field, the electric exerts forces on the freely movable charge in the conductor and they arrange such that they create an electric field of their own (internal electric field) which has the exactly opposite direction of the external electric field and exactly the same electric field strength. The sum of the external and internal electric field is zero, so there is no electric field inside the conductor.

What happens when we have a non-conductor? Here we have fixed charges. The external electric field causes the charges shift a little bit: electrical dipoles are induced! They are arranged such the they weaken the electrical field. Electrical dipoles are described mathematically by the electric dipole moment:

$$
\begin{equation}
  \vec{p} = e\vec{x}
\end{equation}
$$

$$e$$ is how much positive charge the dipole has. The magnitude of $$\vec{x}$$ is the distance between the positive and negative charge. **The orientation of the dipole is defined from negative to positive (opposed to the electric field!)**. Now comes the confusion causer: **The electric field and the induced electric moments have the same orientation! (this is important to know)**.

Now we define a macroscopic expression for the induced electric dipole moment: How much induced dipole moments per volume $$V$$ do I have? (density of electric moments). This is called <em>polarisation</em> $$\vec{P}$$:

$$
\begin{equation}
  \vec{P} = \frac{\sum{p_i}}{V}
\end{equation}
$$


Now back to the physics: As we see because of the movement of charges in conductors and shift of charges in non-conductors the electrical field strength outside of the material is always different from inside of the material:  $$\vec{E}_{internal} \neq \vec{E}_{external}$$. In conductors: $$\vec{E}_{internal} = 0$$, in non-conductors: $$\vec{E}_{internal} < \vec{E}_{external}$$. Is there any quantity whose value is independent of the material? Yes, the electric flux density $$\vec{D}$$!:

$$
\begin{equation}
  \vec{D} = \epsilon_0 \vec{E} + \vec{P}
\end{equation}
$$

**Confusion causer: with $$\vec{E}$$ we now mean $$\vec{E}_{internal}$$!**. Also note that $$\vec{E}$$ and $$\vec{P}$$ have the same orientation! So somehow $$\vec{D} \propto E_{external}$$ and $$E_{external}$$ is of course independent of the material.

**Confusion causer: $$\epsilon_0 \vec{E}$$:** Please note that the electric displacement field is **just a definition**. Don't try to overinterpret it $$\epsilon_0 \vec{E}$$. The internal electric field $$\vec{E}_{internal}$$ and the polarisation $$\vec{P}$$ are somehow added up together and result in a quantity which is independent of the material.

What is the intuition behind the electric displacement field $$\vec{D}$$? $$\vec{D}$$ is also called the <em>electric flux density</em> with a unit of $$\frac{C}{m^2}$$. It is a measure of how many electric field lines per area we have: fields lines of $$\vec{E}$$ and field lines of $$\vec{P}$$. I think this is why we define the orientation of the dipoles from negative to positive: to be able to imagine $$\vec{D}$$ better (there is probably a more mathematical reason behind it, but I think like this unless something bad happens).

Now want to have a look at the relationship between the internal electric field with the strength $$\vec{E}$$ and polarisation $$\vec{P}$$. It should be like this: when the material is more polarised, the original external field in the material is more weakened so the internal field strength $$\vec{E}$$ decreases and vice versa. We can measure a proportionality constant between $$\vec{E}$$ and $$\vec{P}$$ (for linear materials):

$$
\begin{equation}
  \frac{\vec{P}}{\vec{E}} = \epsilon_0 \chi = \epsilon_0 (\epsilon_r - 1)
\end{equation}
$$

$$\epsilon_r$$ is the relative permeability (dimensionless) and somehow describes how "easily" one material gets polarised. Higher $$\epsilon_r$$ means that the "portion" of the polarisation in the material is higher compared to the internal electrical field. $$\chi$$ is called the electric susceptibility and like $$\epsilon$$ (they are more or less the same) how "easily" a material gets polarised.



Using this equation we get a more simplified expression for the electric flux density (electric displacement field):

$$
\begin{equation}
  \vec{D} = \epsilon_0 \vec{E} + \vec{P} =  \epsilon_0 \vec{E} + \epsilon_0 (\epsilon_r - 1) \vec{E} = \epsilon_0 \epsilon_r \vec{E}
\end{equation}
$$

Generally in real dielectric materials the polarisation does depend on orientation of the applied electric field because they are not completely symmetric. For example an electric field applied in $$\vec{x}$$ direction may cause a higher density of dipoles (polarisation) than an electric field in $$\vec{y}$$ direction. Also an electric field applied in one direction may cause in a polarisation with a different orientation. That's why the electric susceptibility is generally a matrix: $$\chi_{ij}$$:

$$
\begin{equation}
  P_i = \epsilon_0 \sum_{j}{\chi_{ij} E_j}
\end{equation}
$$

How can we intuitively understand $$\chi_{ij}$$? The first index $$i$$ has always something to do with the result ($$\vec{P}$$). The second index $$j$$ has always something to do with the input ($$\vec{E}$$). $$\chi_{21}$$ for example describes the "influence" of the first component of the electric field ($$E_x$$) on the second component of the polarisation ($$P_y$$). So for example if $$\chi_{21}$$ is non-zero and every other component of the matrix is zero we only get a polarisation if we apply an electric field in $$\vec{x}$$ direction and the resulted polarisation is in $$\vec{y}$$ direction (strange behaviour though).







![capacitor](/assets/images/capacitor.svg){:height="50%" width="50%"}
