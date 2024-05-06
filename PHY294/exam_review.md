# Quantum Mechanics
*by jchoi*

## Lecture 1 
### Photoelectric Effect
- Light is quantized. 
 $$E = h \nu_o + \frac{1}{2} mv^2$$  
### Emission Spectrum of Hydrogen: 
- Light of discrete wavelength excites the electron to a higher energy level. 
- $$\Delta E = E_2 - E_1 = h \nu$$ 
- $$ \frac{1}{\lambda} = R_H \left( \frac{1}{n_1^2} - \frac{1}{n_2^2} \right)$$


## Lecture 2

### Bohr Model of the atom
- The centripetal force of the electron in balanced by the electrostatic acctraction between the electron and the nucleus: 
$$F = \frac{m_e v^2}{r} = \frac{1}{4 \pi \varepsilon_0} \frac{e^2}{r^2}$$
- In addition, the energy of the electron is given as the sum of the kinetic and potential energy:
$$E = \frac{1}{2} m_e v^2 - \frac{1}{4 \pi \varepsilon_0} \frac{e^2}{r}$$
- By assuming that the angular momentum is quantized as $l = m_e vr = \frac{nh}{2\pi}$, we are able to derive the energy levels of the hydrogen atom: 
$$E_n = - \frac{m_e e^4}{8 \varepsilon_0^2 h^2 n^2}$$

### De Broglie Wavelength
- The wavelength of a particle is given by $\lambda = \frac{h}{p}$. The wave properties of matter is only relevant when the de Broglie wavelenght is comparable to the size of the object.

- It was believed that electrons behave like a standing wave in the hydrogen atom, as such, the length of the wave must fit the circumference of the orbit: 
$$ 2\pi r = n \lambda \rightarrow 2 \ pi r = n \frac{h}{m_e \nu} \implies  m_e \nu r = \frac{nh}{2\pi}$$ 
- *Which is exactly the quantization of the angular momentum in the Bohr model.*

### Schrödinger Equation
#### Particle in a 1D box
- Recall particle in a box problem with an infinite square well. We guess the wavefunction to be a sine wave $\psi(x) = A \sin(kx) + B \cos(kx)$, with boundary conditions $\psi(x) = \psi(a) = 0$, thus, $A \sin(ka) = 0 \implies ka = n\pi \implies k = \frac{n\pi}{a}$. We also know that $k = \frac{2\pi}{\lambda}$, thus, $\lambda = \frac{2a}{n}$. Using the de Broglie wavelength, we find the quantized energy levels of the particle in a well to be: 
$$ E_n = \frac{p_n^2}{2m} \implies E_n = \frac{n^2 \hbar^2}{2m a^2}$$
#### Particle in a 2D box
- We have that $$f(x,y) = \begin{cases} 0, 0\leq x \leq a \text{ and }0 \leq y \leq a \\ \infty \end{cases}$$
We write the PDE as $$\nabla^2 \psi = \frac{2m}{\hbar^2} (E - V) \psi$$
- We guess the wavefunction to be equal to some separable function $\psi(x,y) = X(x)Y(y)$. Through differentiation, we find $\frac{X''(x)}{X(x)} = -k_x^2$  and $\frac{Y''(y)}{Y(y)} = -k_y^2$. We realize that these are two separate ODEs which are the same as in the 1D case, so $\psi = \sin(k_x x) \sin(k_y y)$. We find the energy levels to be:
$$E_{n_x,n_y} = \frac{\hbar^2 \pi^2}{2m} \left( \frac{n_x^2}{a^2} + \frac{n_y^2}{b^2} \right)$$

## Lecture 3

### Hydrogen Atom
Writing the Schrödinger equation in spherical coordinates, we have: 
$$\nabla^2 \Psi = \frac{2m}{\hbar^2} (E - V) \Psi$$
To solve the wave equation for hte hydrogen atom, we apply separation of variables: 
$$\Psi = R(r) \Theta (\theta) \Phi(\phi)$$
- We find that $\psi(r, \theta, \phi) = R_n(r) \Theta_{lm}(\theta)  \phi_m (\phi)$
- Where $n, l, m$ are called the quantum numbers. 
    - $n = 1,2,3, ...$ is the principle quanum number: determines the size an energy of an orbital through $E_n = - \frac{E_r}{n^2}$ 
    - $l = 0,1,2,...,n-1$ is the angular momentum number: defines the 3D shape of the orbital within a shell 
    - $m = -l, -l+1, ..., 0, ..., l-1, l$ is the magnetic quantum number: determines the orientation of the orbital in space
- No two electrons in an atom can have the same set of quantum numbers.
- The ground state is $n=1, l =0, m = 0$ 
    - Total angular momentum is quantized as $l = \sqrt{l(l+1)} \hbar$
    - The total angular momentum can be projected onto the z-axis where $L_z = m \hbar$


### Probability Distributions
 - Recall in PHY293, we were working with 1D, now in radial coordinates, we note that the probability of finding an electron in a shell $r$ to $r + dr$ is given by $P(r) = 4\pi r^2 \Psi^2 dr$


- For the 1s orbital, we see a maximum that occurs at $r = a_0$, which is the Bohr Radius, meaning that the electron in the 1s orbital is most likely to be found at the Bohr radius.

- Note, the number of nodes in the radial probabliity distribution $P(r)$ is $n-1$ where $n$ is the principle quantum number.

![](exam_review_1.png)


## Lecture 4

### Zeeman Effect 
- Splitting of spectral lines in the presence of a magnetic field. This is a result of the angular momentum $L_z = m \hbar$ which generates a magnetic dipole and moment $\mu$. 

- The spin quantum number $m_s$ takes on values of $\pm \frac{1}{2}$, so if the electrons spins are anti parallel, they are able to occupy the same orbital.

$$ \Delta E = m \mu_B B$$ 


## Lecture 5

### 2-Body Problem 
- We now have to worry about the interaction between two electrons, which makes the Schrödinger equation unsolvable. This is all due to the Coulomb potential between the two electrons: 
$$V_{\text{electron electron}}(r) = \frac{e^2}{4\pi \varepsilon_0 r_{12}}$$

#### IPA
We find an approximate solution called the independent particle approximation. 

1) We treat each electron as moving in a time average potential defined by the other electron. i.e. we assume that the potential is $U(r) = -Z_{\text{eff}} \frac{ke^2}{r}$, where the effect of the other electrons is smeared out to be radially symmetric. 

2) We then solve for $e_1$ as a 1 electron problem (Hydrogem atom) in the potential $U'(r_1, r_2)$. We are able to then define a new $\Psi'$ and potential energy for $e_2$ 

3) We repeat the loop until the calculated energy converges to the lowest possible energy 


#### Variational Theorem
Used to determine $Z_{\text{eff}}$ in the IPA. The theorem states that the expectation value of the energy of a trial wavefunction is always greater than or equal to the ground state energy of the system.

1) Use a variational parameter $Z$: 
$$ \Psi(\mathbf{r_1}, \mathbf{r_2}) = e^{-Z_{\text{eff}} (r_1 + r_2)}$$ 

2) Determine $E$ interms of the variational parameter $Z$, and take the derivative and set it equal to zero, to find the optimal $Z_{\text{eff}}$
$$ \frac{dE}{dZ} = 0 $$




## Lecture 6

### What the electron "sees" 
- When $r$ is outside all of the other electrons, then the potential becomes 
$$ U = - \frac{ke^2}{r}$$, since the inner electrons screen the outer electron from the nucleus, thus the only charge that isn't screened is one from the nucleus. 

- When $r \rightarrow 0$, $U \approx - \frac{Zke^2}{r}$, since the inner electrons are no longer screening, so the potential experienced is much higher. 



### Multielectron Atoms
- With the hydrogen atom, energy levels only depend on the principle quantum number $n$, so orbitals are degenerate. 

Multielectron atoms, depend on $n$ and $l$. 

### Pauli Exclusion Principle
**No two electrons in an atom can have the same set of quantum numbers.**

- All electrons are identical, so we cannot distinguish between them. So wavefunctions must be symmetric or antisymmetric under exchange of electrons.
$\Psi(A,B) = \pm \Psi(B,A)$ 
    - Particles that have $\Psi(A,B) = \Psi(B,A)$ are called bosons like photons
    - Particles that have $\Psi(A,B) = - \Psi(B,A)$ are called fermions like electrons

- Electrons are fermions, so they obey the Pauli Exclusion Principle: no two electrons can occupy the same quantum state: 
    - So, let us assume that two electrons A and B occupy the same state then 
