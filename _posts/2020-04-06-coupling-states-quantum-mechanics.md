---
layout: post
title: The coupling of states in quantum mechanics
description:
summary:
tags: [physics]
---

Consider a simple quantum mechanical system consisting of two eigenstates $$\ket{0}$$ and $$\ket{1}$$. A coupling between these two states means that there is a non-zero probability of a particle to go from one state to the other. Physically a coupling between two states is always achieved only by external influences. For example, light can couple different states in an atom. An electron can absorb a photon and go to a higher energy state, thus we can say these two states are coupled by the photon.

Generally there are some physical quantity changes associated with such a transition. In simple terms: when a particle goes from one state to another state, something is changed. For example in case of photon absorption the energy of the electron will increase.

How do we calculate such changes in physical quantities in quantum mechanics? Let's consider the energy.

Generally the Hamiltonian can be written as:

$$
H_{fi} = \left< f \middle| \hat{H} \middle| i \right>
$$

If $$f \ne i$$, $$H_{fi}$$ is the energy difference between the final state $$\ket{f}$$ and the initial state $$\ket{i}$$. The sign of $$H_{fi}$$ determines the energy gain or loss.

$$H_{fi}$$ can be calculated by an integral:

$$
H_{fi} = \left< f \middle| \hat{H} \middle| i \right> = \int{\psi_f^* \hat{H} \psi_i dx}
$$
