# ECE259 Midterm Notes
*by jchoi*

## Lecture 1 - Charge

## Lecture 2 - Coulomb's Law

$$ \mathbf{F} = \frac{1}{4 \pi \varepsilon_o} \frac{q_1 q_2}{(d_{12})^2} \mathbf{a_{d12}}$$
$$ \mathbf{F} = \frac{1}{4 \pi \varepsilon_o} \frac{q_1 q_2}{|\mathbf{R_2} - \mathbf{R_1}|^3} (\mathbf{R_2} - \mathbf{R_1})$$

- Where $\mathbf{R_1}$ and $\mathbf{R_2}$ are the position vectors of the charges $q_1$ and $q_2$ respectively.

## Lecture 3 - Electric Field

$$\mathbf{E} = \frac{\mathbf{F}}{q} = \frac{1}{4 \pi \varepsilon_o} \frac{q_1}{|\mathbf{R_2} - \mathbf{R_1}|^3} (\mathbf{R_2} - \mathbf{R_1})$$

- Still decays like $\frac{1}{d^2}$

## Lecture 4 - Coordinate systems

- Cartesian position vector: $\mathbf{R} = x_o \mathbf{a_x} + y_o \mathbf{a_y} + z_o \mathbf{a_z}$

- Cylindrical position vector: $\mathbf{R} = r_o \mathbf{a_r} + z_o \mathbf{a_z}$

- Spherical position vector: $\mathbf{R} = R_o \mathbf{a_R} $

## Lecture 5 - Superposition I

**Discrete Distributions**
$$ \mathbf{E} = \sum_{k=1}^{N} \frac{q_k}{4 \pi \varepsilon_o} \frac{(\mathbf{R} - \mathbf{R_k})}{|\mathbf{R} - \mathbf{R_k}|^3} $$

- Where $k$ are the various charges in space and $R_k$ are their respective position vectors. $\mathbf{R}$ is the position at which we are calculating the electric field.

**Continuous Distributions**
1. Volume: $\rho_v$ measured in $[C/m^3]$
2. Surface: $\rho_s$ measured in $[C/m^2]$
3. Line: $\rho_l$ measured in $[C/m]$ 

