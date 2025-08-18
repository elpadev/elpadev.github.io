---
layout: post
title: Light and atoms - A classical description, Lorentz Oscillator
description:
summary:
tags: [physics, condensed_matter_physics]
---

How is the interaction of light and atoms described in classical physics? First we start defining light and matter in terms of classical physics.

In classical electrodynamics, light is a wave. It is a wave of alternating electric and magnetic fields that are perpendicular to the direction of propagation and to each other. The electric and magnetic fields of light must be solutions to the electromagnetic wave equation:


$$
\begin{equation}
  \nabla^2 \vec{E} = \frac{1}{c^2} \frac{\partial^2 \vec{E}}{\partial t^2}
\end{equation}
$$

$$
\begin{equation}
  \nabla^2 \vec{B} = \frac{1}{c^2} \frac{\partial^2 \vec{B}}{\partial t^2}
\end{equation}
$$

$$c$$ is the propagation speed. Every solution to the wave equation can be thought as a linear combination of many simple sinus waves with the same propagation speed $$c$$. So the must simple description of light is a sinus magnetic and a sinus electric field, for example:

$$
\begin{equation}
  \vec{E}(\vec{r}, t) = \vec{E}_0 \cos{(\vec{k} \cdot \vec{r} - \omega t)}
\end{equation}
$$

$$
\begin{equation}
  \vec{B}(\vec{r}, t) = \vec{B}_0 \cos{(\vec{k} \cdot \vec{r} - \omega t)}
\end{equation}
$$

$$\vec{k}$$ is the wave vector. It points to the direction of propagation and $$ \\|\overrightarrow{k}\\| = \dfrac{2\pi }{\lambda }$$. And there is actually a simple and nice relationship between the electric and magnetic field:

$$
\begin{equation}
  \overrightarrow {B}=\dfrac {1}{\omega}\left( \overrightarrow {k}\times \overrightarrow {E}\right)
\end{equation}
$$

What is the relationship between $$c$$, $$\vec{k}$$ and $$\omega$$? Imagine a point fixed to a wave. How fast does it move? We now that after the time period $$T$$ it covers a distance of the wavelength $$\lambda$$, so its effective speed is:

$$
\begin{equation}
  c=\dfrac {\lambda }{T}=\lambda \dfrac {1}{T}=\dfrac {2\pi }{\left| \overrightarrow {k}\right| }\dfrac {\omega }{2\pi }=\dfrac {\omega}{\left| \overrightarrow {k}\right| }
\end{equation}
$$

(Here, if we imagine a point fixed to the wave, $$c$$ is the <em>effective speed</em> of the point. This speed is called the <em>phase velocity</em>. As the point goes up and down, and not in straight line, its actual speed must be higher)

Now, how can we describe an atom classically? Simple, as a positive and a negative charge connected by a spring!

So classically, the interaction of light and matter becomes the interaction of a spring bounded dipole with an alternating electric field! The equation of motion of this system is simply that of the driven and damped harmonic oscillator, the Lorentz oscillator:

$$
\begin{equation}
m_{e}\dfrac {\partial ^{2}}{\partial t^{2}}x \left( t\right) +m_{e  } \gamma \dfrac {\partial}{\partial t}x \left( t\right) +m_{e}{\omega}^{2}_{0}x\left( t\right) =-e\overrightarrow {E}_{0}e^{i\left( \overrightarrow {k}\overrightarrow {x}-\omega t\right) }
\end{equation}
$$

$$\gamma$$ is the damping constant. This considers possible energy losses in the atom. For the eigenfrequency $$\omega_0$$ we have: $$\omega_0 = \frac{\kappa}{m}$$ ($$\kappa$$ is the sprint constant). This is the frequency of the oscillation of the simple harmonic oscillator: if we don't have damping and external drive forces. So $$\omega_0 $$ is somehow "intrinsic" to the oscillator.

The solution of the Lorentz oscillator for the distance between the electron the and core is given by:

$$
\begin{equation}
  x \left( t\right) =\overrightarrow {x}_{0}\left( t\right) e^{i( \overrightarrow {k}\overrightarrow {r}-\omega t + \phi)}
\end{equation}
$$

$$
\begin{equation}
{\vec{x}}_0 = \frac{-e\vec{E}_0}{m_e}\frac{1}{\sqrt{(\omega^2 - \omega_0^2)^2+ (\gamma \omega^2)}}
\end{equation}
$$

$$
\begin{equation}
  \tan{\phi} = \frac{\gamma \omega}{\omega_0^2 - \omega^2}
\end{equation}
$$

What does this mean? When the frequency of the external electric field $$\omega$$ approaches the intrinsic frequency of the oscillator $$\omega_0$$ we get a higher and higher amplitude:  the distance between the electron and the core becomes larger and larger. Also we get a phase-shift between the external field and the oscillation of $$\frac{\pi}{2}$$ when $$\omega$$ approaches $$\omega_0$$ (look at these plots: amplitude against $$\omega/\omega_0$$ and $$\phi$$ against $$\omega/\omega_0$$).