$$\Psi(A,B) = \Psi(B,A) \rightarrow \Psi(A,B) = - \Psi(A,B) \rightarrow \Psi(A,B) = 0$$ 
- So we find that the probability of this is 0 


## Lecture 7

### Covalent Bond for $H_2^+$
We use two protons with a distance $R$ between them; we only consider one electron—$H_2^+$ The wavefunction is equal to the linear combination of the two hydrogen atom wavefunctions, which is a superposition, this is also known as a molecular orbital:
$$\Psi = c_1 \Psi_1 + c_2 \Psi_2$$

Bonding MO: 
- $$\psi_+ = c_1 \psi_1 + c_2 \psi_2$$
- Construcitve interference between the two wave functions. Both wave functions are in phase.
- The bonding state has lower energy
- **Build up of electron density between the two nuclei**


Antibonding MO:
- $$\psi_- = c_1 \psi_1 - c_2 \psi_2$$
- Destructive interference between the two wave functions. Wave functions are out of phase.
- The antibonding state has higher energy
- **Decreased electron density between the two nuclei**

Nonbonding MO:
- $$\psi_0 = c_1 \psi_1 + c_2 \psi_2$$
- The constructive and destructive interference parts perfectly cancel out 

![](exam_review_2.png)


## Lecture 8, 9

### Formation of Molecular Wavefunctions 
When two atoms are brought together, bonding, antibonding and nonbonding orbitals are created. 
- A bonding orbital is created when the LCAO is in phase. They are also named $g$ orbitals 
- An antibonding orbital is created when the LCAO is out of phase. They are also named $u$ orbitals
- Nonbonding orbitals are lone pairs

### Orbital Overlap (Overlap Integrals)
The orbital overlap is $S_{ab}$ is the extent to which  $\Psi_a$ overlaps in space $\Psi_b$
When wave functions are orthogonal, their overlap integrl is zero, $S_{ab} = 0$


### Bond Order:
$$\text{Bond Order} = \frac{\text{numer of bonding electrons} - \text{number of antibonding electrons}}{2}$$

### MOs: 1s, 2s, 2p
We apply the Aufbau principle to fill the MOs with electrons, from lowest to highest energy. 
- Consider $He_2$, the bond order is 0 because two electrons fill out the $\sigma_{1s}$ MO and then the $\sigma^*_{1s}$ MO, leading to a bond order of 0 (hence why He is inert). 


### Note on MOs of homonuclear diatomics: 
There is orbital mixing around $Z = 7$, meaning that after $O_2$ and $N_2$ and $F_2$ the $\pi > \sigma_p$ in energy (**symmetrical**)




## Lecture 10

### Heteronuclear Diatomic Orbitals
- Same atoms: the contribution is equal, and the intreaction is purely covalent 
- Two atoms with different energy: the lower energy AO contributes more to the bonding MO, higher energy AO contributes more to antibonding
- Two atoms with large energy difference: ionic

### Electronegativity 
$$ | \Delta \chi | = \sqrt{ \chi_A - \chi_B}$$

### Dipole Moments 
- When there is a charge separation in a molecule (the center of positive charge does not coincide with the center of negative charge), a dipole moment is created.(defined from the positive to the negative charge).
$$ \mu  = qr$$ 

### Hybridization 
- The mixing of atomic orbitals to form new degenerate hydbrid orbitals. Through wave functions, a hybrid orbital is a linear combination of s and p atomic orbitals. Unhybridized p orbitals form $\pi$ bonds from the lateral overlap of their electron densities. Any other overlap is a $\sigma$ bond (head on). 

    - $sp$ hybridization: 2 hybrid orbitals, 1 s and 1 p orbital
    - $sp^2$ hybridization: 3 hybrid orbitals, 1 s and 2 p orbitals
    - $sp^3$ hybridization: 4 hybrid orbitals, 1 s and 3 p orbitals 
    $$\Psi_{sp^3} = \frac{1}{\sqrt{4}} (\Psi_s + \Psi_{p_x} + \Psi_{p_y} + \Psi_{p_z})$$
- This is an example of a tetrahedral geometry.


## Lecture 11
### Correspondence Principle
Quantum effects are important when the scale of the motion is comparable to the De Broglie wavelength of the particle.

In the classical limit, $\Delta E \ll kT$, the effects of quantum are blurred and the system behaves classically. 

Correspondence explains that there is a **continuous** bridge from discrete quantized conditions to classical conditions.
- Consider the particle in a box $$E= \frac{h^2 n ^2}{8mL^2}$$. We can see that as $n, m, L \rightarrow \infty$, the energy levels become continuous an classical. 



### Long Range Intermolecular Forces 
Ionic, covalent and metallic bonds 
- Metallic bonds are covalent bonding with different degrees of ionic character.

### Short Range Intermolecular Forces

- Ion Coulomb forces: between a polar molecule with a permanent dipole and an ion 
    -Potential function on the order of $1/r^6$
    - e.g. dissolving salt in water perturbs 100 water molecules

- The Hydrogen Bond: 
    - Hydrogen bonds to oxygen, nitrogen or fluorine
    - On the order of $1/r^6$

- Dipole-Dipole Interactions: 
    - Difference in electronegativity between atoms
    - On the order of $1/r^6$


- Ion induced dipole interactions: 
    - Ion polarizes an otherwise neutral atom, leading to a dipole moment
    - On the order of $1/r^4$

- Dipole induced dipole interactions: 
    - A dipole polarizes an otherwise neutral atom, leading to a dipole moment

- Induced dipole induced dipole interactions: 
    - Two neutral atoms polarize each other, leading to a dipole moment
    - Only when all the molecules are nonpolar


## Lecture 12
### Hydrogen Bonding
- Hydrogen atoms are bonded to oxygen nitrogen or fluorine 
    - The hydrogen is partially positive 
    - Chlorine does not form a hydrogen bond, since it's screened due to ionic bonding

- Hydrogen bond properties: 
    - Higher boiling points 
    - Higher density in the liquid phase 
    - Negative thermal expansion (expands in the solid phase)
    - High sepcific heat capacity
    - Anomalous surface tension

### Summary of Intermolecular Forces
- Ions present: 
    - Ions only: ionic bonding
    - Ion + polar molecule: ion-dipole force 
- Ions not present:
    - Polar molecules only:
        - Dipole dipole forces 
        - Hydrogen bonding (H bonded to O, N, F)
    - Polar + nonpolar molecules:
        - Dipole induced dipole forces 
    - Nonpolar molecules only:
        - Dispersion forces only


## Lecture 13
### Hydrogen Bonding again
- Water's hydrogen bond imposes a minimum volume constraint to drive hydrophobic collapse:
    - The hydrophobic effect is the driving force behind protein folding 
    - The hydrophobic effect is responsible for the forming of spheres in oil 
- The hydrogen bond connects long range forces, making it flexible allowing it to flow, but still strong enough for surface tension.

### Levinthal's Paradox
- The number of possible conformations of a protein is astronomical, so how does a protein fold so quickly?
- The protein folds through a series of intermediates, which are not random, but are guided by the hydrophobic effect.
- So, the assumption that all degrees of freedom are independent is wrong. 

## Lecture 14
### Photon absorption 
- The incoming photon is an EM wave which is able to excite an electron to a higher energy level 
- The electric field distort the electron density and changes its shape to a new stable configuration 2s to 2p

#### Spectroscopy 
- Measures the absorption of a photon 
- The spectrum has a finite width defined by the uncertainty principle $\Delta E \Delta t \geq \frac{\hbar}{2}$, where $\Delta t$ is the lifetime of the excitation 
- The potential energy is $U = \mu E$ where $\mu$ is the dipole moment 
- The expectation value for the electric field to create a dipole moment via the mixing of electron distributions has selection rules. 
    - Transitions are either allowed (high prob) or forbidden (low prob)

#### Selection Rules
- There is no dipole change if there is no transition in symmetry: e.g. $s \rightarrow s$ is forbidden, but $s \rightarrow p$ is allowed. Therefore, $\Delta l = \pm 1$
- There can be no change in overall spin: $\Delta S = 0$\

### Beer Lambert Law
- EM from a source of intensity $I_0$ is incident on a sample that is confined in a cell of length $b$. After it travels through the sample, the intensity is some measured $I$. 
- The chemical speciaes in the sample undergoes transitions that absorb the light. 
$$ \frac{I(\lambda)}{I_0(\lambda)} = e^{-\varepsilon(\lambda) c b}$$
- $\varepsilon$ is the molar absorptivity, $c$ is the concentration of the absorbing species, and $b$ is the path length of the cell.