- In either case, the electric field is calculated by integrating over the volume, surface or line element: $$\int_{\Omega} d\mathbf{E}' = \int_{\Omega} \frac{\rho_{\Omega}' d \Omega}{4  \pi \varepsilon_o} \frac{(\mathbf{R} - \mathbf{R'})}{|\mathbf{R} - \mathbf{R'}|}$$

## Lecture 6 - Superposition II
Steps for finding $\mathbf{E}$: 

1. Choose coordinate system and make use of symmetry if applicable 
2. Find the differential charge $dq' = \rho_{\Omega} d \Omega$ 
3. Compute $\mathbf{R}$, $\mathbf{R'}$, $\mathbf{R} - \mathbf{R'}$ and $|\mathbf{R} - \mathbf{R'}|$, where $\mathbf{R}$ is the position of interest. 
4. Compute the integral 

## Lecture 7 and 8 — Gauss' Law
- For any closed surface, the total flux is equal to the total charge enclosed by the surface divided by $\varepsilon_o$. 
 $$\oint \mathbf{E} \cdot d\mathbf{S} = \frac{Q}{\varepsilon_o}$$ 

 - The integral represents the outwards flux of the electric field through the surface. Consider a point charge outside some closed surface $S$, the electric field lines entering the solid will have negative contribution, whereas those leaving will have positive contribution. 



**Gauss'Law and Computing Electric Field**

Valid for:
- Constant charge densities 
- Surface must be Gaussian and closed 
    - $\mathbf{E} \perp d\mathbf{S} \implies \mathbf{E} \cdot d\mathbf{S} = 0$
    - $\mathbf{E} \ \| \ d\mathbf{S} \implies \mathbf{E} \cdot d\mathbf{S} = |\mathbf{E}| |\mathbf{dS}|$ 


## Lecture 9 — Gauss' Law in Differential Form
$$ \oint_{S} \mathbf{E} \cdot d\mathbf{S} = \int_{V} \nabla \cdot \mathbf{E} \ dV = \frac{Q_{enc}}{\varepsilon_o}$$
$$ \int_V \nabla \cdot \mathbf{E} dV = \int_V \frac{\rho}{\varepsilon_o} \ dV \implies \nabla \cdot \mathbf{E} = \frac{\rho}{\varepsilon_o}$$ 

- For a positive point charge, $\rho_v > 0$, so the divergence of the electric field is positive, the converse is true for a negative point charge.

## Lecture 10 - Work in Electrostatics

$$ W = \int_{\gamma } \mathbf{F} \cdot d \mathbf{l} = - q \int_{\gamma} \mathbf{E} \cdot d \mathbf{l}$$

**Work done on a closed path**
- Due to the conservation of energy, $\mathbf{E}$ produced by a static distrribution of charge is conservative.

$$ \oint_{\gamma} \mathbf{E} \cdot d \mathbf{l} = 0 \impliedby \nabla \times \mathbf{E} = 0 $$   

**Scalar Potential V**
- Any conservative field can be written in terms of some scalar field $V$ that is defined by $$\mathbf{E}  = - \nabla V$$ 
- The motivation for this is that scalar fields are easier to work with than vector fields.

**Finding $V$ from $\mathbf{E}$**
- Since in electrostatics $\mathbf{E}$ is conservative, then we can apply the fundamental theorem of line integrals 
$$\frac{W}{q} = - \int_{p_1}^{p_2} \mathbf{E} \cdot d \mathbf{l} = V(p_1) - V(p_2)$$ 
- The voltage between points $p_1$ and $p_2$ is equal to the work required to move a unit charge from $p_1$ to $p_2$.
- If a charge is bounded, it is convention to set the potential at infinity to be zero: $V(\infty) = 0$

**Equipotential Lines** 
- Lines along which the potential is constant. These lines will always be perpendiculr to the electric field lines. $\mathbf{E} = - \nabla V $ 
points in the direction of steepest decrease of $V$, as such electric field lines are always perpendicular to equipotential lines. 



## Lecture 11 - More on Potential

- To find the potential produced by a charge distribution we use the difference in potential, taking the reference to be at infinity. 
$$ V(p_2) - V(p_1) = - \int_{p_1}^{p_2} \mathbf{E} \cdot d \mathbf{l} \rightarrow V(p_2) - V(\infty) = - \int_{\infty} ^{p_2} \mathbf{E} \cdot d \mathbf{l}$$ 
- We must note that the bounds of integration must always be increasing, so we take the negative: $$V(p_2) = \int_{p_2}^{\infty} \mathbf{E} \cdot d \mathbf{l}$$ 

## Lecture 12 - Superposition for Potential and Materials

**Potential due to a single charge**
- Applying the line integral formula, we can find the potential due to a single charge at some point $p_2 = R$: 
$$ V(p_2 = R) - V(p_1 = \infty) =  -\int_{R' = \infty}^{R' = R} \mathbf{E} \cdot d \mathbf{l}$$
- We know that the electric field is radial, so we can write the electric field as $E = \frac{q \mathbf{R'}}{4 \pi \varepsilon_o |\mathbf{R}|^3}$: 
$$ V(R) = \int_{R' = R}^{R'= \infty} \frac{q}{4 \pi \varepsilon_o |\mathbf{R'}|^3} R' \mathbf{a_R} \cdot \mathbf{a_R} d R = \frac{q}{4\pi \varepsilon R}$$  

- The above formula allows us to generalize:
$$dV = \frac{dq}{4\pi \varepsilon_o |\mathbf{R} - \mathbf{R'}|}$$
- Where $dq$ is found from the charge distribution: $dq = \rho_{\Omega} d \Omega'$, so the continous superposition formula for potential is:
$$V(\mathbf{R}) = \int_{v'} \frac{\rho_v dv'}{4\pi \varepsilon_o |\mathbf{R} - \mathbf{R'}|}$$

**Steps for finding V:**

1. Choose coordinate system and make use of symmetry if applicable 
2. Find the differential charge $dq' = \rho_{\Omega} d \Omega$ 
3. Compute $\mathbf{R}$, $\mathbf{R'}$, $\mathbf{R} - \mathbf{R'}$ and $|\mathbf{R} - \mathbf{R'}|$, where $\mathbf{R}$ is the position of interest. 
4. Compute the differential voltage element: $$dV = \frac{\rho_{\Omega} d \Omega}{4\pi \varepsilon_o |\mathbf{R} - \mathbf{R'}|}$$
5. Integrate







### Electrostatics in the Presence of Materials
- So far just been interested in point, line, surface and volume charges in free space. 

- **Conductors**
    - Charges are free to leave their atoms and move. 
    - Conductivity is very high, so we idealize and assume that they are a perfect conductor with $\sigma \rightarrow \infty$ 

- **Dielectrics**
    - Electrons are tightly bound to their atom
    - Conductivity is very low, so we idealize and assume that that $\sigma = 0$


**Applying a field to a conductor**
- When a field is applied to a conductor, the electrons will move towards the positive end of the field, similarly, the positive cations will move towards the negative end. There will be an accumulation of surface charges $\pm \rho_s$ on either side of the conductor, which will produce an electric field that is equal and opposite to the applied field. As such, there is no electric field within the material, $V$ must be held constant, and there is no longer any volume charge density
    - $\mathbf{E} = 0 $.
    - $\mathbf{E} = 0 = - \nabla V \implies V = \text{constant}$
    - $\rho_v = \varepsilon_o (\nabla \cdot \mathbf{E})= 0 $ 

    



## Lecture 13 - Boundary Conditions


### Boundary between free space and a perfect conductor
**Tangential Component of the Electric Field** 

- Since the electric field is conservative $\oint_c \mathbf{E} \cdot d \mathbf{l} = 0$ because the curl of the electric field is 0, i.e. $\nabla \times \mathbf{E} = 0$. So drawing a rectangle of width $\Delta w$ and height $\Delta h$, we are essentially computing a closed line integral which must amount to 0 
$$\int_{\Delta w} \mathbf{E} \cdot d \mathbf{l} + \int_{\Delta h} \mathbf{E} \cdot d \mathbf{l} + \int_{\Delta w} \mathbf{E} \cdot d \mathbf{l} + \int_{\Delta h} \mathbf{E} \cdot d \mathbf{l} = 0$$ 
- The first path integral is zero since the electric field within a perfect conductor is 0. The third path is taken as $E_t \Delta w$, where $E_t$ is the tangential component of the electric field. The second and fourth paths are taken as 0, as we take $\Delta h \rightarrow 0$. As such, we are left with $$E_t \Delta w + 0 + 0 + 0 = 0 \implies E_t = 0$$, 
- Thus, the tangential component of the electric field on the surface of a good conductor is 0. Intuitively, if $E_t \neq 0$, charges woulld move along the surface until $E_t = 0$.

**Normal Component of the Electric Field** 

- Take a cylinder with surface $\Delta S$ and height $\Delta h$, we can make use of Gauss' Law in integral form to compute the flux through the cylinder, and thus the normal component of the electric field: 
- We break down the cylinder into its top, side and bottom surface, and we know that the charge enclosed by the cylinder is equal to the surface charge density times the area $\rho_s \Delta s = q_{enc}$  
$$ \int_{S_{top}} \mathbf{E} \cdot d \mathbf{S} + \int_{S_{side}} \mathbf{E} \cdot d \mathbf{S} + \int_{S_{bottom}} \mathbf{E} \cdot d \mathbf{S} = \frac{\rho_s \Delta S}{\varepsilon_o}$$
- The flux on the bottom surface is 0, since $\mathbf{E} = 0$ in a perfect conductor. The flux on the sides is 0, as we take $\Delta h \rightarrow 0$. As such, we are left with the flux out the top, which is equal to $E_n \Delta S$ (as a result of the dot product, where the normal is defined relative to the surface). 
$$E_n \Delta S = \frac{\rho_s \Delta S}{\varepsilon_o} \implies E_n = \frac{\rho_s}{\varepsilon_o}$$

**Summary:** 
- Inside a perfect conductor $\mathbf{E}  = 0$ and $\rho_v = 0$ 
- On the surface of a perfect conductor $E_t = 0$ and $E_n = \frac{\rho_s}{\varepsilon_o}$




## Lecture 14—Dielectrics and Polarization 

- Dielectrics: There are no free charges, but the atoms are polarizable. As opposed to the free charges of a conductor, the charges in a dielectric are bound to the atoms, so we can model each individual atom as a dipole with a positive and negative charge. 
- When the electric field is applied, the dipoles will align themselves with the field, creating a net polarization.
- Define the polarization vector as the dipole moment per unit volume: $\mathbf{P} = \frac{\mathbf{p}}{V}$. The polarization vector points in the direction of the positive charge.

### Potential produced by a dipole $\mathbf{p_k} $

$$ V_k \simeq \frac{\mathbf{p_k} \cdot (\mathbf{R} - \mathbf{R'_k})}{4\pi \varepsilon_o |\mathbf{R} - \mathbf{R'_k}|^3}$$
- We call the density of electric dipole moments $\mathbf{P}$, the polarization vector. By definition $\mathbf{P} = \frac{d \mathbf{p}}{dv'}$, where $\mathbf{p}$ is the dipole moment of the atom per unit volume element $dv'$. thus, the differential potential produced by a dipole $d \mathbf{p}$ is:
$$dV = dv' \frac{\mathbf{P} \cdot (\mathbf{R} - \mathbf{R'})}{4\pi \varepsilon_o |\mathbf{R} - \mathbf{R'}|^3}$$
- Since $\mathbf{p} = \mathbf{P} dv'$. 
- The total potential produced by the polarization is the integral over the entire volume: 
$$ V = \int_{v'} \frac{\mathbf{P} \cdot (\mathbf{R} - \mathbf{R'})}{4\pi \varepsilon_o |\mathbf{R} - \mathbf{R'}|^3} dv'$$


## Lecture 15—Dielectrics: Densities of Polarization Charges and Generalized Gauss' Law

### Polarization Charge Density
- Using the above formula, we apply the divergence theorem to find the volume charge density of polarization charges (not shown):
$$ V = \int_{s'} \frac{\mathbf{P} \cdot \mathbf{a_n'} }{4\pi \varepsilon_o |\mathbf{R} - \mathbf{R'}|} ds' + \int_{v'} \frac{\nabla' \cdot \mathbf{P}}{4\pi \varepsilon_o |\mathbf{R} - \mathbf{R'}|} dv'$$ 
- We call $\rho_{p,s} = \mathbf{P} \cdot \mathbf{a_n'}$ the surface charge density of polarization charges. Its reppective integral is the potential produced by the polarization charges on the surface.
- We call $\rho_{p,v} = - \nabla' \cdot \mathbf{P}$ the volume charge density of polarization charges. Its respective integral is the potential produced by the polarization charges in the volume.

- Intuitively, the surface charge density of polarization charges is the projection of the polarization vector onto the normal vector of the surface. 
- The volume charge density is the divergence of the polarization vector. 
    - If the electric field is uniform, the polarization vector will be uniform, and the volume charge density will be 0, since the divergence or the flux of the polarization vector at an infintesimal volume is 0 
    - If the electric field is non uniform, then the polarization vector will not be uniform, and the volume charge density will be non zero. 


### Generalized Gauss' Law 
- Now, we may generalize Gauss' Law to include both free charges $\rho_v$ and polarization/bound charges $\rho_v$. 
- In free space, we have that $\nabla \cdot \mathbf{E}  = \frac{\rho_v}{\varepsilon_o}$; however, in a material we simply add the free and polarization charges together: 
$$ \nabla \cdot \mathbf{E} = \frac{\rho_v + \rho_{p,v}}{\varepsilon_o} $$
- Similarly, $\varepsilon_o \nabla \cdot \mathbf{E} = \rho_v - \nabla \cdot \mathbf{P} \rightarrow \nabla \cdot (\varepsilon_o \mathbf{E} + \mathbf{P}) = \rho_v$, we define $\mathbf{D} = \varepsilon_o \mathbf{E} + \mathbf{P}$, the *electric displacement field*.
$$\nabla \cdot \mathbf{D} = \rho_v$$ 
- So the divergence of the electric displacement field is equal to the free charge density. Note that this is the same situation as before: when dealing with charges in free space, $\mathbf{P} = 0 \implies \mathbf{D} = \mathbf{\epsilon_o \mathbf{E}}$ which is just Gauss' Law. 






## Lecture 16 - Material Behaviours

### Funadmental Postulates of Electrostatics
$$\text{Differential Form} = \begin{cases} \nabla \cdot \mathbf{D} = \rho_v \\ \nabla \times \mathbf{E} = 0 \end{cases}$$

$$\text{Integral Form} = \begin{cases}  \oint \mathbf{D} \cdot d \mathbf{S} = Q_{enc} \\  \oint \mathbf{E} \cdot d \mathbf{l} = 0 \end{cases}$$

### Material Behaviour—Linear and Isotropic: 
- $\mathbf{D} = \varepsilon \mathbf{E} + \mathbf{P}$ depends on the material. 
- Linear and isotropic materials: 
$$\mathbf{P} = \varepsilon_o \chi_o  \mathbf{E}$$
- So in the case of a perfect conductor, where $\mathbf{E} = 0$, there is no polarization vector

$$\mathbf{D} = \varepsilon \mathbf{E} + \mathbf{P} = \varepsilon \mathbf{E} + \varepsilon_o \chi_e \mathbf{E} = \varepsilon_o (1 + \chi_e) \mathbf{E} = \varepsilon_o \varepsilon_r \mathbf{E} = \varepsilon \mathbf{E}$$ 
- We call $\chi_e$ the dielectric susceptibility, $\varepsilon_r$ the relative permitivity and $\varepsilon$  the total or absolute permitivity. 

- We may also consider Electrets, which are materials with constant polarization vectors $\mathbf{P}$ even in the absence of an electric field (permanent magnets). 

## Lecture 17 - Generalized Gauss Law and Boundary Conditions

### Tangential Boundary Conditions:
- Recall that the curl of the electric field is 0, so we can apply the same logic as before to find the tangential component of the electric field:
$$\oint_c \mathbf{E} \cdot d \mathbf{l} = 0 \implies {E_{t,1}} = {E_{t,2}}$$
### Normal Boundary Conditions: 
- Using Gauss' Law with the displacement field: 
$$\oint \mathbf{D} \cdot d \mathbf{S} = Q_{enc} \implies D_{n,1} - D_{n,2} = \rho_{s}$$ 
- Where $\rho_s$ is the surface charge density of free charges, if the boundary is between two perfect dielectrics, then there is **no free charge density**, so $\rho_s = 0 \implies D_{n,1} = D_{n,2}$


## Lecture 18 - Refraction and Dielectric Breakdown: 

### Electromagnetic derivation of Snell's Law 
- Let us derive a relation bewteen the angle of incidence $\alpha_1$ and angle of refraction $\alpha_2$ between two perfect dielectrics.
- Consider two media with $\mathbf{E_1}$ and $\mathbf{E_2}$, and absolute permitivities $\varepsilon_1$ and $\varepsilon_2$.
    - **Tangential BC:** At their interface, we know that $E_{t,1} = E_{t,2}$, expressing these values in terms of their angles we have that $E_{1} \sin \alpha_1 = E_{2} \sin \alpha_2$. 
    - **Normal BC:** At their interface, we know that $D_{n,1} - D_{n,2}= \rho_s = 0 $ since we are working with two perfect dielectrics with no free surface charges. Expressing these values in terms of their angles we have that: 
    $$ D_{n,1} = \varepsilon_1 E_1 \cos \alpha_1 = \varepsilon_2 E_2 \cos \alpha_2 = D_{n,2}$$
    - Combining both of these equalities through dividsiton we have that $$\tan \alpha_1 = \frac{\varepsilon_1}{\varepsilon_2} \tan \alpha_2$$


### Dielectric Breakdown 
- Recall, the electric field is simply the force experienced by a charge at a point in space. It makes sense that at a large $\mathbf{E}$, even bound electrons can be ripped from their clouds and become free charges. 
- We express the breakdown field as the field at which the dielectric becomes a conductor. It is also called the dielectric strength: $$|\mathbf{E}| > E_{br}$$



## Lecture 19 - Capcitance: 
- At the corners and edges of conductors, charges will bunch up, to minimize the repelling effects of other electrons. Due to the large free charge surface density, the electric field will be largest at these points: $E_n = \frac{\rho_s}{\varepsilon_o}$.  

### Capacitance

#### Single Object: 
- Consider a conductor, with total charge $Q$ and potential $V$, doubling the charge will double the potential—$Q$ is always proportional to $V$. We say that $$Q = C V$$ where $C$ is the capacitance of the conductor.

#### Two Objects:
- Consider two conductors 1 and 2 with charges $+Q$ and $-Q$ respectively. The potential difference between the two conductors is $V_{12}$. Capcitence is defined as the ratio of the charge on one conductor to the potential difference between the two conductors: 
$$ C = \frac{Q}{V_{12}}$$

- $C$ depedns only on the geometry and material, not on the charge or potential.

**Steps to find capacitance:**
1) Choose coordinate system
2) Assume there is $+Q$ on one conductor and $-Q$ on the other. The conductor with $+Q$ is called object 1. 
3) Find the electric field
4) Find the potential difference between the two conductors $$V_{12} = - \int_{\text{object 2}}^{\text{object 1}} \mathbf{E} \cdot d \mathbf{l}$$
5) Find the capacitance: $$C = \frac{Q}{V_{12}}$$

    - Note that the charge $Q$ should not appear in the final calculation of $C$, as the capacitence only depends on the geometry and material.


## Lecture 20 - Parallel Plate Capacitor
- Consider two plates with area $A$ at a distance $d$ from each other with permetivity $\varepsilon$ between the plates. Assume that there are no edge effects. Let us find the capacitence:
1) We choose cartesian coordinate system
2) Place $+Q$ on the top plate and $-Q$ on the bottom plate. Let us now assume that the charge distributes evenly throughout the plates.
3) The electric field is found to be $\mathbf{E} - \frac{\rho_s}{\epsilon} \mathbf{a_y} \rightarrow \mathbf{E} = -\frac{Q}{A \varepsilon} \mathbf{a_y}$  
4) Now we can find the potential between the two objects: 
$$V_{12} = - \int_{y=0}^{y=d} -\frac{Q}{A \varepsilon} \mathbf{a_y} \cdot d \mathbf{l} = \frac{Qd}{A \varepsilon}$$
5) Finally, we can find the capacitance:
$$C = \frac{Q}{V_{12}} = \frac{A \varepsilon}{d}$$

- As expected the capacitence depends solely on the geometrical and material properties of the capacitor.


## Lecture 21 - Energy in Electrostatics


### Theory
- Consider two point charges at some distance from each other. Pretend these charges are held together by some stick; when we break the stick, the charge gain kinetic energy and repel. 
- Let's consider the work done to bring the charges from infinity to their positions. The work done to move $q_1$ to $\mathbf{R_1}$ is 0 J since there is no electric field. To move $q_2$, we must overcome the repulsion of $q_1$, as such, we consider the potential of $V_1$ at the position of $q_2$ which is $\mathbf{R_2}$, $V_1(\mathbf{R_2}) = \frac{W}{q_2}$. Thus, the work done is $$W = q_2 V_1(\mathbf{R_2})$$
- Notice that we could have done the same thing, but moving $q_2$ first, $$W = q_1 V_2(\mathbf{R_1}) = q_2 V_1 (\mathbf{R_2}) = W$$

### Discrete
- For $N$ discrete charges of value $q_N$ in positions $\mathbf{R_N}$, the total work done to bring the charges from infinity to their positions is: $$W_e = \frac{1}{2} \sum_{i=1}^{N} q_i V_i(\mathbf{R_i})$$
- Where $V_i(\mathbf{R_i})$ is the potential at the position of charge $q_i$ due to all the other charges excluding $q_i$. 
- Note that the factor of $\frac{1}{2}$ is to avoid double counting the work done. Without the factor, we would be counting the work done to bring $q_i$ to its position twice.

### Continuous
$$ W_e = \frac{1}{2} \int_{v'} \rho_v V(\mathbf{R}) dv$$

- By applying some identities, we can find other, more practical forms of the energy in electrostatics. First we know that from generalized Gauss' Law $\rho_v = \nabla \cdot \mathbf{D}$, so we get that (derivation not shown here):
$$W_e = \frac{1}{2} \int_{\mathbb{R}^3} \mathbf{D} \cdot \mathbf{E} dv'= \frac{1}{2} \int_{\mathbb{R}^3} \varepsilon_{absolute}\mathbf{E} \cdot \mathbf{E} dv' = \frac{1}{2} \int_{\mathbb{R}^3} \varepsilon |\mathbf{E}|^2 dv'$$

- Using the above formula, we can revisit the parallel plate capacitor calculation to find the energy stored in the capacitor:
    - Recall that the electric field between the plates (assuming no edge effects) is $$\mathbf{E}  = \frac{1}{2} \int_{\mathbb{R}^3} \varepsilon \left(\frac{V_o}{d}\right)^2 dv' = \frac{1}{2} \varepsilon \frac{V_o^2}{d^2} A d = \frac{1}{2} \frac{Q^2}{C} = \frac{1}{2} Q V_o = \frac{1}{2} C V_o^2$$ 




## Lecture 22 - Poisson Equation and BVPs
- From the generalized Gauss' Law we know that $\nabla \cdot \mathbf{D} = \rho_v$, and from linear materials we know that $\mathbf{D} = \varepsilon \mathbf{E} = - \varepsilon \nabla V$. Combining these two, $$\nabla \cdot (\varepsilon \nabla V) = - \rho_v$$

### Boundary Value Problems
- Consider a volume $v$ with boundary $S$, where $\rho_v$ is the volume charge density: $$\begin{cases} \nabla \cdot (\varepsilon \nabla V) = - \rho_v  \text{ in } v \\ V = V_o \text{ on } s \end{cases}$$ 

**Example** 
- Consider two maetallic plates at $V = 0$ and $V = V_o$ respectively with a dielectric in between with uniform $\varepsilon$. We apply the Poisson Equation, 
$$ \nabla \cdot (\varepsilon \nabla V) = 0 \rightarrow \varepsilon \nabla ^2 V = 0$$  
- Now, we solve for $V$ by applying the boundary conditions: $V(y=0) = 0, V(y=d) = V_o$ 


### Image Theory 
- Consider a point charge $q$ at some distance $d$ from a grounded conductor. The potential at the conductor is $V_o$ and is an infinite metallic plane where $\mathbf{E} = 0$. This problem is difficult to solve, so we can use image theory to simplify the problem: we place a charge $-q$ at a distance $d$ from the plane, called an image charge 


## Lecture 23 - Current and Current Density
- Current is any motion of charge. The possible mechanisms are conduction, electrolysis, convection and displacement. 


### Conduction of Current
- Consider a lock of conductive material, when there is on external field applied, $\mathbf{E} = 0 $, electrons move randomly due to thermal vibrations and energy, there is no **net** flow of charge. 
However, when $\mathbf \neq 0$ there will be organized **steady** curren. We call $\mathbf{u}_e = -\mu_e \mathbf{E}$ the drift velocity of the electrons, where $\mu_e$ is the electron mobility.

### Current 
- Consider a differential surface element $d \mathbf{S}$. At time $ t= 0$, there is no charge passing through the surface; however, at time $t = dt$, there is some charge passing through the surface, $dq$. The differential current element is $dI = \frac{dq}{dt}$
- To find the total current through some surface S, we take the surface integral: $$I = \int_S dI = \int_S \rho \mathbf{u} \cdot d \mathbf{S}$$
- This is similar to fluid mechanics, where $\dot{m} = \int_S \rho_m \mathbf{u} \cdot d \mathbf{S}$
- A proof of the continuity equation is as follows: 
    - Consider the side view of some plane $d\mathbf{S}$ with some differential length element $d\mathbf{l}$. In some time $dt$, charges will move by $d \mathbf{l} = \mathbf{u} dt$ 
    - As such, the amount of charge is $dq = \rho dv = \rho \  d\mathbf{l} \cdot d\mathbf{S}$
    - Thus, the current element is $dI = \frac{dq}{dt} = \rho \mathbf{u} \cdot d\mathbf{S}$ as required. 
- **Note** current has a positive sign convention (i.e. a positive current is a result of positive charges moving in that direction, or negative charges moving in the opposite direction, or both)

### Current Density
- The current is a macroscopic property, in that it is the total charge passing through a surface. The current density is a microscopic property, in that it is the charge passing through a unit area. $$I = \int_S \rho \mathbf{u} \cdot d \mathbf{S} = \int_S \mathbf{J} \cdot d \mathbf{S} \implies \mathbf{J} = \rho \mathbf{u}$$
- Replacing $\mathbf{u}$ with our previous definition of drift velocity $\mathbf{u} = -\mu \mathbf{E}$: 
$$\mathbf{J} = -\rho \mu \mathbf{E} \rightarrow \mathbf{E} \sigma$$
- We call $\sigma = \rho \mu$ the conductivity of the material, and is positive for conductors. Current density is also known as microscopic Ohm's Law.


## Lecture 24 - Ohm's Law, Resistance and Continuity

### Resistance
- Consider two conductors with connected by a conductive material with conductivity $\sigma$. Now place a battery with potential difference $V_o$ between the two conductors: an electric field will be established between the two conductors and there will be current density $\mathbf{J} = \sigma \mathbf{E}$. 
- From a macroscopic perspective, we can define the resistance $R$ as the ratio of the potential difference to the current: $$R = \frac{V}{I}$$

**Example Calculating Resistance**
- Consider a parallel plate capacitor connected by a wire with current flowing through it. the conductivity of the material between the plates is given by $\sigma$

1) Choose coordinate system
2) Find $\mathbf{E}$ in the case of a parallel plate capacitor $\mathbf{E} = \frac{V_{12}}{l} (-\mathbf{a_z}) $
3) Find $\mathbf{J}$ using Ohm's Law: $\mathbf{J} = \sigma \mathbf{E} = \frac{\sigma V_{12}}{l} (-\mathbf{a_z})$
4) Find $I$ by integrating the current density over the surface: $$I = \int_S \mathbf{J} \cdot d \mathbf{S} = \frac{\sigma V_{12} S}{l}$$
5) Find resisitance $R = \frac{V_{12}}{I} = \frac{l}{\sigma S}$

- Once again, we see that resistance just like capacitence depends only on the geometry and material properties of the conductor.

### Continuity Equation
- Consider a closed surface $S$. By conservation of charge $q_{in}(t) + q_{out}(t) = C$. By taking the time derivative: $\frac{\partial q_{in}(t)}{\partial t} + \frac{\partial q_{out}(t)}{\partial t} = 0$. Now we can rewrite the above equation in terms of a volume integral and the flux of current density: 
$$ \frac{\partial }{\partial t} \left[ \int_v \rho_v(t) dv\right] + \int_S \mathbf{J} \cdot d \mathbf{S} = 0$$ 
- Intuitively, we have that the change of charge within the surface $S$ plus the current flowing thorugh the surface $S$ is equal to 0. By Divergence Theorem, we rewrite the above as: $$\frac{\partial \rho_v}{\partial t} + \nabla \cdot \mathbf{J} = 0$$
- Intuitively, if $\nabla \cdot \mathbf{J} > 0$, then the charge density at that point must decrease since charge is moving away. 

**Kirchoff Current Law Derivation**
- Consider a closed surface $S$ with various branches of current flowing through. By the continuity equation $\int_S \mathbf{J} \cdot d \mathbf{S} = 0$, we can rewrite this as:

$$\int_{S_1} \mathbf{J} \cdot d \mathbf{S} + \int_{S_2} \mathbf{J} \cdot d \mathbf{S} +... + \int_{S_n} \mathbf{J} \cdot d \mathbf{S} = 0 \rightarrow \sum_{i=1}^{n} \int_{S_i} \mathbf{J} \cdot d \mathbf{S} = 0 $$





## Lecture 25 - Relaxation Equation and Joule Effect

### Relaxation Equation
- Consider a piece of uniform material with conductivity $\sigma$ and absolute permitivity $\varepsilon$. We can make use of the differential form of the continuity equation: 
$$\frac{\partial \rho_v}{\partial t} + \nabla \cdot \mathbf{J} = 0 \rightarrow \frac{\partial \rho_v}{\partial t} + \nabla \cdot (\sigma \mathbf{E}) = 0 \rightarrow \frac{\partial \rho_v}{\partial t} + \sigma \nabla \cdot \mathbf{E} = 0 $$
- Recall from Gauss' Law that $\nabla \cdot \mathbf{E} = \frac{\rho_v}{\varepsilon} $, so we can rewrite the above equation as a first order differential equation: 
$$\frac{\partial \rho_v}{\partial t} + \frac{\sigma }{\varepsilon} \rho_v= 0$$
- Solving this differential equation, we find that the charge density decays exponentially with time: $$\rho_v(t) = \rho_v(0) e^{-\frac{t}{\tau}}$$ 
- We call $\tau = \frac{\varepsilon}{\sigma}$ the relaxation time and it is the time required for the charge density to decrease by a factor of $e$.

### Joule Effect
- Consider the work done by $\mathbf{E}$ to move $dq$ by some distance $d \mathbf{l}$. From classical mechanics, we know that $W = \mathbf{F} \cdot \mathbf{l}$, we can apply the same thing, but with the electric field: $dW = dq \mathbf{E} \cdot d\mathbf{l} = \rho dv \mathbf{E} \cdot d\mathbf{l}$. 
- Now, if we were to divide both sides by $dt$, we would receive power: $\frac{dW}{dt} = \rho dv \mathbf{E} \frac{d \mathbf{l}}{dt} \rightarrow P = \rho \ \mathbf{E} \cdot \mathbf{u} dv = \mathbf{J} \cdot \mathbf{E} \ dv$. To find the total power we simply integrate over the entire volume:
$$ P = \int_v \mathbf{J}\cdot \mathbf{E} dv  \rightarrow P = \int_v \sigma |\mathbf{E}|^2 dv$$
- Note the similarities between $P = IV = I^2 R$



## Lecture 26 - Boundary Conditions for Current Density


### Tangential Boundary Conditions
- Consider a surface $S$ between two media with different conductivities $\sigma_1$ and $\sigma_2$. From the boundary conditions of a perfect conductor, we know that the tangential components of the electric field are equal: $E_{t,1} = E_{t,2}$; therefore, $$\frac{{J_{1,t}}}{\sigma_1} = \frac{{J_{2,t}}}{\sigma_2}$$

### Normal Boundary Conditions
- We can apply the continuity equation in integral form: 
$$\int_{S} \mathbf{J} \cdot d \mathbf{S} + \frac{\partial}{\partial t} \int_v \rho_v dv = 0 \rightarrow J_{2,n} A - J_{1,n} + \frac{\partial \rho_s}{\partial t} = 0 $$




## Lecture 27 - Magnetostatics 

### Magnetostatics: Magnetic Force and Postulates
- When charges are in motion, they produce a magnetic field. The magnetic force is proportional to the charge, the velocity and the magnetic flux density. $$\mathbf{F} = q \mathbf{u} \times \mathbf{B} + q \mathbf{E}$$
- Note when using the RHR, the index finger is the first term in the cross product $\mathbf{u}$, the middle finger is the second term, $\mathbf{B}$ and the thumb is the product, the force. 


**Postualte 1**
- The magnetic field is divergenceless: $\nabla \cdot \mathbf{B} = 0 \implies \oint_s \mathbf{B} \cdot d \mathbf{S} = 0$. This is because there are no isolated magnetic charges like there are in electrostatics. Also note that you can never have an isolated +ve or -ve magnetic charge. Breaking a magnet will result in two magnets with a north and south pole and so forth.

**Postulate 2: Ampère's Law**
- The magnetic field is solenoidal:$$\nabla \times \mathbf{B} = \mu \mathbf{J} \implies \oint_c \mathbf{B} \cdot d \mathbf{l} = \mu I_{enc}$$ 
- Where $\mu_o$ is called hte permeavility of free space

### Vector Potential (some math)
- From vector calculus we know that $\nabla \cdot (\nabla \times \mathbf{A}) = 0$. We express the magnetic flux density as the curl of some vector potential: $\mathbf{B} = \nabla \times \mathbf{A}$. 
    - Proof: $\nabla \cdot \mathbf{B} = \nabla \cdot (\nabla \times \mathbf{A}) = 0$, so $\mathbf{B} = \nabla \times \mathbf{A}$
- We need to contrain $\nabla \cdot \mathbf{A}$ since there exists an infinite number of vector potentials that satisfy $\mathbf{B} = \nabla \times \mathbf{A}$. We choose $\nabla \cdot \mathbf{A} = 0$, called the Coulomb gauge.


### Poisson Equation for the Vector Potential
- From the second postulate we konw that $\nabla \times \mathbf{B} = \mu \mathbf{J} \rightarrow \nabla \times (\nabla \times \mathbf{A})$. We can apply the identity $\nabla \times (\nabla \times \mathbf{A}) = \nabla(\nabla \cdot \mathbf{A}) - \nabla^2 \mathbf{A}$ to find the Poisson Equation for the vector potential:
$$\nabla (\nabla \cdot \mathbf{A} ) - \nabla^2 \mathbf{A} = - \mu \mathbf{J} \rightarrow - \nabla^2 \mathbf{A} = - \mu \mathbf{J}$$
- We make this simplifcation due to the Coulomb gauge.
- Note that this expression is the dual of the Poisson equation for the electric potential: $\nabla^2 V = - \frac{\rho_v}{\varepsilon}$

### Superposition Integral of the Vector Potential
$$\mathbf{A}(\mathbf{R}) = \frac{\mu}{4\pi} \int_{v'} \frac{\mathbf{J}}{|\mathbf{R} - \mathbf{R'}|} dv'$$

- Note again, that this is the dual of the superposition integral for $V$: 
$$V(\mathbf{R}) = \frac{1}{4\pi \varepsilon} \int_{v'} \frac{\rho_v}{|\mathbf{R} - \mathbf{R'}|} dv'$$


## Lecture 28 - Biot-Savart Law

### Alternate Form of the Superposition Integral
- Consider a wire, we can integrate along $c'$ in the direction where current $I$ is measured: 
$$\mathbf{A}(\mathbf{R}) = \frac{\mu}{4\pi} \int_{c'} \frac{I d \mathbf{l'} }{|\mathbf{R} - \mathbf{R'}|}$$

### Biot-Savart Law
- Instead of using the above integral to find $\mathbf{A}$ and then using $\mathbf{B} = \nabla \times \mathbf{A}$ to find the magnetic flux density, we can directly solve for $\mathbf{B}$ using the Biot-Savart Law:
$$\mathbf{B}(\mathbf{R}) = \frac{\mu}{4\pi} \int_{c'} \frac{I d \mathbf{l'} \times (\mathbf{R} - \mathbf{R'})}{|\mathbf{R} - \mathbf{R'}|^3}$$
- Note, both processes are equivalent, but the Biot-Savart Law is more practical for certain geometries.: 
    - Find $\mathbf{A}$ using the superposition integral and then compute $\mathbf{B}$ using $\mathbf{B} = \nabla \times \mathbf{A}$ 
    - Find $\mathbf{B}$ using the Biot-Savart Law

### Ampère's Law
- Consider a wire with current $I$ and a circular path $c$ around the wire. We can apply Ampère's Law to find the magnetic field. We choose $c$ such that the magnetic field is everywhere perpendicular or parallel to the path (amperium path):
$$\oint_c \mathbf{B} \cdot d \mathbf{l} = \mu_o I_{enc} $$

**Example: wire** 
- $\mathbf{B}$ can be found easily. Choose an amperium path $c$ which is a circle around the path at some radius $\mathbf{R}$ that encloses the wire and thus the current $I$. We see that $\mathbf{B}$ is everywhere parallel to the path, and so $\mathbf{B} \cdot d \mathbf{l} = B dl$. Thus, we have that:
$$\oint_c \mathbf{B} \cdot d \mathbf{l} = B \oint_c dl = B(2\pi R) = \mu_o I_{enc} \rightarrow B = \frac{\mu_o I}{2\pi R} \mathbf{a_\phi}$$





## Lecture 29 - Surface Current Density and Torque 

### Surface Current Density
- We have current density $\mathbf{J}$ for current in a volume. Let's assume a cross section of a prism has some $\Delta h$ and $\Delta w$. The current through the cross section is $I = J \Delta h \Delta w$. 
- By taking $\Delta h \rightarrow 0$, we have $\mathbf{J}_S$, the current per unit width, so $I = \mathbf{J}_S \cdot \Delta \mathbf{w}$.


### Ampère's Force Law
- Consider two closed circuits $c_1$ and $c_2$ with currents $I_1$ and $I_2$ respectively. The magnetic force due to circuit 1 on 2 is $\mathbf{F_m} = q_2 \mathbf{U_2} \times \mathbf{B}_1$. 
- The differential element is $d\mathbf{F}_{12} = dq_2 \mathbf{u_2} \times \mathbf{B_1} = dq_2 \frac{d\mathbf{l_2}}{dt}\times \mathbf{B_1} = I_2 d\mathbf{l_2} \times \mathbf{B_1}$
- Thus, the total force on circuit 2 is: 
$$ \mathbf{F}_{12} = \int_{c_2} d\mathbf{F}_{12}$$

### Magnetic Dipole
- Any small loop enclosing a surface $S$ carrying a current $I$ will create a magnetic dipole moment: $$\mathbf{m} = I \mathbf{a}$$


### Torque on a Current Loop
- Consider a circular loop with current flwoing around the loop in the clock wise direction. Apply some $\mathbf{B}$ with components normal to the plane and within the plane of the loop: $\mathbf{B} = \mathbf{B}_{\parallel} + \mathbf{B}_{\perp}$

    - Effect of $\mathbf{B}_{\perp}$: we know that $d \mathbf{F}_m = I d\mathbf{l} \times \mathbf{B}_{\perp}$, so in taking the cross product, we see that the force at every point on the circle points inwards, so the net force cancels out.

    - Effect of $\mathbf{B}_{\parallel}$: applying the same logic, we see that there is a force into the page at the top of the loop, and out from the page at the bottom of the loop. This creates a net torque on the loop: 

- In terms of the magnetic dipole, we realize that the normal, is into the page as defined by the RHR. We can now express the torque as follows: 
    $$\mathbf{T} = \mathbf{m} \times \mathbf{B}$$ 


# Midterm 2 Coverage ^


## Lecture 30 - Magnetization Current Densities

### Torque
- COnsider a loop in space, with a magnetic field $\mathbf{B}$, the torque on the loop is given by $\mathbf{T} = \mathbf{m} \times \mathbf{B}$



### Electrons producing magnetic dipole
- Consider an electron orbiting a nucleus, the electron creates a magnetic dipole (opposite its direction of travel by RHR)

- In a material, there are many of these atoms, when there is no magnetic field, $B_{ext} = 0$, the sum of the magnetic dipoles is 0, due to thermal vibrations. 
- However, apply an magnetic field, and the magnetic dipoles will align with the field. There will be a net current along ther boundary of the material 
$$\mathbf{B} = \mathbf{B}_{ext} + \sum \mathbf{B}_{k}$$


### Magnetization Current Densities 
- We define the magnetic current density as $$\mathbf{J}_m = \nabla \times \mathbf{M}$$, where $\mathbf{M}$ is the magnetization of the material.
- The surface current density is: $$\mathbf{J}_{m,s} = \mathbf{M} \times \mathbf{a}_n$$

### Generalized Ampère's Law 
- In free space, if we have some current density: $$\nabla \times \mathbf{B} = \mu_0 \mathbf{J}$$
- In a material, we have a magnetization current density: $$\nabla \times \mathbf{B} = \mu_0 (\mathbf{J} + \mathbf{J}_m)$$
    - We can further expand this to $$\nabla \times \frac{\mathbf{B}}{\mu_0} =  \mathbf{J} + \nabla \times \mathbf{M} \rightarrow \nabla \times \left(\frac{\mathbf{B}}{\mu_0} - \mathbf{M}\right) = \mathbf{J} \rightarrow \nabla \times \mathbf{H} = \mathbf{J}$$
    - Where $\mathbf{H} = \frac{\mathbf{B}}{\mu_0} - \mathbf{M}$ is the magnetic field intensity
- Rearranging for $\mathbf{B}$, we have that $$\mathbf{B} = \mu_0 \mathbf{H} + \mu_0 \mathbf{M} = \mu \mathbf{H}$$ 

### Material Behaviours:
1) Permanent magnets: $\mathbf{M}$ is constant even if $\mathbf{H} = 0$
2) Linear materials: $\mathbf{M} = \chi_m \mathbf{H}$, where $\chi_m$ is the magnetic susceptibility
    - $\mathbf{B} = \mu_0 \chi_m \mathbf{H} + \mu_0 \mathbf{H} = \mu_0 (1 + \chi_m) \mathbf{H} = \mu \mathbf{H}$, where in free space $\mu = \mu_0$, which is similar to the electric displacement field, $\mathbf{D} =  \varepsilon_0 (1 + \chi_e)\mathbf{E} = \varepsilon \mathbf{E}$
    - We call $\mu$ the permeability of the material and $\mu_r$ the relative permeability 




## Lecture 31 - Behaviours of Materials 
### Behaviours of Materials
1. Diamagentic
- When there is no magnetic field applied, $\mathbf{M} = 0$ 
- When a magnetic field is applied, $\mathbf{H} \rightarrow \mathbf{H} \approx 0$ 
    - Superconductors: $T < T_c \rightarrow \text{no resistsance}$, 
    - So $\chi_m = -1$  and $\mu_r = 1 + \chi_m =0 \implies \mathbf{B} = 0$

2. Paramagnetic Materials 
- $\mu_r > 1$, $\chi_m > 0$


3. Ferromagnetic Materials
- Iron and Nickel 


### Hysterisis Curve and Ferromagnetic Materials
- Ferromagnetic materials have many boundaries (grain boundaries) that each have their own magnetization. 
- When we apply an external $\mathbf{H}$, the magnetic dipoles will align with the field. 


**Magnetization**
1. Apply an external $\mathbf{H}$, 
2. Saturation is achieved, all atoms are magnetized 
3. We created a permanent magnet 

- When we remove the external field, the magnetic dipoles will not return to their original state, but will remain aligned.

**Demagnetization**
1. To remove the magnetization, we apply an external field in the opposite direction. 
2. The magnetization will not return to 0 when the external field is 0 
3. If we continue to increase the external field, the magnetization will eventually return to 0, at some value $H_c$ called the coercivity.
4. If we continue, the magnetization reaches its saturation value in the opposite direction.

### Boundary Conditions
- Between two media, the normal components of the magnetic flux density are equal: $$B_{n,1} = B_{n,2}$$
- The difference in the tangential components of the magnetic field is equal to the surface current density: $$H_{t,1} - H_{t,2} = J_s$$, similarly, $$\mathbf{a}_n \times (\mathbf{H}_1 - \mathbf{H}_2) = \mathbf{J}_s$$ 



## Lecture 32 - Magnetic Circuits 

### Analogy between Electric and Magnetic Circuits

**Magnetic**
- Consider a metallic C shaped material with $N$ turns of wire, where current $I$ flows. From the RHR, we know that there is an induced magnetic field $\mathbf{B}$ in the core. 
- Since the metal has high $\mu$, $\mathbf{B}$ will be confined to the core, as it flows along paths of high permeability.

**Electric**
- We compare this to a circuit with some magnetic material of conductance $\sigma$. The current flows along paths of high conductance. 


### Approximations 
1. We assume that all $\mathbf{B}$ lines flow in the core
2. Gaps are short
3. The area $S$ is small $\Phi_m = \oint_S \mathbf{B} \cdot d \mathbf{S} = B S$

![image-2.png](exam_review_1.png)
- From generalized Ampère's Law, we know that $\oint_c \mathbf{H} \cdot d \mathbf{l} = I_{enc}$. 
- Since there is a gap between the core, we split up the integral into two parts:
$$\oint_{L_g} \frac{\mathbf{B}}{\mu_c} \cdot d \mathbf{l} + \oint_{L_g} \frac{\mathbf{B}}{\mu_0} \cdot d \mathbf{l} = I_{enc} = NI$$
- Now let us work with the magnetic flux, recalling that $\phi_m = BS \rightarrow B = \frac{\Phi_m}{S}$: 
$$\int_{L_g} \frac{\Phi_m}{\mu_c S} \cdot d {l} + \int_{L_g} \frac{\Phi_m}{\mu_0 S} \cdot d {l} = NI$$
- Now we can evaluate the intergals as follows: 
$$\frac{\Phi_m}{\mu_c S} L_g + \frac{\Phi_m}{\mu_0 S} L_g = NI \rightarrow \Phi_m = \frac{NI}{\frac{L_g}{\mu_c S} + \frac{L_g}{\mu_0 S}}$$

#### Electric circuit analogy
- Using Ohm's Law, we see that:
1. The "Voltage" is $NI$ which is called the magnetomotive force 
2. The "Current" is $\Phi_m$ which is called the flux 
3. The "Resistances" are $\frac{L_g}{\mu_c S} + \frac{L_g}{\mu_0 S}$ which is called the reluctance
    - We have two resistances in series, $\mathbb{R}_c = \frac{L_g}{\mu_c S}$ and $\mathbb{R}_g = \frac{L_g}{\mu_0 S}$

- When generating our electric circuit, sign convention is important:
    - The magnetomotive force obeys the right hand rule
    - If the coils point the induced magnetic flux density downwards, then the magnetomotive force will also point downards 



## Lecture 33 - Inductance and Energy in Magnetic Fields

### Mutual Inductance 
- Consider two closed circuits carrying some current $I_1$ and $I_2$. 
- Consider the magnetic flux produced from $\mathbf{B}_1$ through surface $C_2$ 

$$\Phi_{21}  = \int_{s_2} \mathbf{B_1} \cdot d \mathbf{S_2} = L_{21} I_1$$
- Note in $L_{21}$, the first index is that experiencing the magnetic field, and the second index is the one producing the magnetic field: 
- Note that the units of inductance are Henrys, $H = \frac{Wb}{A}$


### Self Inductance
- We can also consider the flux produced by $\mathbf{B}_1$ through $C_1$ 
$$\Phi_{11} = \int_{s_1} \mathbf{B_1} \cdot d \mathbf{S_1} = L_{11} I_1$$
- So in this case $L_{11}$ means that circuit 1 experiences the magnetic field produced by itself.


*It is important to note that $\Phi_{21} < \Phi_{11}$* 
- This is becaue $L_{11} \geq L_{21}$, notall $B_1$ lines will flow through $C_2$


### Steps to Find Inductance
1. Choose your coordinate system 
2. Assume some current $I_1$ on circuit 1 
3. Find $\mathbf{B}_1$ through Ampère's Law 
4. Find $\phi_{21}$ through integration: 
$$\Phi_{21} = \int_{s_2} \mathbf{B}_1 \cdot d \mathbf{S}_2$$
5. Find $L_{21}$ by dividing by $I_1$
    - You should find that the inductance depends on the geometry 
    - It can be negative as well but that just depends on the sign convention you start with


### Energy in Magnetic Fields
- Recall ECE159, when current flows through an inductor, we know it creates a magnetic field. Thus energy is stored within the field: 
$$W_m = \frac{1}{2} \int_{\mathbb{R}^3} \mathbf B \cdot \mathbf H dv'$$
- Note the similarities between this and the energy stored in an electric field:
$$W_e = \frac{1}{2} \int_{\mathbb{R}^3} \mathbf D \cdot \mathbf E dv'$$

### Energy stored in a Inductor 
 $$ W_m = \frac{1}{2} L I^2$$


### Finding $L$ through magnetic energy 
1. Impose current $I_1$ 
2. Find $\mathbf{B}_1$ through Ampère's Law
3. Find $W_m$ 


## Lecture 34 - Inductance and Chemical Batteries and EMF 

### Finding $L$ through magnetic energy 
1. Impose current $I_1$ 
2. Find $\mathbf{B}_1$ through Ampère's Law
3. Find $W_m$ 

![image-2.png](exam_review_2.png)
1. So we impose some current $I1$ through the cylinder. 
2. We can find $B$: 
    - Inside the first cylindre, $\mathbf{B} = \frac{\mu_0 r I_1}{2 \pi a^2} \mathbf{a}_\phi$ 
    - In the gap, $\mathbf{B} = \frac{\mu_0 I_1}{2 \pi r} \mathbf{a}_\phi$
    - Outside the second cylinder, $\mathbf{B} = 0$

3. We can find the magnetic energy by integrating over the various regions: $W = W_{m,1} + W_{m,2}+ W_{m,3}$
- To find the inductance per unit length, we divide by the length.......

### Non Conservative Electric Fields
- For some surface, with some current density $\mathbf{J}$, we require an electric field to maintain the current. Since $\oint \mathbf{E} \cdot d \mathbf{l} = 0$, the work done, is zero, so to maintain the current, the electric field must be non-conservative, and there must be an input of energy. 

### Chemical Batteries 
- In a battery, chemical reactions produe a force on its charges called $E_{nc}$ which is non-conservative. The postive ions will move to the positive terminal and the negative ions will move to the negative terminal, according to $E_{nc}$. 
- However, the charge separations will produce a consdervative electric field $\mathbf{E_c}$, which cancels out the non-conservative field within the battery
- However, outside of the battery, there will be a conservative field
- So we have that $$\mathbf{E} = \mathbf{E_c} + \mathbf{E_{nc}}$$


### Electromotive Force
$$ V_{emf} = \oint \mathbf{F}_{nc} \cdot d \mathbf{l}$$
- So it is the work done by an EM field on a charge $q$ along a closed path $c$
- Note that we only need non conservative $\mathbf{E}$ 
- $$ V_{emf} = \oint \left[ \frac{q \mathbf{E} + q \mathbf{u} \times \mathbf{B}}{q} \right] \cdot d \mathbf{l}$$



### EMF of battery
- The total electric field is $\mathbf{E} = \mathbf{E_{nc}} + \mathbf{E_c}$
- Take the EMF on some closed path $c$ where we divide the path into two parts: $c_1$ outside the battery and $c_2$ inside the battery
$$ V_{emf} = \oint_{c_1 + c_2} \mathbf{E} \cdot d \mathbf{l} = \int_{c_1 + c_2} \mathbf{E}_{nc} \cdot d \mathbf{l}  + \int_{c_1 + c_2} \mathbf{E}_{c} \cdot d \mathbf{l}$$ 
- However, we know that the path integral for the conservative field must be 0, and we know that $\mathbf{E}_{nc} exists only within the battery, so we can rewrite the above as:

$$ V_{emf} = \int_{c_2} \mathbf{E}_{nc} \cdot d \mathbf{l}$$ 


*Altnerate Expression*
- We can also consider the line integral to be 
$$ V_{emf} = \oint_{c_1 + c_2} \mathbf{E} \cdot d \mathbf{l} = \int_{c_1} \mathbf{E} \cdot d \mathbf{l} + \int_{c_2} \mathbf{E} \cdot d \mathbf{l}$$
- We know that the first integral is 0, since the total electric field is 0 within the battery 
- We also know that the second integral simply represents the voltage across the battery 



## Lecture 35 - Faraday's Law 
*Relating electric and magnetic phenomena*
### Faraday's Law
- Given some closed contour $S$ with some normal normal surface vector $\mathbf{a}_n$ defined according to the RHR, we define 
$$ \oint \mathbf{E} \cdot d \mathbf{l} = - \frac{d}{dt} \int_{s} \mathbf{B} \cdot d \mathbf{S}$$
- This states that the EMF is equal to the negative rate of change of the magnetic flux. 
- We can rewrite this using Stokes' Theorem:
$$ \nabla \times \mathbf{E} = - \frac{\partial \mathbf{B}}{\partial t}$$
- We represent the EMF as a voltage source using the right hand rule, where our fingers represent the positive end of the voltage source.


### Induced EMF
From the equation, we can see the conditions that lead to an induced EMF:
1. Transformer EMF: Time  varying $\mathbf{B}(t)$ 
2. Motional EMF: Motion (changes $ds$) 
3. Total EMF: both 



## Lecture 36 - Inductors and Transformers

### Inductors
- Within some coil, we put in a time varying current. The flux is equal to the self inductance times the current: $\Phi = Li_L(t)$
- The induced EMF is therefore: 
$$ V_{emf} = - \frac{d}{dt} \Phi_m(t) = -L \frac{dI_L}{dt}$$
- We also know that the flux enclosed within the circuit, points upward. So applying the RHR to the circuit, we see that the induced EMD will point in the same direction as the current source. 
$$ V_L(t) + V_{emf} = 0 \rightarrow V_L(t) = -L \frac{dI_L}{dt}$$


### Transformers
- Consider two coils wrapped around some magnetic core. 
- Coil 1 has $N_1$ turns and coil 2 has $N_2$ turns.
- From the right hand rule, we can apply our circuit analogies and we see that $N_1 i_1$ will produce a magnetic field that points in the same direction as the magnetic field produced by $N_2 i_2$
- We know that there is some reluctance from the core, and we also know that the magnetic flux is:
$$\\Phi_m(t) = \frac{N_1 i_1 (t) + N _2 i_2(t)}{R_C}$$

We can find the induced EMF in coil 1:
- $$V_{emf, 1} = - \frac{d}{dt} ( N_1 \Phi_m (t)) = - N_1 \frac{d \Phi_m(t)}{dt}$$
- From KVL, we know that the voltage produced at the coil 1 is the negative of the induced EMF:
$$V_1(t) = - V_{emf, 1} = N_1 \frac{d \Phi_m(t)}{dt}$$

We can find the induced EMF in coil 2 and thus the voltage on coil 2: 
- $$_2(t) = - V_{emf, 2} = N_2 \frac{d \Phi_m(t)}{dt}$$

Dividing the two ratios we have that 
$$\frac{V_1(t)}{V_2(t)} = \frac{N_1}{N_2}$$

We can also substitute our magnetic circuit expression into the voltages for $V_1(t)$ and $V_2(t)$ to find that:
$$ \begin{cases}
v_1(t) = \frac{N_1^2}{R_C} \frac{di_1(t)}{dt} + \frac{N_1 N_2}{R_C} \frac{di_2(t)}{dt} \\
v_2(t) = \frac{N_1 N_2}{R_C} \frac{di_1(t)}{dt} + \frac{N_2^2}{R_C} \frac{di_2(t)}{dt}
\end{cases}$$

$$ \begin{cases}
v_1(t) = L_{11} \frac{di_1(t)}{dt} + L_{12} \frac{di_2(t)}{dt} \\
v_2(t) = L_{21} \frac{di_1(t)}{dt} + L_{22} \frac{di_2(t)}{dt}
\end{cases}$$

- What is interesting to note is that $L_{12} = L{21}$, this is what couples our inductors, hence coupled magnetic circuits 


### Lenz' Law 
- Given some external, time varying magnetic field $\mathbf{B_1}(t)$, the induced EMF will produce a current that will produce a magnetic field $\mathbf{B_2}(t)$ that opposes the external field.
- So at time $t_1$, let us assume that the external field is increasing, 
- At some time $t_2$, there will be some induced EMF that will produce a current that will produce a magnetic field that opposes the external field.
$$ V_{emf} = - \frac{d}{dt} \Phi_m(t) $$



## Lecture 37 - Faraday's Law 

### Faraday's Law
- Recall that: 
$$ \oint \mathbf{E} \cdot d \mathbf{l} = - \frac{d}{dt} \int_{s} \mathbf{B} \cdot d \mathbf{S}$$

### $\mathbf{E}$ and $\mathbf{H}$ in different reference systems
- We know that $\mathbf{F} = q \mathbf{E} + q \mathbf{u} \times \mathbf{B}$ 
- However, we can consider two reference frames for a charge: 
    - According to the reference frame at rest, the charge is moving with some velocity $\mathbf{u}$, so $F = q\mathbf{E}  + q \mathbf{u} \times \mathbf{B}$ 
    - According to the reference frame of the particle, the charge is at rest, so $F = q \mathbf{E'}$

- We can equate the two forces to find that:
$$ q \mathbf{E} + q \mathbf{u} \times \mathbf{B} = q \mathbf{E'} \implies \mathbf{E'} = \mathbf{E} + \mathbf{u} \times \mathbf{B}$$


### Another way to find $V_{emf}$
$$V_{emf} = - \int_{S} \frac{\partial \mathbf{B}}{\partial t} \cdot d \mathbf{S} + \oint_{c} (\mathbf{u} \times \mathbf{B}) \cdot d \mathbf{l}$$
- We call the first term the transformer EMF and the second term is the motional EMF 



## Lecture 38 - Motional EMF and Eddy Currents 
- Recall that 
$$V_{emf} = - \int_S \frac{\partial \mathbf{B}}{\partial t} \cdot d \mathbf{S} + \oint_c (\mathbf{u} \times \mathbf{B}) \cdot d \mathbf{l}$$
- From the specics of the system, we can tell if **there is motion that contributes to the motional EMF** 
    - Note, we could also compute it, but we would find that the integral would be 0 


### Eddy Currents
- When there is a magnetic flux that is time varying on a surface with high permeability, there is a current density. 


### Ampère Maxwell Law: 

$$ \nabla \times \mathbf{H} = \mathbf{J} + \frac{\partial \mathbf{D}}{\partial t} \iff \oint_c \mathbf{H} \cdot d \mathbf{l} = I_{enc} + \frac{d}{dt} \int_s \mathbf{D} \cdot d \mathbf{S}$$
- The last term is called the displacement current density 
- In integral form it is the total displacement current through S 

#### Displacement Current Density
- We recall that $\mathbf{D} = \varepsilon \mathbf{E}$, so we can rewrite the displacement current density as:
$$\mathbf{J}_d = \frac{\partial \mathbf{D}}{\partial t} = \varepsilon_0 \frac{\partial \mathbf{E}}{\partial t}  + \frac{\partial \mathbf{P}}{\partial t}$$
- Where the second term is the current from the motion of polarization charges


#### Charge Conservation:
- Let us take the divergence of the Ampère Maxwell Law in differential form: 
$$\nabla \cdot (\nabla \times \mathbf{H}) = \nabla \cdot \mathbf{J} + \frac{\partial}{\partial t} \nabla \cdot \mathbf{D} \rightarrow 0  = \nabla \cdot \mathbf{J}+ \frac{\partial \rho_v}{\partial t}$$

# FIN
