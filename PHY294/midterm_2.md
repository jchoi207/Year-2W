# Lecture 1: Monday February 26

## Introduction

-   Particles exhibit *universal* behaviour regardless of composition.
    When the number of particles $N$ becomes large (in the thermodynamic
    limit $\sim 10^{23}$, the velocity follows the Maxwell-Boltzmann
    distribution: $n(v) \propto v^2 e^{-mv^2/2kT}$

-   Historically, it was difficult to quantify the number of particles
    within everyday samples. Allegedly, around 1773, Ben Franklin
    estimated the number of molecules within a teaspoon of olive oil to
    be in the order of $10^{21}$. This is an example of a macroscopic
    quantity.

-   **Microscopic:** If we wanted to describe a gas by studying its
    behaviour microscopically, we would account for the positions and
    velocities of each $N$ particle.
    $$m \ddot{\vec{r_i}} = \vec{F_{i}}(\vec{r_1}, ... , \vec{r_N}, \dot{\vec{r_1}}, ... , \dot{\vec{r_N}})$$

    -   This represents $3\times 10^{23}$ 2nd-order coupled differential
        equations. Not possible due to the limits of computation. Thus,
        the microscopic description is the most rigorous but useless in
        practical systems.

-   **Macroscopic:** consider how we could describe a system by
    considering it as a whole. We care about thermodynamic quantities:
    Entropy $S$, Temperature $T$, Pressure $P$, Number of particles $N$
    and Volume $V$. These quantities are much easier to measure.

-   Ideal Gas (model system): experiments show that a given volume $V$
    with $N$ particles eventually comes to a state known as TD
    equilibrium, where

    -   The number density of the particles is uniform, and the pressure
        $P$ and temperature $T$ are uniform and constant in time, so
        **no macroscopic fluxes exist**.

-   Energy transitions:

    -   Thermal Conductivity: Placing two objects at different
        temperatures in contact

    -   Convection: Exchange of heat between different states

    -   Radiation: Exchange of photons between hot and cold objects

# Lecture 2: Wednesday February 28

## Ideal Classical Gas

-   Ideal classical gasses have many particles and can be treated as
    point-like spheres. $$PV = NkT$$

-   The Ideal Gas Law is an example of **universal behaviour**: any gas
    sufficiently hot and dilute will obey it.

## Deriving the Ideal Gas Law

-   We attempt to calculate the macroscopic pressure gas molecules exert
    in a rectangular tank. To do so, we make assumptions about their
    velocities, then we find their momentum and thus the force they
    exert on the tank (which is pressure)

-   Assumptions:

    1.  $N \approx 10^{23}$

    2.  Gases will bounce elastically with each other and the container

    3.  The density is uniform (in any volume, the molecular density
        remains the same)

    4.  Velocities are isotropically distributed (as many molecules move
        in one direction as any other)

    5.  There is some average speed that the molecules exhibit

-   It is important to note that
    $\overline{v}_x = \frac{1}{N} \sum v_{xi} = 0$ by isotropy, there
    are as many molecules with negative velocities in the x direction as
    there are moving in the positive direction. This is the same with
    any direction $\bar{v}_y$ and $\bar{v}_z$ equal zero. This is why we
    define $\bar{v_x}^2 = \sum v^2_{xi}$ as the average speed (just
    considering the x direction)

-   We may consider the average speed in all 3 directions
    $$\overline{\vec{v^2}} = \frac{1}{N} \sum ||\vec{v}||^2 = \frac{1}{N} \sum v^2_{xi}+ v^2_{yi}+ v^2_{zi} = 3 \bar{v}^2$$

-   From our derivation (not done here), we have that
    $kT = m\bar{v}^2 = \frac{1}{3}m\bar{\vec{v}^2}$, using the above
    velocity expression. Therefore

    $$KE = \frac{1}{2} m\overline{\vec{v}^2} = \frac{3}{2}kT$$

-   We also define the root mean squared velocity:
    $$v_{rms}={\overline{\vec{v}^2}} = \sqrt{\frac{3kT}{m}}$$

-   Note: the average kinetic energy of an ideal gas is $\frac{3}{2}kT$
    and is only dependent on temperature. However, the $v_{rms}$,
    depends on the **molecular mass** of the gas. So, lighter gasses at
    the same temperature will, on average, travel faster than heavier
    ones.

\

# Lecture 3: Friday March 1

## Classical Equipartition Theorem

-   Temperature as a measure of average kinetic energy is an example of
    the classical equipartition theorem.

-   At thermodynamic equilibrium, the energy of the system will tend to
    spread out evenly to its thermally active degrees of freedom. The
    average energy per degree of freedom of a molecule is

    -   Translational: $\frac{1}{2}kT$

    -   Rotational: $\frac{1}{2}kT$

    -   Vibrational: $kT$

-   We can determine a gas's average internal energy from its
    temperature and composition. This allows us to calculate its heat
    capacity.

1.  Monoatomic (e.g. Ne): the monoatomic gas can translate in all three
    directions. It can technically rotate, but in doing so, it does not
    change the spatial density (i.e. mass is not moving). It cannot
    vibrate. So, with $n =3$ degrees of freedom, it has internal energy
    $U = 3 \frac{1}{2}NkT$, with specific heat capacity equal to
    $C_v = \frac{3}{2}Nk$. (note we can also find the specific heat
    capacity per molecule by differentiating $C_v$ w.r.t $N$)

2.  Diatomic (e.g. $O_2$): the diatomic gas can translate in three
    directions, and it can technically rotate along all three axes, but
    one of them (roll) does not lead to a change in mass density, so
    $2$. There is one vibrational mode **; however, this mode might not
    necessarily be thermally active if temperatures are too low**. Thus
    a diatomic has internal energy
    $U = (3 + 2 + 1 \times 2) \frac{1}{2} NkT = \frac{7}{2} NkT$ with
    specific heat capacity $C_v = \frac{7}{2}Nk$.

    -   Note, we multiply the $1$ dof from the vibrational mode by 2,
        because with each vibration, there are two energies associated:
        kinetic (movement) and potential (attraction + repulsion). Each
        vibration is a harmonic oscillator.

    -   Note that this is only valid given that the gas's temperature is
        high enough $kT \gg \hbar \omega$. At lower temperatures, the
        vibrational modes are \"frozen out\", meaning that they don't
        have enough energy to occur.

3.  For linear molecules: $3$ translational, $2$ rotational (for the
    same reason as diatomics) and $3N-5$ vibrational degrees of freedom.
    The energy per molecule is $\frac{kT}{2}(6n-5)$

4.  For non-linear molecules: $3$ translational, $3$ rotational (any
    rotation leads to change in density) and $3N-6$ vibrational degrees
    of freedom. The energy per molecule is $kT(3n-3)$

5.  For solids in a lattice, atoms cannot translate or rotate; however,
    they may vibrate in all 3 directions, so $f=6$ since each
    vibrational mode has kinetic and potential.

## Heat Capacity

-   Heat capacity is not constant with increasing $T$ until
    $1000 \ \text{K}$. Below this temperature, the heat capacity
    increases in discrete steps. At lower temperatures, movements are
    only translational; however, at higher temperatures, the rotational
    and then vibrational modes become thermally active. Quantum
    mechanics only allows molecules to vibrate and rotate if they
    possess some minimum energy.

 

# Lecture 4: Monday March 4

## Heat Transfer and the First Law of Thermodynamics

-   Consider how we might change the energy of a thermodynamic system.
    Place an object in contact with a thermal reservoir at a different
    temperature. The initial internal energy will be different from the
    final, since the final temperature $T_f$ changes:
    $U_{i} = \frac{3}{2}NkT_i$ and
    $U_f = \frac{3}{2}NkT_f \rightarrow \Delta U = \frac{3}{2}Nk(T_f - T_i)$.
    We attribute this heat transfer from the hotter system to colder as
    $Q = \Delta U$

-   Consider a piston compressing a gas. When the wall moves in, the
    molecules that collide with the piston speed up, increasing $U$ and
    $T$. When the piston expands, the molecules slow down and both $U$
    and $T$ decrease. The work done on the system by pushing the piston,
    or the work done by the gas on the surroundings by expanding the
    piston changes the internal energy of the gas $W = \Delta U$

-   As such, the change in internal energy is equal to the sum of the
    heat absorbed $Q$ and work done on the system $W$. This is also
    known as the first law of TD: $$\Delta U = Q + W$$

-   An alternate form is $dU = \delta Q - pdV$ . Note the negative term
    is because a compression $dV < 0$ represents work done on the
    system, and expansion $dV > 0$, is work done on the surroundings, so
    work is negative.

## Quasistatic Processes

-   A quasistatic process is one where the system is in TD equilibrium
    at any instant. There is uniform density and pressure and
    temperature are constant. *The process proceeds slow enough s.t. the
    system equilibrates at every step*

-   We may compute the work done on/by the gas in infinitesimal steps.
    Consider an initial pressure $P_1$ with a compression in volume i.e.
    $\Delta V_1 < 0$. The work on the gas in this infinitesimal step is
    $-P_1 \Delta V_1$. Now, we wait for the pressure to equilibrate, and
    repeat:
    $W = -p_1 \Delta V_1 - p_2 \Delta V_2 - ... - p_n \Delta V_n$, as
    $n \rightarrow \infty$, we integrate
    $W_{\text{on the gas}} = - \int_{V_i}^{V_{f}} \ p \ dV$

-   However, we don't know the conditions at which the process occurs,
    so the pressure is a function of $V$ and $T$
    $$W_{\text{on the gas}} = - \int_{V_i}^{V_{f}} \ p(V,T) \ dV$$

-   For an ideal gas, $p = \frac{1}{V}NkT$. Now we can consider the
    characteristics of various processes:

### Isothermal $T = C$

-   Consider the expansion or compression at constant temperature. This
    could be achieved by placing the reaction vessel in a water bath.
    The work done in an isothermal process is
    $$W = - NkT \int \frac{dV}{V} = - NkT \ln (\frac{V_f}{V_i})$$

-   *Since the temperature is fixed, $U$ must remain constant before and
    after the process. As a result, a compression, compression ($W>0$)
    requires heat to flow out of the system. Conversely, expansion
    $W < 0$, requires heat absorption from the reservoir.*
    $\Delta U = 0 = W + Q \rightarrow W = - Q$.

-   Moreover, $pV = C$

### Adiabatic $Q =0$

-   An adiabatic process is one that is isolated where heat losses or
    gains are not possible. Adiabatic processes can be both quasistatic
    and non-quasistatic. In the case of a non-quasistatic adiabate,
    consider an isolated gas partitioned, into volumes, one with
    particles, one without. By removing the barrier rapidly, there is no
    work done.

-   In a quasistatic process:

    -   $pV = NkT$ by the ideal gas law, $U= \frac{f}{2}NkT$ by the
        equipartition theorem, and $dU = -pdV$ by the first law of TD.
        By rearranging and plugging things in, we get that
        $(\frac{V_1}{V_2})^{\frac{2+f}{f}} = \frac{p_2}{p_1}$, this
        implies that $V_2 ^{\frac{2+f}{f}} p_2$ is a constant.

    -   $\frac{2+f}{f} = \gamma >1$ since $f$ is the degrees of freedom,
        meaning that the volume and pressure are inversely proportional.
        **The adiabatic P-V curve falls steeper than the isotherm.**

    -   $pV^{1 + 2/f} = c$

# Lecture 5: Wednesday March 6

## Heat Capacity

\
The heat needed to increase the temperature of a substance by $1$ K.

### Constant Pressure

-   Heating at a constant volume means that no work can be done, so
    $dU = \delta Q$. Applying the equipartition theorem, the internal
    energy is $U = \frac{f}{2}NkT$, thus, we can find the heat capacity
    by differentiating w.r.t T.
    $$C_v = \left( \frac{\delta Q}{\Delta V}\right)_{V} =  \left( \frac{\partial Q}{\partial V}\right)_{V}$$

-   The constant volume specific heat capacity is $C_v = \frac{f}{2} kN$

### Constant Volume

-   Heating a gas up at constant pressure leads to
    $Q = \Delta U + p\Delta V$, through algebra, we get that
    $C_p = \frac{f+2}{f} Nk = \gamma C_v$, where gamma is the adiabate
    constant. As such $C_p > C_v$.

# Lecture 6: Thursday March 7

## Discrepancy in Heat Capacity

-   Consider a hydrogen molecule with interatomic distance of
    $0.7 \times 10^{-10} \text{ m}$ and mass of
    $1 \times 10^{-27} \text{ kg}$. Classically, angular momentum is
    $L = I \dot{\phi}$, and the rotational energy is
    $\frac{1}{2} I \dot{\phi}^2 = \frac{L^2}{2I}$.

-   Recall that the angular momentum is quantized, so we can consider
    $L=0$ as no rotation, and $L \geq n\hbar$ as rotation. Therefore,
    the minimum energy of rotation is $E \approx \frac{1\hbar^2}{I}$,
    calculating $I \approx mr^2 = 1\times 10^{-48} \text{ kg m}^2$,
    meaning that the minimum energy to observe rotation is on the order
    of $1\times 10^{-20} J$. Comparing this to $E \approx kT$ , the
    minimum temperature is $T= 1000 \text{K}$. Thus a temperature of
    1000 kelvin is needed to excite rotations.

## Introduction To Statistical Mechanics

-   In an isolated gas of many particles, there are many ways that the
    energy $E$ can be distributed among the particles. Each of the ways
    in which the energy can be distributed is called a **microstate**,
    whereas the total energy is the **macrostate**

-   The fundamental postulate of statistical mechanics states that *all
    accessible microstates are equally likely*.

    -   Accessible microstates are those that have total energy that
        matches a given macrostate

    -   The multiplicity function is the number of microstates
        accessible to a given macrostate. The multiplicity function
        $\Omega$ lets you describe the system.

-   We can no longer describe the system classically with trajectories.
    Thus, we use probabilistic distributions, and with $N$ large,
    probabilities become certainties as probability distributions become
    sharper ($\delta$ functions)

## Electronic Paramagnet

-   The macrostate of a paramagnet is the macroscopic quantity of
    magnetic moment.

-   We can model the material as a lattice. Each of the $N$ atoms has
    two degrees of freedom, spin up and spin down: $s_i = \{ +1, -1\}$
    for $i = 1 , ..., N$. It is easy to recognize that there are
    $2^N$possible microstates (each of the $N$ atoms has 2 independent
    possibilities because we ignore spin-spin and spin-atom
    interactions).

-   The energy of a single spin in a magnetic field $\mathbf{B}$ is
    $U_i = -\mu_o \mathbf{B} s_i$, thus the total energy of the system
    is $U = - \mu_o \mathbf{B} \sum_{i=1}^{N} s_i = -\mu \mathbf{B} S$.
    where $S$ is the total spin, which is the sum of the individual
    spins.

-   Take the energy of a single spin in a $\vec{B}$ field to be
    $U_i = -\mu_o B s_i$ note that $\mu_i = \mu_o s_i$

    $$U = - \mu_o B \sum_{i=1}^{N}s_i = - \mu _o B S'$$

# Lecture 7: Monday March 11

## Fundamental Postulate of Statistical Mechanics

-   In an isolated gas of many particles, we can describe each
    individual state's energy as a microstate. The total energy is
    considered a macrostate.

-   The fundamental postulate states **all microstates are equally
    likely.** A microstate is said to be accessible if its total energy
    matches a given macrostate.

```{=html}
<!-- -->
```
-   For a closed system $U$ fixed, in TD equilibrium all microstates are
    equally likely.

## Electronic Paramagnetic

-   Recall the spin system with $N$ possible spins with $s_i = \pm 1$

    -   Microstates = $\{s_1, ..., s_N\}$. Thus, there are $2^N$
        possible microstates since each $N$ electron has two options

    -   Macrostate or the total energy is defined by
        $U = i\mu_o B \sum_{i=1}^{N} s_i = -\mu_o BS$ , where $S$ is the
        **total spin**. Note that $S$ is determined by the sum of all
        microstates. Moreover, $S$ is determined by $N_{up}$ since
        $N = N_{up} +N_{down}$ and $S = N_{up} - N_{down}$, which
        implies that $S = 2N_{up} - N$. So $S$ can be fully expressed
        i.t.o $N_{up}$ .

    -   We also see that there are $N+1$ possible values of $N_{up}$,
        thus $S$ has $N+1$ macrostates.

-   Macrostates are fixed by $S$. We say that a microstate is accessible
    from the macrostate w/ given $S$ on $N_{up}$ if it has the same
    $N_{up}$

-   The multiplicity of the general macrostate is the number of
    accessible microstates given $N_{up}$ is
    $$\Omega(N, N_{up}) = \frac{N!}{N_{up}! (N-N_{up})!}$$

## Einstein Solid

-   Collection of $N$ simple harmonic oscillators that function
    independently of each other.

-   The i-th oscillator has energy $\hbar \omega (q_i+ \frac{1}{2})$
    where $q_i = 0,1,2, ..., N$ . We ignore the constant of 1/2
    (zero-point energy)

    -   Microstates $= \{q_1 , ... , q_N \}$ so the number of
        microstates is countably infinite as we take $N$ on the order of
        Avogadro's number.

    -   Macrostates = $U = \sum_{i=1}^{N}q_i = \hbar w q$. Where
        $q = \sum q_i$

-   To find the multiplicity function of the macrostate, we can assume
    that $N−1$ partitions and $q$ units of energy or objects represent
    our system. These objects can be partitioned or spread out across
    the system. $$\Omega(N, q) = \frac{(q+N-1)!)}{q! (N-1)!}$$