### IR Spectroscopy
- A vibrating molecule behaves like 2 masses joined by a spring
- There is some restoring force $F = -kx$
- We apprxoimate the potential energy as a harmonic oscillator $U = \frac{1}{2} k x^2$
- The real potential is called the Morse potential 
$$ E_{vib} = \left( v + \frac{1}{2} \right) h \nu$$, where $v = 0, 1, 2, ...$ is the vibrational quantum number
- The selection rule is $\Delta v = \pm 1$

#### IR activity 
- Molecules have dipole moments which allows them to interact with IR (EM radiation)
- For a molecule to be IR active, we impose $$\frac{d \mu}{dr} > 0$$
- So the electric dipole must chagne with bond length during a vibration
- Although diatomic molecules have one vibration mode (stretching), it is symmetric, so there is no net change in dipole moment, so they are IR inactive.

#### Normal Modes of Vibration for Molecules of $N$ atoms 
- Diatomic: 1 normal mode
- Nonlinear: $3N - 6$ normal modes
- Linear: $3N - 5$ normal modes


## Lecture 15
### Quantum Treatment of the SHM 
- Let us assume that bonds are harmonic oscillators, so the potential energy is $U = \frac{1}{2} k x^2$
- We set up our boundary conditions: 
    - $\psi$ must be symmetric or antisymmetric at $x=0$
    - $\psi$ must go to $0$ as $x \rightarrow \pm \infty$
- We plug in our potential $U$ into the Schrödinger equation and solve for the wave function: 
$$\psi_n(x) = N_n e^{-\beta^2 x^2/2} H_n(\beta x)$$ 
- Where $H_n$ are the Hermite polynomials. We find that the energy levels are quantized as
$$E_n = \left( n + \frac{1}{2} \right) h \nu$$


![](exam_review_3.png)

Note how the energy levels are equally spaced, with zero point energy at $\frac{1}{2} h \nu$ (at 0K). 

Even number states are symmetric, odd number states are antisymmetric.
- Note by squaring the wave functions, we find the probability distribution of the SHM.

![](exam_review_4.png)


## Lecture 16
### Franck-Condon Principle
- The molecule undergoes a vertical transition to a higher vibrational state of the electronically excited state that is in the same vibrational state as the ground state.
    - The favoured transitions are those that have the same probabilties before and after (so more overlap)
    - In the excited state, there is distortion of the bond length, because they are higher in energy 
    - The molecule then relaxes to the lowest vibrational state of the excited state, emitting a photon (fluorescence)

    - Phosphorescence is the emission of light after **intersystem crossing** (spin flip) to the triplet state

![](exam_review_5.png)






---
# Thermal Physics
----
## Lecture 1
### Introduction to Thermal Physics
- When the number of particles $N$ becomes large, the behaviour is universally obesrved 


### Microscopic vs Macroscopic
**Microscopic**
- If we wanted to describe a gas by studying its behaviour microscopically, we would account for the positions and velocities of all hte particles. 
- The represents $3 \times N$ secodn order DEs, not possible to analytically solve 

**Macroscopic**
- Describing a system as a whole. We care about thermodynamic or macroscopic quantities. 


## Lecture 2
### Ideal Classical Gas
- We treat particles as point-like spheres. The ideal gas law is an example of **universal behaviour**: any gas sufficiently hot and dilute will obey it (see Lecture n)
$$ pV = NkT$$

### Derviation: 
- Derivation is not shown here 
- Note that $\bar{v}_x = \frac{1}{N} \sum v_{xi} =  0$ by isotropy, meaning that there is an equal number of particles moving in the positive and negative directions.
    - Thus, we square the individual velocities: $\bar{v}_x^2 = \frac{1}{N} \sum v_{xi}^2$, and call this the average speed squared.
- We also defined the room mean squared speed: 
$$\bar{\vec{v}^2} = \frac{1}{N} \sum \vec{v_i}^2 = \frac{1}{N} \sum v_{xi}^2 + v_{yi}^2 + v_{zi}^2 = 3 \bar{v}^2$$
- From the derivation which isn't shown here, we have that $kT = m \bar{v}^2 = \frac{1}{3}m \bar{\vec{v}^2}$. Therefore, we define the kinetic energy as: 
$$KE = \frac{1}{2} m \bar{\vec{v}^2} = \frac{3}{2} kT$$
- We can also define the root mean squared speed as:
$$v_{rms} = \sqrt{\bar{\vec{v}^2}} = \sqrt{\frac{3kT}{m}}$$
- Note: the average KE of an ideal gas is only dependent on temperature; however, the $v_{rms}$ depends on the mass of the particles. So lighter particles move faster than heavier ones at the same temperature 



## Lecture 3
### Equipartion Theorem
- As we saw in lecture 2, KE being a measure of temperature $kT$ is an example of the equipartion theorem.
- At thermodynamic equilibrium, the energy of the system is evenly distributed to its thermally active degrees of freedom. The average energy per dof of a molecule is: 
    - Translational: $\frac{1}{2} kT$
    - Rotational: $\frac{1}{2} kT$
    - Vibratonal: $ kT$ (technically there are 2 dof for each vibration mode)
- Thus, from the number of particles, we can calculate the internal energy of a gas, at some temperature and determine its heat capacity. 
$$U = \frac{f}{2} NkT$$
$$C_v = \frac{\partial U}{\partial T} = \frac{f}{2} Nk$$

- For a monoatomic gas, $f = 3$
- For a diatomic gas, $f = 5 +2(1)$ (3 translational, two rotational, 1 vibrational)
    - Note the vibrational mode might not be thermally active if the temperatures are too low. 
- Linear molecules have 3 translational, 2 rotational, 3N-6 vibrational modes
- Nonlinear molecules have 3 translational, 3 rotational, 3N-5 vibrational modes
- For solids in a lattice, atoms cannot translate or rotate; however, they may vibrate in all 3 directions, so $f= 6$ since each vibrational mode comes w/ a potential and kinetic energy

### Heat Capacity
- Heat capacity is not constant with increasing $T$ until around $1000K$. Below this temperature, the $C_v$ increases in discrete steps. At lower temperatures, movements are only translational; however, eventually, the rotational, then vibrational modes become thermally active.



## Lecture 4
### Heat Transfer and the First Law of Thermodynamics
- Temperature change leads to a change in internal energy. We define the increase in internal energy as the heat: $\Delta U = \frac{3}{2} Nk \Delta T = Q$

- Compression of a gas leads to molecules that collide with the piston, increaseing $T$ and $U$. Thus the change in internal energy is $\Delta U = W$

- Combining the two, the change in the internal energy must tbe the sum of the heat absorbed $Q$ and the work done on the system $W$:
$$ \Delta U = Q + W$$

- We can rewrite the first law as $dU = \delta Q - p dV$. Note the negative sign because a compression $dV < 0$ and does work on the system. 

### Quasistatic Processes
- A process is one that is slow enough such that each step of the process is allowed to reach TD equilibrium. There is uniform density and pressure, with constant temperature. 
- We are able to compute the work done on the system by summing all the individual steps:
$W = - P_1 \Delta V_1 - P_2 \Delta V_2 - ... - P_n \Delta V_n$ as we take $n\rightarrow \infty$, we have an intergal:
$$W_{done on system} = - \int_{V_i}^{V_f} P dV$$

- However, we do not know the conditions at which the process occurs, so the pressure is function of $V, T$. However, from the ideal gas law, we know that $P = \frac{NkT}{V}$ 

#### Isothermal Process $T = C$
- Consider the expansion or compression at constant temperature (water bath):
$$ W = -NkT \int_{V_i}^{V_f} \frac{dV}{V} = -NkT \ln \left( \frac{V_f}{V_i} \right)$$
- Since $\Delta T = 0$, the internal energy is constant which implies that compression requires an outflow of heat, and a expansion requires an inflow of heat:
$$\Delta U = 0 \implies W = - Q$$

- In addition, since $PV = NkT$, we know that $PV = C'$ 

#### Adiabatic Process $Q = 0$
- A process that is isolated from surrounds, so there are no heat losses or gains. Adiabatic processes can be quasistatic and non-quasistatic. In the non-quasistatic case, there is no work done. 
- In a quasistatic process, we have that $PV = NkT$ and $U = \frac{f}{2} NkT$ and $dU = - p dV \impliedby Q = 0$
- By rearranging, we find that $\left( \frac{V_f}{V_i} \right)^{\frac{f+2}{f}} = \frac{p_2}{p_1}$, implying that $$V_1^{\gamma} p_1 = C$$ 
- We define the adiabate constant as $\gamma = \frac{f+2}{f}$, where $f$ is the number of degrees of freedom.
- Since $\gamma > 1$, volume and pressure are inversely related.
- Also, we know that the adiabatic PV curve is steeper than the isothermal curve.
    - We can think of an adiabatic process as a process that moves across isothermal curves. 

## Lecture 5
### Heat Capacity
- The heat needed to increase the temperature of a substance by 1K.

#### Constant Pressure 
- Heating at a constant volume means that no work can be done: $dU = \delta Q$. Applying the equipartition theorem, the internal energy is given as $U = \frac{f}{2} NkT$, thus the heat capacity is found by differentiating w.r.t temperature:
$$C_v = \left( \frac{\partial U}{\partial T} \right)_V = \frac{f}{2} Nk$$

#### Constant Volume 
- Heating up a gas at constnat pressure leads to $Q = \Delta U - (- p \Delta V)$, we get that $C_p = \frac{f+2}{f} Nk = \gamma C_v$, where gamma is the adiabate constant. As such we always have that $C_p > C_v \impliedby \gamma >1 $



## Lecture 6
### Discrepancy in Heat Capacity
- We calculate the minimum temperature needed for rotations to be thermally active. We get the equipartition theorem, stating that $E \approx kT$. So at $T \approx 1000 K$, the rotational modes become thermally active.

### Introduction to Statistical Mechanics
- In the TD limit, energy can be distributed among many ways to its particles. Each of the ways in which the energy can be distributed is called a **microstate**, whereas the total energy of the system is the **macrostate**.

- The fundamental postulate of statistical mechanics states that *all accessible microstates are equally likely*
    - An accessible microstate is one that posses a total energy, matching a given macrostate. 
    - The multiplicity function is thus, the number of microstates accessible to a given macrostate. The multiplicity function, $\Omega$ allows us to describe the system. 

- We can no longer describe the system with trajectories. Thus we study probability distributions, and with large $N$, probabilities become certainties ($\delta$ functions). This is the beauty of stat mech. 



## Lecture 7 

### Electronic Paramagnet 
- The macrostate of a paramagnet is the macroscopic quantity of energy.
- We can model the material as a lattice. Each of the $N$ atoms has two dof, spin up and spin down: $s_i = {+1, -1}$ for $i = 1, 2, ... N$. 
    - Thus, there are $2^N$ possible microstates because we ignore spin-spin interactions (so each microstate is independent)
- The energy of the system is $E = - \mu B N_{up} = - \mu B \sum s_i = - \mu_o B S$ 
- Note that $S$ is the total spin of the system. We see that there are $N+1$ possible values of $S$, so we say $S$ has $N+1$ possible macrostates.
    - $N = N_{up} + N_{down}$ and $S = N_{up} - N_{down}$, so $S = 2 N_{up} - N$ 

- The multiplicity of a general macrostate is the number of accessible microstates given som $N_{up}$: 
$$\Omega(N_{up}) = \frac{N!}{N_{up}! (N-N_{up})!}$$


### Einstein Solid
- Collection of $N$ simple harmonic oscillators independent of each other 
- The $i$-th oscillator has some energy $\hbar \omega (q_i + \frac{1}{2})$, where $q_i = 0, 1, 2, ..., N$. Note we ignore the constant term $\frac{1}{2}$ (zero point energy)
- Microstate = $\{q_1, q_2, ..., q_N\}$, so the number of microstates is countable infinite in the TD limit. 
- Macrostate: $q = \sum q_i$ 
- We find the multiplicity function by assuming that $N-1$ partitions divide $q$ units of energy. These objects can be partitioned across the system:
$$\Omega(q) = \frac{(q+N-1)!}{q!(N-1)!}$$