## Example: Energy Flow

-   Consider two systems $N_A$ with $q_A$ and $N_B$ with $q_B$ such that
    $q_A + q_B$ (the initial states) equals the final states (after the
    systems come into thermal equilibrium)
    $q_A + q_B = q_A' + q_B' = c$.

-   Thus, the multiplicity function of $A$ is $\Omega(N_A, q_A')$ and
    the multiplicity function of $B$ is $\Omega (N_B, q-q_A')$.
    Therefore, for the system of $A$ in contact with $B$, the
    probability of observing some $(q_A', q-q_A')$ is thus proportional
    to the product between the individual multiplicities
    $\Omega(N_A,q_A')$ and $\Omega(N_B, q-q_A')$.

-   Note, for each of the $\Omega_A$ microstates available to $A$, there
    are $\Omega_B$ microstates available for $B$, hence the product.

# Lecture 8: Wednesday March 13

## General Thermal Equilibrium - Statistical Definition of Temperature and Energy

-   Consider system 1 with energy $E_1$ and system 2 with energy $E_2$
    that are brought together and allowed to reach thermal equilibrium.

-   In TD equilibrium, the overall system has energy $E = E_1 + E_2$
    assuming the process is adiabatic. Thus, we have $E_1$ and
    $E_2 = E - E_1$

-   The probability of having a particular $E_1$ is $P(E_1)$ is
    $$P(\Delta) = \frac{\Omega_1(E_1) \Omega_2(E - E_1)}{{\sum^{E/2}_{\bar{\Delta} = -E/2}} \Omega_1(E_1) \Omega_2(E - E_1)}$$

-   We aim to find the $E_1$ for the maximum probability of $P(E_1)$.
    Thus we differentiate the numerator with respect to $E_1$
    $$\frac{\partial }{\partial \Delta} \Omega_1(E_1) \Omega_2(E-E_1) = 0$$

-   Differentiation eventually leads to
    $$\frac{\partial }{\partial E} k\ln \Omega_1 (E_1) = \frac{\partial }{\partial E} k\ln \Omega_2 (E_2) \implies \frac{1}{T_1} = \frac{1}{T_2}$$

-   Each term is a property of a single system, so when they are brought
    into contact and reach TD equilibrium, their properties, i.e.
    temperatures must be equal.

-   We define, entropy as $$S(E, N,V)   = k \ln \Omega (E,N,V)$$

-   The inverse temperature of a system is defined as
    $$\frac{1}{T(E,N,V)} = (\frac{\partial S}{\partial E})_{N,V}$$

-   **Some Important Notes:** A closed system evolves s.t. its entropy
    tends to a maximum value. Since each macrostate must have a
    multiplicity of at least 1 $\Omega \geq 1$, we must also have
    $S \geq 0$

    -   In the case of the electronic paramagnetic, the states
        $N_{up} = N$ only have one microstate, so $\Omega = 1$, $S =0$,
        thus this system is considered to be very ordered

    -   If the system is defined by the macrostate
        $N_{up} = \frac{N}{2}$ , then $S \gg 1$, so this system is
        disordered. In this case, *disordered*, refers to the higher
        number of microstates that are accessible.

    -   We can also see entropy as the inverse of how much information
        we have about a system. When $N_{up} = N$, we known exactly what
        microstate the system is in, but in the case of
        $N_{up} = \frac{N}{2}$, we have little information about the
        microstate the system is in.

    -   Finally notice that $T\geq 0$ because
        $\frac{\partial S}{\partial E} \geq 0$, so if you add energy
        into the system, there are more ways to distribute the energy,
        so entropy increases

    -   Multiplicity is multiplicable $\Omega_{1+2} = \Omega_1 \Omega_2$
        since the multiplicity functions are logarithms

    -   Entropy is additive $S_{1+2} = S_1 + S_2$

# Lecture 9: Thursday March 14

## On the Einstein Solid: consideration of the ratio $q/N$

-   In the TD limit where $N, V, E \rightarrow \infty$ (all extensive
    properties), and density and energy density is kept fixed, the
    results of statistical mechanics become certainties.

-   The E.S. was defined with $E = \hbar \omega q$ (zero point energy is
    ignored) with $\Omega = \frac{(N-1+q)!}{(N-1)!q!}$. Keeping $q/N$
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
    distribute among the two systems? $q_1 = q/2 + X$, $q_2 = q/2 - X$.
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
        fractional energy imbalance between 1 and 2 of $10^{-5}$ (which
        is already tiny!). Then
        $\frac{P(\frac{2x}{q} \sim 10^{-5})}{P(0)} = e^{-10^{23} 10^{-10}} \approx e^{-10^{13}}$.
        Thus, this essentially says that the probability that the energy
        imbalance is as small as $10^{-5}$ is essentially 0.

# Lecture 10: Monday March 18

## Thermodynamic Potential

-   Second Law of Thermodynamics: A closed system will evolve towards a
    TD equilibrium state that maximizes the entropy (subject to imposed
    constraints)

-   Given a closed system with energy $E$, particles $N$ and volume $V$,
    we define its entropy as $S(E, N,V) = k \ln \Omega (E, N,V)$. We
    think of $S$ as a **TD potential** which determines the approach of
    TD equilibrium. A similar analogy is how a potential $\mathbf{U}$
    defines equilibrium in classical systems
    $\mathbf{F} = - \nabla \mathbf{U}$.

-   $S$ wants to maximize, so the gradient of $S$ as a function of
    $E, N,V$ (TD coordinates) play a role in the force that drives a
    system to TD equilibrium.

## Thermodynamic Potential

-   Given a closed system with energy E, particles N and volume V:
    $S(E, N,V) = k \ln \Omega (E, N,V)$. We can think of $S$ as a **\"TD
    potential\"** which determines the approach of TD equilibrium. In
    the same way that $\mathbf{F} = - \nabla \mathbf{U}$ defines
    classical systems.

-   $S$ wants to maximize

-   The gradient of $S$ as a function of $E, N,V$ plays a role of a
    force that drives the system to TD equilibrium:
    $$\frac{1}{T} = \left(\frac{\partial S(E,N,V)}{\partial E}\right)_{N,V}$$

-   So we if we have $\frac{1}{T_1}> \frac{1}{T_2}$, then energy will
    flow until the two are equal

-   Note that $\frac{\partial S}{\partial V}$ and
    $\frac{\partial S}{\partial N}$ are the pressure and chemical
    potential and are also forced towards equilibrium

## General Properties of Entropy

-   From the ES for $\hbar \omega \ll kT$, then,
    $S \approx kN \ln \frac{Ee}{N\hbar w}$: meaning more energy, more
    microstates (linear term $N$ beats $\ln(1/N)$).

-   Properties to consider:

    -   The entropy $S$ curve as a function of $E$ is an increasing
        function, so as $E$ increases, so does $S$ for $T \geq 0$

    -   The second derivative of entropy w.r.t energy, so
        $\frac{\partial S}{\partial E}$ decreases, and so temperature
        increases.

    -   So energy transfer requires $C_v > 0$. All \"normal\" TD systems
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

# Lecture 11: Wednesday March 20

## Ideal Gas (Sackur-Tetrode Equation)

-   For a given internal energy of a monoatomic ideal gas $U$, how many
    microstates are there? Recall that the total energy $U$ is equal to
    the sum of all kinetic energies and thus momenta:
    $$U = \sum_{i=1}^{N}\frac{\vec{p_i}^2}{2m} \rightarrow \sum_{i=1}^N \vec{p_i}^2  = \sum_{i=1}^N p^2_{xi} + p^2_{yi} + p^2_{zi} = 2mU$$

-   Recall the particle in a box problem, the momentum can be expressed
    as the sum of the squares of the quantum numbers associated with
    each coordinate: $p_{xi}^2 = \frac{\pi \hbar}{L} n_x$.

-   Thus we take the sum of all the quantum numbers which is $3N$ since
    each particle can move in all three directions:
    $n_{1x}^2 + n_{1y}^2 + n_{1z}^2 + ... + n_{Nx}^2 + n_{Ny}^2 + n_{Nz}^2 = \frac{2mU}{\frac{\pi \hbar}{\omega}} = R^2$
    , which represents a sphere in $\mathbb{R}^{3N-1}$.

-   Thus, we define the multiplicity function
    $\Omega(N, U,V) = \text{microstates with energy} \in (U - \frac{\Delta}{2}, U + \frac{\Delta}{2})$.
    Geometrically this represents two spheres drawn in the
    $\mathbb{R}^{3N}$ coordinate plane that differ in radius by
    $\Delta$. $\Omega = A_{3N-1}(R)= \Delta$. Thus, for small enough
    $\Delta$, the multiplicity function is the area of the sphere times
    $\Delta$

-   Corrections:

    -   We must partition our space since we only take the positive
        values ($n_{kx,ky,kz} > 0)$. Thus, we divide by a factor of
        $2^n$ for each dimension $n$ (Intuition: circle in
        $\mathbb{R}^2$ gets divided by 4, the sphere in $\mathbb{R}^3$
        gets divided by 8)

    -   Gibbs factor: extensive property (if you double all the
        properties of a system, you would expect entropy to double as
        well, hence the need for $\frac{1}{N!}$)

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

# Lecture 12: Thursday March 21

## When is a Gas No Longer Ideal?

-   We always say that a gas has to be hot and dilute enough. What does
    \"enough\" mean? With the Sackur-Tetrode Formula, we can quantify
    these statements.
    $\frac{\partial S}{\partial U} = \frac{1}{T} \implies U = \frac{3}{2}kNT$

-   We introduce the de thermal Broglie wavelength
    $\lambda_{th} = \frac{h}{\sqrt{mKT}}$, which is the de Broglie
    wavelength but with $p = \sqrt{mkT}$; as such, a larger mass and
    temperature will decrease the thermal wavelength:
    $\lambda_{th} \propto \frac{1}{\sqrt{mT}}$.

-   Define the characteristic length between particles as
    $l = (\frac{V}{N})^{\frac{1}{3}}$. Thus, the ideal gas law holds
    when $l \gg \lambda_{th}$---where the typical distance between
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
    gas---low density and high temperatures. To summarize, a gas becomes
    quantum when
    $\frac{h}{mkT}=\lambda_{th} \approx l = (\frac{V}{N})^{1/3}$