#### Energy Flow
- Consider two systems $N_A$ and $N_B$ with $q_A$ and $q_B$ units of energy. $q_A$ can exchange energy with $q_B$, so $q_A + q_B = q_A' + q_B' = c$. So the multiplicity function of $A$ is $\Omega(N_A, q_A')$ and that of B is $\Omega(N_B, q - q_A')$.
- The probability of observing some $(q_A, q - q_A')$ is proportional to the product of the individual multiplicities 
- This is because for each of the $\Omega_A$ microstates available to $A$, there are $\Omega_B$ microstates available to $B$, hence the product 



## Lecture 8

### General Thermal Equilibrium - Statistical Definition of Temperature and Energy

-   Consider system 1 with energy $E_1$ and system 2 with energy $E_2$
    that are brought together and allowed to reach thermal equilibrium.

-   In TD equilibrium, the total energy is $E = E_1 + E_2$. Assuming the process is adiabatic, we have $E_1$ and $E_2 = E - E_1$

-   The probability of a particular $E_1$ is denoted as $P(E_1)$:
    $$P(\Delta) = \frac{\Omega_1(E_1) \Omega_2(E - E_1)}{{\sum^{E/2}_{\bar{\Delta} = -E/2}} \Omega_1(E_1) \Omega_2(E - E_1)}$$

-   We aim to find $E_1$ for the maximum probability of $P(E_1)$.
    Thus we differentiate the numerator with respect to $E_1$
    $$\frac{\partial }{\partial \Delta} \Omega_1(E_1) \Omega_2(E-E_1) = 0$$

-   Differentiation eventually leads to
    $$\frac{\partial }{\partial E} k\ln \Omega_1 (E_1) = \frac{\partial }{\partial E} k\ln \Omega_2 (E_2) \implies \frac{1}{T_1} = \frac{1}{T_2}$$

-   Each term is a property of a single system, so when they are brought
    into contact and reach TD equilibrium, their properties, i.e.
    temperatures must be equal.

-   We define, entropy as $$S(E, N,V) = k \ln \Omega (E,N,V)$$

-   The inverse temperature of a system is defined as
    $$\frac{1}{T(E,N,V)} = \left(\frac{\partial S}{\partial E}\right)_{N,V}$$

-   **Some Important Notes:**  A closed system evolves s.t. entropy is maximized. Since each macrostate must have a multiplicity of at least 1, $\Omega \geq 1 \implies S \geq 0$

    -   In the case of the electronic paramagnetic, the state
        $N_{up} = N$ only has one microstate, so $\Omega = 1$, $S = 0$,
        thus this system is very ordered

    -   If the system is defined by the macrostate
        $N_{up} = \frac{N}{2}$ , then $S \gg 1$, as the number of microstates acessible $\Omega$ by this macrostate is very large, so this system is disordered. 

    -   We can also consider entropy as the inverse of how much information
        we have about a system. When $N_{up} = N$, we know the microstate the system is in. In the case of $N_{up} = \frac{N}{2}$, we have little information about the
        microstate the system is in.

    -   Finally notice that $T\geq 0$ because
        $\frac{\partial S}{\partial E} \geq 0$, so if you add energy
        into the system, there are more ways to distribute the energy,
        so entropy increases

    -   Multiplicity is multiplicable $\Omega_{1+2} = \Omega_1 \Omega_2$
        since the multiplicity functions are logarithms

    -   Entropy is additive $S_{1+2} = S_1 + S_2$


## Lecture 9

### On the Einstein Solid: consideration of the ratio $q/N$

-   In the TD limit where $N, V, E \rightarrow \infty$ (all extensive
    properties), and density and energy density is kept fixed, the
    results of statistical mechanics become certainties.

-   The E.S. was defined with $E = \hbar \omega q$ (zero point energy is ignored) with $\Omega = \frac{(N-1+q)!}{(N-1)!q!}$. Keeping $q/N$
    fixed, we consider two constraints $q/N \gg 1$ and $q/N \ll 1$.

-   In the **first limit,** the multiplicity function becomes
    $\Omega = \frac{(N+q)!}{N!q!}$, recalling that $S =k \ln (\Omega)$,
    we have that $\ln(\Omega) = \ln (N+q)! - \ln N! - \ln q!$, for large
    $N$ on the order of $N_a$, we make use of the Stirling
    approximation: $\ln n! = n \ln n$:
    $$\ln(\Omega) \approx (N+1) \ln(N+1) - N \ln N - q \ln q$$

-   After some derivation, we get that
    $\ln(\Omega) = N \ln \frac{qe}{N} \rightarrow \Omega = (\frac{qe}{N})^N$
    , thus entropy for the limit of large $q/N \gg 1$ is
    $$S = k \ln \left(\frac{qe}{N}\right)^N \rightarrow S = kN \ln \frac{Ee}{\hbar \omega N}$$

-   $\frac{1}{T} = \frac{\partial S}{\partial E} = \frac{kN}{E} \implies \frac{E}{N} = kT$.
    When $q/N \gg 1$, we have that $kT \gg \hbar \omega$, which are the
    conditions required for equipartition theory.

-   In the **second limit** $q/N \ll 1$, we realize that the
    multiplicity function is symmetric $\Omega(N, q) = \Omega(q,N)$, so
    limit 2 is equal to the limit of 1 with $q$ and $N$ switched:
    $\Omega = (\frac{Ne}{q})^q$, thus entropy is
    $$S = k \ln \left(\frac{Ne}{q} \right)^q \rightarrow S = k \frac{E}{\hbar \omega} \ln \frac{N e \hbar \omega}{E}$$

-   $\frac{1}{T} = \frac{\partial S}{\partial E} = \frac{k}{\hbar \omega} \ln \frac{N\hbar \omega}{E}$,
    solving for the energy density
    $\frac{E}{N} = \hbar \omega e^{-\frac{\hbar \omega}{kT}}$. Clearly,
    equipartition does not hold in the small limit. If the energy of the
    system is small, the temperature is too low to excite the
    vibrational modes of the particles, thus the energy per particle
    drops exponentially.

## Two Einstein Solids

-   Consider two Einstein solids with the same number of oscillators:
    $q_1 + q_2 = q = C$ and both satisfying the limit
    $\frac{q}{N} \gg 1$ (high temperature regime). How will the energy
    distribute among the two systems? Define, $q_1 = q/2 + X$, $q_2 = q/2 - X$.
    The multiplicity function of both systems is proportional to the
    probability of observing some state $X$.
    $P(X) \sim \Omega (q_1, q_2, N, N) = (\frac{e q_1}{N})^N (\frac{e q_2}{N})^N = (\frac{e q/2 + X}{N})^N (\frac{e q/2 - X}{N})^N = (\frac{e^2}{N^2})^N (\frac{q^2}{4} - x^2)^N$.

-   Now take the ratio of $\Omega(X)$ to $\Omega(0)$. Through algebra we
    end up with
    $$\frac{P(X)}{P(0)} = \frac{\Omega(X)}{\Omega(0)}= \frac{(\frac{e^2}{N^2})^N (\frac{q^2}{4} - x^2)^N}{(\frac{e^2}{N^2})^N (\frac{q^2}{4})^N} = \left(1- (\frac{x}{q/2})^2\right)^N$$

-   $$\ln \frac{P(x)}{P_o} = N \ln \left(1- \left(\frac{x}{q/2} \right) ^2 \right)$$

-   Where $\frac{x}{q/2}$ is called the relative energy balance. If we
    consider small energy balance changes, we approximate the above as
    $-N \left( \frac{x}{q/2} \right)^2$, thus the probability function
    becomes: $$P(x) = P_o e ^{-N\left( \frac{x}{q/2} \right)^2}$$

-   Thus, the probability distribution of $X$ (the difference in
    energies) is a Gaussian that is **only non-zero for one value**,
    that value is $x=0$, meaning that the probability of observing some
    $0$ energy difference between the two systems is a certainty. (The
    PDF looks like $\perp$, a $\delta$ function)

    -   We call $\frac{x}{q/2}$ the fractional energy distribution, and
        is helpful when estimating probabilities. Let us consider a
        fractional energy imbalance between systems 1 and 2 of $10^{-5}$ (which
        is already tiny!). Then
        $\frac{P(\frac{2x}{q} \sim 10^{-5})}{P(0)} = e^{-10^{23} 10^{-10}} \approx e^{-10^{13}}$.
        Thus, this essentially says that the probability that the energy
        imbalance is as small as $10^{-5}$ is 0. 







## Lecture 10

### Thermodynamic Potential

- Second Law of Thermodynamics: A closed system will evolve towards a TD equilibrium state that maximizes the entropy (subject to imposed constraints)

- Given a closed system with energy $E$, particles $N$ and volume $V$, we define its entropy as $S(E, N, V) = k \ln \Omega (E, N ,V)$. We think of $S$ as a **TD potential** which determines the approach of TD equilibrium. A similar analogy is how a potential $\mathbf{U}$ defines equilibrium in classical systems $\mathbf{F} = - \nabla \mathbf{U}$.

-   $S$ wants to maximize, so the gradient of $S$ as a function of
    $E, N,V$ (TD coordinates) play a role in the force that drives a
    system to TD equilibrium.

-   So we if we have $\frac{1}{T_1}> \frac{1}{T_2}$, then energy will flow until the two are equal



### General Properties of Entropy

-   From the ES for $ kT \gg \hbar \omega$, then,
    $S \approx kN \ln \frac{Ee}{N\hbar w}$: meaning more energy, more microstates (linear term $N$ beats $\ln(1/N)$).

-   Properties to consider:

    -   The entropy $S$ curve as a function of $E$ is an increasing
        function, so as $E$ increases, so does $S$ for $T \geq 0$

    -   The second derivative of entropy w.r.t energy is negative,so $\frac{\partial S}{\partial E}$ decreases, and so temperature increases, since it is the inverse of the entropy.

    -   So energy transfer requires $C_v > 0$. All "normal" TD systems
        have $C_v >0$. Consider two systems with $T_1 > T_2$, as 1 gives
        away energy, $T_1$ decreases since $C_{v1} >0$, conversely, as
        energy flows into system 2, $T_2$ increases since $C_{v2} > 0$
        until $T_1 = T_2$.

    -   Now let's suppose $C_v < 0$, then heat loss leads to an
        increased temperature, and heat gained leads to a decreased
        temperature, it is clear that this system has no equilibrium,
        and one system will end up with all the energy, and one without
        any.

-   Find the multiplicity function, then you get the entropy and can
    define the system's extensive properties.



## Lecture 11

### Ideal Gas (Sackur-Tetrode Equation)
*For a given internal energy of a monoatomic ideal gas $U$, how many microstates are there?* 
- Recall that the total energy $U$ is equal to the sum of all kinetic energies, which can be expressed i.t.o momenta: 

    $$U = \sum_{i=1}^{N}\frac{\vec{p_i}^2}{2m} \rightarrow \sum_{i=1}^N \vec{p_i}^2  = \sum_{i=1}^N p^2_{xi} + p^2_{yi} + p^2_{zi} = 2mU$$

-   Recall the particle in a 3d box problem, the momentum can be expressed
    as the sum of the squares of the quantum numbers associated with
    each coordinate: $p_{xi}^2 = \frac{\pi \hbar}{L} n_x$.

-   Thus we take the sum of all the quantum numbers which is $3N$ since
    each particle can move in all three directions:
    $n_{1x}^2 + n_{1y}^2 + n_{1z}^2 + ... + n_{Nx}^2 + n_{Ny}^2 + n_{Nz}^2 = \frac{2mU}{\frac{\pi \hbar}{\omega}} = R^2$
    , which represents a sphere in $\mathbb{R}^{3N}$.

-   Thus, we define the multiplicity function
    $\Omega(N, U,V) = \text{microstates with energy} \in (U - \frac{\Delta}{2}, U + \frac{\Delta}{2})$.
    Geometrically, this represents two spheres drawn in the
    $\mathbb{R}^{3N}$ coordinate plane that differ in radius by some 
    $\Delta$. $\Omega = A_{3N-1}(R)\Delta$. Thus, for small enough
    $\Delta$, the multiplicity function is the area of the sphere times
    $\Delta$

-   **Corrections:**

    -   We must partition our space since we only take the positive
        values ($n_{kx,ky,kz} > 0)$. Thus, we divide by a factor of
        $2^n$ for each dimension $n$ (Intuition: circle in
        $\mathbb{R}^2$ gets divided by 4, the sphere in $\mathbb{R}^3$
        gets divided by 8)

    -   Gibbs factor (extensive property): if you double all the
        properties of a system, you would expect entropy to double as
        well, hence the need for $\frac{1}{N!}$

    $$\Omega(N,U,V) = \frac{2\pi ^{\frac{3}{2}}N}{N! (\frac{3}{2}N-1)! 2^{3N}} \left( \frac{\sqrt{2mU}L}{\pi \hbar} \right)^{3N-1}$$

-   Now, we find that the entropy $S$ of an ideal gas is (also known as
    the Sackur Tetrode Equation):
    $$S(T, N, V) =  k_B N\left( \ln \left[ \frac{V}{N} \left( \frac{4 \pi m U}{h^2} \right)^{\frac{3}{2}} \right] + \frac{5}{2} \right)$$

-   Note the following properties of the equation:

    -   The entropy $S$ is on the same order as $k_B N$

    -   The doubling of all extensive properties $N, U, V$ leads to the
        doubling of entropy (due to the Gibbs factor)

    -   $S$ increases with $U$ and then reaches a maximum

    -   If we lower $U$ enough, then the argument of the log becomes
        less than $1$, and entropy becomes negative. As such, this
        formula is only valid for sufficiently high energies.

    -   Similarly, if $\frac{V}{N}$, the volume per particle, becomes
        small enough (denser gas), the entropy can become negative.

        -   Thus, at low temperatures and high densities, the Ideal Gas
            Law does not apply because entropy becomes negative which is
            not possible.

-   Taking the partial derivative to find the temperature:
    $$\frac{1}{T} = \frac{\partial S}{\partial U} = kN \frac{3}{2} \frac{1}{U} \rightarrow U = \frac{3}{2}NkT$$

-   Which implies that equipartition is a property of an ideal gas,
    moreover, we can take
    $\frac{P}{T} = \frac{\partial S}{V} = \frac{kN}{V} = \frac{P}{T} \rightarrow pV = NkT$,
    which is the ideal gas law.



## Lecture 12

## When is a Gas No Longer Ideal?
*We always say that a gas has to be hot and dilute enough. What does \"enough\" mean?*
-   With the Sackur-Tetrode Formula, we can quantify
    these statements.
    $\frac{\partial S}{\partial U} = \frac{1}{T} \implies U = \frac{3}{2}kNT$

-   We introduce the de thermal Broglie wavelength
    $\lambda_{th} = \frac{h}{\sqrt{mKT}}$, which is the de Broglie
    wavelength but with $p = \sqrt{mkT}$; as such, a larger mass and
    temperature will decrease the thermal wavelength:
    $\lambda_{th} \propto \frac{1}{\sqrt{mT}}$.

-   Define the characteristic length between particles as
    $l = (\frac{V}{N})^{\frac{1}{3}}$. Thus, the ideal gas law holds
    when $l \gg \lambda_{th}$, where the typical distance between
    particles is much greater than their thermal de Broglie wavelength,
    and the quantum effects are not as noticeable. Conversely, when
    $l \ll \lambda_{th}$---where the typical distance is much smaller
    than the thermal wavelength, the ideal gas law no longer holds, and
    the gas is deemed \"quantum\".
    $$S \approx kN \ln \left(\frac{l}{\lambda_{th}}\right)^3$$

-   We can make a gas \"quantum\" by decreasing $l$ or increasing
    $\lambda_{th}$

    -   If we increase the number density of particles, we decrease the
        $\frac{V}{N}$ term, which decreases the characteristic length
        $l$

    -   If we lower the temperature, we increase the de Broglie
        wavelength $\lambda_{th}$

-   These statements make sense as they oppose the behaviour of an ideal
    gas: low density and high temperatures. To summarize, a gas becomes
    quantum when
    $\frac{h}{mkT}=\lambda_{th} \approx l = (\frac{V}{N})^{1/3}$





## Lecture 13
### Clausius Definition of Entropy
- Given a system with energy $E$, fixed volume $V$, and number of particles $N$, the entropy is given as $$S(E,V,N) = k \ln \Omega(E,V,N)$$. 
- Consider keeping $N$ and $V$ fixed, then for an infinitesimal change in energy $\Delta E$ we have $\frac{\Delta S }{\Delta E} = \frac{1}{T} \rightarrow S = \frac{\Delta E}{T}$
- Since we kept the volume fixed, we have that $\Delta U = \delta Q$, and so $$\Delta S = \frac{\delta Q}{T}$$ 

- It was also that $\Delta S \geq 0$ for all closed systems
    - Thus, there is a unidirectional flow of heat; heat always flows from hot to cold. 
    - The loss of entropy of the hotter object is always less than the gain in entropy of the colder object: 
    $$\Delta S_{\text{hot}} = -\frac{\delta Q}{T_{\text{hot}}} \leq \Delta S_{\text{cold}} = \frac{\delta Q}{T_{\text{cold}}} \impliedby T_{\text{hot}} > T_{\text{cold}}$$
    - Similarly, $$\Delta S_{h+c} = \Delta S_h + \Delta S_c = \Delta Q (-\frac{1}{T_h} + \frac{1}{T_c}) \geq 0$$


### Heat Capacity and Entropy 


- $C_v = \frac{\Delta U}{\Delta T}$, and with $\Delta S = \frac{\Delta U}{ T} = c_v \frac{\Delta T}{T}$. Integrating this expression, from temperature $T_1$ to temperature $T_2$ we have the change in entropy: 
$$ S(T_2) - S(T_1) = \int_{T_1}^{T_2} \frac{C_v(T)}{T} dT$$ 
- Recall for an ideal monoatomic gas, $C_v = \frac{3}{2} kN$, which, independent of $T$. $$S(T_2) - S(T_1) = \frac{3}{2} \int_{T_1}^{T_2} \frac{dT}{T} = \frac{3}{2} kN \ln \frac{T_2}{T_1}$$

#### Heat Capacity at Low Temperatures 

- Imagine taking $T_1$ to be large and $T_2 \rightarrow 0$, then we would find that $\Delta S \rightarrow - \infty$, which is a contradiction. 
- **We cannot have a $C_v$ which is temperature independent at arbitrarily low temperatures**.
- Thus, in order for $S(T_2) - S(T_1)$ to be finite as $T_2 \rightarrow 0$, we require $\int^{T_2 \rightarrow 0} \frac{C_v(T)}{T} dT $ to converge.
- It is sufficient to impose that as $T_2 \rightarrow 0 \implies C_v \sim T^{\alpha}$, where $\alpha \geq 0$. This is because $$\int \frac{T^\alpha \ dT}{T} = \int T^{\alpha - 1} dT = \frac{T^{\alpha}}{\alpha}$$ which converges for $\alpha \geq 0$.

### Metals as Ideal Quantum Gases (Fermi Gases)
- Electrons within a metal are delocalized; however, they are dense (compared to an ideal classical gas) and have large de Broglie wavelengths due to their small mass. Thus we can treat them as a quantum gas: $\lambda = \frac{h}{p} = \frac{h}{\sqrt{mkT}}$. 
- For a system like this, we take $C_v \sim aT + b T^3$ where $aT$ is due to the electrons and $bT^3$ is due to the lattice vibrations "phonons".





## Lecture 14 


### Chemical Diffuse Potential 
*Consider two systems with $U_1, N_1, V_1$ and $U_2, N_2, V_2$ what happens if we allow both the exchange of $U$ and $N$?*

---
- Initially we keep the barrier fixed, the energy will exchange until thermal equilibrium is reached. Systems have $U_1', U_2'$ 
- We want to determine some, $U_1''$ and $U_2''$  and some $N_1''$ and $N_2''$ such that the total entropy is maximized: 
$$ S = S_1(U_1'', N_1'') + S_2(U- U_1'', N - N_1'')$$
- Thus, want the derivatives w.r.t to $U_1''$ and $N_1''$ to be zero: 
$$ \frac{\partial S}{\partial U_1''} = 0 \implies \frac{\partial S_1}{\partial U_1''} = \frac{\partial S_2}{\partial U_2''}$$
$$ \frac{\partial S}{\partial N_1''} = 0 \implies \frac{\partial S_1}{\partial N_1''} = \frac{\partial S_2}{\partial N_2''}$$
- Therefore, we require that the system property $\frac{\partial S_i}{\partial N_i}$ for both systems must be equal 
---

- We define $-\frac{\mu}{T} = \frac{\partial S}{\partial N}$, where $\mu$ is called the chemical potential 
- The negative sign means that particles will flow from regions with higher chemical potential to lower chemical potential. 


#### Thermodynamic Definition of Pressure:
- If the volume is exchanged, then we have that $V_1 + V_2 = V$ then, 
$$\frac{1}{T_1} = \left(\frac{\partial S_1}{\partial U_1} \right)_{V_1,N_1} = \left(\frac{\partial S_2}{\partial U_2} \right)_{V_2,N_2} = \frac{1}{T_2}$$


### Chemical Potential of Classical Monoatomic Gas
$$ \frac{\mu}{T} = -\frac{\partial}{\partial N} \left[ kN (\frac{5}{2} + \ln \frac{V}{N}\left(\frac{4 \pi m E}{3N h^2}\right)^{3/2}\right]$$
- Evaluating the derivative and subbing in $E = \frac{3}{2} kT$ and $N/V = n$ (the number density) we have that: 
$$\mu = -kT \ln \frac{1}{n} \left(\frac{2\pi mkT}{h^2}\right)^{3/2}$$
- Increasing $n$ the number density, the log term decreases, however, the negative log term increases. 


### Recap: 
- In stat mech, so far we hace been defining our system by $E, V,N$ and we found that the entropy, $S(E,V,N)$ aims to maximize itself given its constratins. We were able to define the following partial derivatives, to define, temperature, pressure and volume 
    - $$\frac{1}{T} = \left( \frac{\partial S}{\partial E} \right)_{V,N}$$
    - $$\frac{P}{T} = \left( \frac{\partial S}{\partial V} \right)_{E,N}$$
    - $$\frac{\mu}{T} = \left( \frac{\partial S}{\partial N} \right)_{E,V}$$



### Consideration of the Taylor Expansion for Entropy 
- Consider coordinates $E, V, N$, then we can write our change in entropy as 
$$dS = \left( \frac{\partial S}{\partial E} \right)_{V,N} dE + \left( \frac{\partial S}{\partial V} \right)_{E,N} dV + \left( \frac{\partial S}{\partial N} \right)_{E,V} dN$$
- Now we apply our thermodynamic identities: 
$$dS = \frac{dE}{T} - \frac{P dV}{T} + \frac{\mu dN}{T}$$

#### Inversion
- We are nt limited to an expression of the differential of entropy. Consider rearranging and solving for $U$: 
$$S = S(U,V,N) \rightarrow U = U(S,V,N)$$
- We may also compute the differential of $U$ as: 
$$dU = \left( \frac{\partial U}{\partial S} \right)_{V,N} dS + \left( \frac{\partial U}{\partial V} \right)_{S,N} dV + \left( \frac{\partial U}{\partial N} \right)_{S,V} dN$$

### Determining the Maxima of Multivariate Functions 
- When the derivative is zero, we can have an inflection point, maxima or minima 
- Suppose we have some $\frac{\partial f}{\partial x_i} = 0$, to find the if the function is a maxima, we can use the use the second derivative test:
    - If the eigenvalues of $$\frac{\partial^2 f}{\partial x_i \partial x_j}$$ are all negative, then we have a maxima.


## Lecture 15 
### Boltzmann Statistics 
*We call $e^{-\beta E}$ the Boltzmann factor, what does it mean?*

#### Microcanonical Distribution 
- So far we've been studying the "microcanonical distribution", which states that all microstates are equally likely. $$P(E) = \frac{1}{\Omega(E)}$$
- The hard part, however, was finding the multiplicity function 

#### Canonical Distribution
- The probability distribution for a system in thermal doncatc with a reservoir. If the system has energy $E$, and some reservoir has energy $U_r$ then the total energy is fixed at $E + U_r$. 
- We wish to find therpboability that the system is in microstate $s$ with some energy $E_s$

$$P (\text{system is in a microstate S w/ energy } E_s)$$
equals the probability that the system has enery $E_s$ and the reservoir has energy $U_r - E_s$:

$$ P(E_s) \propto \Omega_R (U_r - E_s)  
\rightarrow \frac{P(E_s)}{P(E_s')} = \frac{\Omega_R(U_r - E_s)}{\Omega_R(U_r - E_s')} $$
- Recall from the definition of entropy, $\Omega = e^{S/k}$: 
$$ \frac{P(E_s)}{P(E_s')} = e^{\frac{1}{k}(S_r (U_r - E_s) - S_r(U_r - E_s'))}$$
- Rewriting this as a ratio: 
$$ \frac{P(E_s)}{e^{-\frac{E_s}{kT}}} = \frac{P(E_s')}{e^{-\frac{E_s'}{kT}}} = \frac{1}{Z(T,V,N)}$$ 

- Where $Z(T,V,N)$ is the partition function 


### Partition Function
- We can rewrite Boltmann distribution as: 
$$ P(E_s) = \frac{1}{Z} e^{-\frac{E_s}{kT}} = \frac{1}{Z} e^{-\beta E_s}$$

- If we take the sum over all microstates, they add up to 1: 
$$ \sum_{s} P(E_s) = 1 \rightarrow \sum_{s} e^{-\frac{E_s}{kT}} = Z$$
- We could also express $Z$ as: 
$$ Z = \sum_{E} N(E) e^{-\frac{E}{kT}}$$

- Thus, $Z$ is a normalization factor for $P(E_s)$
- $P(E_s)$ is the probability that the system is in microstate $s$ with energy $E_s$, thus the probability of finding a system with some energy $E$ is equal to the probability of finding the macrostate in that microstate $P(E_s =E)$ times the number of microstates with that energy, $N(E)$:
$$ P(\text{System has Energy E}) = \Omega(E) P(E) = \frac{1}{Z} e^{-\frac{E}{kT}} e^{\frac{S(E)}{k}} = \frac{1}{Z} e^{- (\frac{E-TS(E)}{kT})} = \frac{1}{Z} e^{-\frac{F}{kT}} = \frac{1}{Z}e^{-\beta F}$$

- We call $F = E - TS$ the Helmholtz Free Energy, and $\beta = \frac{1}{kT}$

#### Helmholtz Free Energy
- The value of $E$ which which is most likely to be observed is the one that minimizes $F$
    - Consider $T \rightarrow 0$, then $F \approx E$, and the system will want to minimize its energy and become "ordered"

    - Consider $T \rightarrow \infty$, then $F = E - TS$, and the system will want to maximize its entropy and become "disordered"
    


## Lecture 16
### Microcanonical vs Canonical 
- **Microcanonical** has a mulitplicity function, from there we find entropy, which wants to maximize, thus, determining the equilibrium state of the system. 
$$ dS = \frac{1}{T} dE + \frac{P}{T} dV - \frac{\mu}{T} dN = \left( \frac{\partial S}{\partial E} \right)_{V,N} dE + \left( \frac{\partial S}{\partial V} \right)_{E,N} dV + \left( \frac{\partial S}{\partial N} \right)_{E,V} dN$$

- **Canonical** is the probability distribution for a system in thermal contact with a reservoir. We define some partition function $Z(T,V,N)$. We introduce free energy $F(T, V,N) = -kT \ln Z(T,V,N)$, which leads to $$dF(T,V,N) = -S dT - P dV + \mu dN = \left( \frac{\partial F}{\partial T} \right)_{V,N} dT + \left( \frac{\partial F}{\partial V} \right)_{T,N} dV + \left( \frac{\partial F}{\partial N} \right)_{T,V} dN$$
- *You should be faimilar with the partial derivative transformations*

## Free Energy
$$F = E - TS \implies dF = dE - dT S - TdS$$ 
- From the microcanonical distribution: $dS = \frac{1}{T} dE + \frac{P}{T} dV - \frac{\mu}{T} dN$. Plugging this into the above equation we get  $dF = -S dT - P dV + \mu dN$. 

- For a process at fixed $T$ and $N$ we know that $\left(\Delta F \right)_{T,N}= \Delta E - T \Delta S = \Delta Q + \Delta W - \Delta Q = \Delta W$ (work on the system). So it is the maximum free work that can be extracted from the system. 


### $N$ Einstein Solids SHOs-Property of Exponentials
- Microstates are defined as $\{n_1, n_2, n_3, ... n_N\}$, where $n_i$ is the number of quanta in the $i$th oscillator. 
- The macrostate is the total energy of the system $E = \sum_{i=1}^{N} n_i \hbar \omega$.
- Now, we can define our partition function: each oscillator has its own partition sum, as we are summing over all microstates. 
$$ Z = \sum_{q_1}^{\infty} \sum_{q_1}^{\infty} ... \sum_{q_N}^{\infty} e^{-\beta \sum_{i=1}^{N} q_i \hbar \omega} = \left( \sum_{q_1 = 0}^{\infty} e^{-\beta \hbar \omega q_1} \right) \left( \sum_{q_2 = 0}^{\infty} e^{-\beta \hbar \omega q_2 } \right) ... \left( \sum_{q_N = 0}^{\infty} e^{-\beta \hbar \omega q_N } \right) $$

- We have an n fold sum, and each exponential can be moved to its corresponding sum, so 
$$ Z= \left( Z_{sho}\right)^N = \left( \sum_{q} e^{-\beta \hbar \omega} \right)^N = \left(\frac{1}{1- e^{-\beta \hbar \omega}}\right)^N$$


#### Application to the Microcanonical Distribution: 
- The probability of some microstate $s$ is given by:
$$ P_s = \frac{1}{Z} e^{-\beta E_s} $$
- The average energy of the system is given by: 
$$ \langle E \rangle = \sum_{s} E_s P_s = \frac{1}{Z} \sum_{s} E_s e^{-\beta E_s} = \frac{1}{Z} \sum - \frac{\partial}{\partial \beta} e^{-\beta E_s} =-\frac{1}{Z} \frac{\partial Z}{\partial \beta} = - \frac{\partial \ln Z}{\partial \beta}$$



- Thus we have that the average energy of the system is given by:
$$ \langle E\rangle = - \frac{\partial \ln Z}{\partial \beta} = - \frac{\partial}{\partial \beta} \left( N \ln \left( \frac{1}{1 - e^{-\beta \hbar \omega}} \right) \right) = N \frac{\hbar \omega e^{-\beta \hbar \omega}}{1 - e^{-\beta \hbar \omega}} = N \frac{\hbar \omega}{e^{\beta \hbar \omega} - 1} \implies \frac{\langle E \rangle}{N} = \frac{\hbar \omega}{e^{\beta \hbar \omega} - 1}$$

- At low temperatures: $\frac{\hbar \omega}{kT} \gg 1$, so $\frac{\langle E \rangle}{N} = \hbar \omega e^{-\frac{\hbar \omega}{kT}}$
- At high temperatures: $e^{\frac{\hbar \omega}{kT}} \approx 1 + \frac{\hbar \omega}{kT}$, so $\frac{\langle E \rangle}{N} = kT$



## Lecture 17 
### Recap on Boltzmann Statistics
$$P(\text{microstate s}) = \frac{1}{Z} e^{-\beta E_s}, \ \beta = \frac{1}{kT}$$
$$\langle E \rangle = \frac{1}{Z} \sum_s E_s e^{-\beta E_s} =  - \frac{\partial}{\partial \beta} \ln Z$$
$$\langle E^2  \rangle = \frac{1}{Z} \sum_s E_s^2 e^{-\beta E_s} =  - \frac{\partial^2}{\partial \beta^2} \langle E \rangle$$ 
- We argued that the free energy $F = E - TS(E)$ is the thermodynamic potential 


### N SHOs
- The parition function for $N$ SHOs: 
$$Z = \left( \frac{1}{1-e^{-\beta \hbar \omega}} \right)^N$$

- We found that the average energy per oscillator is given by:
$$\frac{\langle E \rangle}{N} = \frac{\hbar \omega e^{-\beta \hbar \omega}}{1-e^{-\beta \hbar \omega}}$$ 
- From here we found two limits. 
1) when $kT \gg \hbar \omega \rightarrow \frac{\langle E \rangle}{N} =kT$
2) When $kT \ll \hbar \omega \rightarrow \frac{\langle E \rangle}{N} =  \hbar \omega e^{-\beta \hbar \omega}$


- From statistics, we can pply the definition of the standard deviation: 
$$\sigma^2 = \frac{\sqrt{\langle E^2 \rangle - \langle E \rangle^2}}{\langle E \rangle } = ...  \sim \frac{1}{\sqrt{N}}$$
- In the TD limit, $\langle E \rangle = E$, since $N \rightarrow \infty$, and the fluctuations (i.e. $\sigma^2$) vanish.

### Free Energy and the Einstein Solid
- When $q/N \gg 1$, we found that the multiplicity function was $\Omega \approx \left( \frac{qe}{N} \right)^N$. The free energy is defined as: 

$$ F = - kT \ln Z = ... = - kTN \ln \left( \frac{kT}{\hbar \omega} \right)$$

$$ S(T,V,N) = - \left( \frac{\partial F}{\partial T} \right)_{V,N} = kN \ln \frac{kT}{\hbar \omega} + kN = k \ln \left( \frac{kT}{\hbar \omega} \right)^N = ... \rightarrow S = k \ln \Omega$$


### Back to the partition function 
$$z = \sum_s e^{-\frac{E_s}{kT}}  = e^{-\frac{E_0}{kT}} + e^{-\frac{E_1}{kT}} + e^{-\frac{E_2}{kT}} + ...$$
- We also know that $E_0 < E_1 < E_2 < ...$, so we could rewrite the partition function as: 
$$z = e^{-\frac{E_0}{kT}} \left( 1 + e^{-\frac{E_{1} - E_{0}}{kT}} + e^{-\frac{E_2 - E_0}{kT}} + ... \right)$$
- The exponential expansion tells us that microstates with $E_j - E_0 \gg kT$$ are exponentially frozen out or suppressed. 
- Microstates with $E_j - E_0 \ll kT$ contribution are significant 
- *So we it is called a partitoin function because it partitions the energy levels into microstates that are important at a given $kT$*

    - When $T \rightarrow 0 $ we have 
    $Z \simeq e^{-\frac{E_0}{kT}} (\text{number of ground states})$
    - When $T \rightarrow \infty$ we have $Z \simeq \text{total number of microstates}$ 

 **Electronic state:**
- $E_{el} - E_{0} \sim 1 eV \simeq k_B 10^4 K$
- For electronic excitations, the factor is $\frac{E_{el} - E_0}{kT} \sim 10^2$, meaning that they are exponentially expressed $e^{-10^2}$ 
- We do not care about electronic states

**Nuclear state:** 
- $E_{nuc} - E_0 \sim GeV$
- So for nuclear excitation, the factor is $e^{-10^{11}}$ 
- We care even less about nuclear states

- Thus, at room temperature, we only consider translational, rotational and vibrational states. Nucealr and electronic states are frozen out.
## Lecture 18

## Lecture 19

### Maxwell Speed Distribution 
**Simple derivation:** 
- Let's take 1 particle of interest and call it some system $S$ 
- For the rest of the particles $N-1$, we call it the reservoir $R$ 

For our particle we ask that $v \in (v, v + dv) = p(v) dv$ 
As probability density function we need that $\int_{0}^{\infty} p(v) dv = 1$ 

So $p(v) dv = e^{-\frac{mv^2}{2kT}} \times (\text{\# of microstates with } v \in (v, v+dv))$

**In the 2 dimensional case**
- We plot $v_x$ and $v_y$, so we take some $dv$ which is an annulus. The area of the annulus is thus $2\pi v dv$ which is proportional to the number of microstates. 

$$p(v)dv = e^{-\frac{mv^2}{2kT}} \times 2\pi v dv C$$ 
- Where $C$ is the normalization constant. As $v \rightarrow 0$, $p(v) \rightarrow v$ As $v \rightarrow \infty$, $p(v) \rightarrow v e^{-\frac{mv^2}{2kT}}$
- So linear and then exponential decay.

**In the 3 dimensional case**
- The surface where the speed is constant (i.e. $v_x^2 + v_y^2 + v_z^2 = v^2$) is a sphere. Then we draw another sphere with raadius $v + dv$, and we wish to find the volume of the spherical shell, which is $4\pi v^2 dv$.

$$p(v)dv = e^{-\frac{mv^2}{2kT}} \times 4\pi v^2 dv C$$ 
- Where $C = \left( \frac{m}{2\pi kT} \right)^{3/2}$, and is found by computing the Gaussian Integral. 

- As $v \rightarrow 0$, $p(v) \rightarrow v^2$ As $v \rightarrow \infty$, $p(v) \rightarrow v^2 e^{-\frac{mv^2}{2kT}}$
- In 3D, the distribution is quadratic and then exponential decay. We can determine the most probable speed $V_{max}$ by taking the derivative of $p(v)$ and setting it to zero.
$$\frac{dp(v)}{dv} = 0 \rightarrow v_{max}= \sqrt{\frac{2kT}{m}}$$ 

- We can also compute the expected value of $v^2$:
$$\left< v^2 \right> = \int_{0}^{\infty} v^2 p(v) dv = \frac{3kT}{m}$$

- We also can get the root mean square speed: $$v_{rms} = \sqrt{\left< v^2 \right>} = \sqrt{\frac{3kT}{m}}$$

- The kinetic energy is given by:
$$\left< KE \right> = \frac{1}{2} m \left< v^2 \right> = \frac{3}{2} kT$$

