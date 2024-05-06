## Thermal Diffusivity Calculations

For a trial with a time difference of n seconds, find $\Delta t$ by measuring the difference in time between the maxima of each temperature curve, take the average of these values.

Find $\omega = \frac{2 \pi}{T}$, where $T$ is the chosen time difference, e.g. 300 seconds. 

$\Delta \phi = \omega \Delta t$ 

Use the above expression to find the phase difference between the two temperatures
rature curves: 
$$\Delta \phi = \frac{2 \pi}{T} \Delta t =\phi_2(r_2, \omega, m) - \phi_1(r_1 , \omega, m)$$


- Find $\tan \phi$ plug values to find $\phi_2$ and $\phi_1$, since $x = r^2  \omega / m$, we can find $m$ by plugging it into the above equation. 


## Introduction: 
Thermal diffusivity, denoted $m$ (or $\alpha$) is a derived material property, dependent on the thermal conductivity $k$, the density $\rho$, and the specific heat capacity $c_p$ of the material. It is a measure of how quickly heat can diffuse through a material [1]. So if a material has a high thermal diffusivity, $m$, the material will transfer heat quickly. Rubber, as used in this experiment, has a low thermal diffusivity, so it will transfer heat slowly. Rubber is known as a good insulator, and is widely used in industrial applications for seals, gaskets, shock absorbers andfew  electrical insulation around copper wires to name a few [2]. This experiment will allow us to measure the thermal diffusivity of rubber by wrapping a thermometer around a rubber tube with known diameter and measuring the temperature change over time as it is heated and cooled multiple times.



## Matematical Background: 

- The temperature of a material can be described through time through space, within an object by the the equation of thermal diffusion: 
$$\frac{\partial T}{\partial t} = m \nabla^2 T$$

The first term, $\frac{\partial T}{\partial t}$, is the rate of change of temperature with time i.e. how quickly the temperature is changing. $m$ is called the thermal diffusivity and is a property of the material and its dimensions, a higher value of $m$ means that heat diffuses more quickly through the material. The final term $\nabla^2 T$ is called the Laplacian of the temperature and is a measure of how the temperature changes with distance, in cylindrical coordinates, the Laplacian is given by: 
$$\nabla^2 T = \frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial T}{\partial r} \right) + \frac{1}{r^2} \frac{\partial^2 T}{\partial \theta^2} + \frac{\partial^2 T}{\partial z^2}$$ 
- However, in this experiment, we are able to simplify the Laplacian using the assumption that the temperature is only changing in the radial direction: 
$$\nabla^2 T = \frac{1}{r} \frac{\partial}{\partial r} \left( r \frac{\partial T}{\partial r} \right) = \frac{\partial^2 T}{\partial r^2} + \frac{1}{r} \frac{\partial T}{\partial r}$$

Thus, the partial differential equation becomes: 
$$\frac{\partial T}{\partial t} = m \left( \frac{\partial^2 T}{\partial r^2} + \frac{1}{r} \frac{\partial T}{\partial r} \right)$$

- THese simplifications allows the use of the method of separation of variables, where we write the temperature as a function of the radial distance and time: $T(r,t) = R(r)\exp (i \omega t)$, where $\omega$ is the angular frequency of the temperature oscillations. Substituting our "guess" solution into the PDE, we get: 
$$\frac{d^2 R}{dr^2} + \frac{1}{r} \frac{dR}{dr} + \frac{i \omega}{m} R = 0$$
- where the exponential term is $\lambda^2 = i \omega / m$. The differential equation is known as Bessel's Equation of order zero. A solution to this equation is called $J_0$, a Bessel function of order zero. Now if we set $z = \lambda r$  the Bessel Equation becomes: 
$$ J_0(z) = \sum_{n=0}^{\infty} \frac{(-1)^n}{(n!)^2} \left( \frac{z}{2} \right)^{2n} = 1 - \frac{z^2}{2^2} + \frac{z^4}{2^2 4^2} - \frac{z^6}{2^2 4^2 6^2} + \ldots$$ 

However, it is noted that by solving for $\phi$, the phase difference between the two temperatures (boiling water and ice water), we can solve for the thermal diffusivity. The phase of the oscillating temperature can be measured by $\Delta t$, which is the time delay it takes for the inner temperature to reach its maximmum after the outer temeprature has reached its maximum. Thus, the Bessel function can be used to find a function for the phase difference $\phi$ by taking the arctangent of the ratio of two Bessel functions: 
$$\tan ( \phi (x)) = \frac{\frac{x^2}{2} - \frac{x^6}{2^2 4 ^2 6^2}}{1 - \frac{x^4}{2^2 4^2}}$$ 

However, we note that $x^2 = \frac{r^2 \omega}{m}$  in the above expression, where all variables are real and known except for $m$, thus, we can rewrite the expression for tangent as 
$$\tan(\phi(x)) = \tan(\phi(r, \omega, m)) $$ 
- By taking the arctangent of the ratio, we have an expression for the phase difference: 
$$\phi(r, \omega, m) = \arctan \left( \frac{\frac{x^2}{2} - \frac{x^6}{2^2 4 ^2 6^2}}{1 - \frac{x^4}{2^2 4^2}} \right)$$


Finally, applying the fact that the angular frequency is equal to $\omega = 2 \pi / T$, we can express the time delay $\Delta t$ as 
$$ \Delta t = \frac{ \Delta \phi }{\omega} = \frac{\phi_2(r_2, \omega, m) - \phi_1(r_1, \omega, m)}{\omega}$$ 
where $\phi_2$ and $\phi_1$ are the phase differences for the two temperatures, and $r_2$ and $r_1$ are the radii of the rubber cylinder.


## Materials: 
- 2 Thermometers
- Rubber tube with $r_1 = _$ and $r_2 = _$
- 2 cylindrical, glass containers with 1 L capacity
- Hot plate
- Ice 
- Water 
- Clamp and retort stand 
- Scissor lift 
- Stopwatch 
- Calipers 

## Procedure: 

We filled up one of the glass containers with water to around 2/3 of its capacity, we placed it on the hot plate and set it to the "high" setting. It takes around 10 minutes for the water to boil, so in the mean time, we measured in the inner and outer radii of the rubber tube using calipers. We then filled up the second container with 2/3 of its capacity with ice, this may seem like a lot; however, upon adding the water to the ice, a lot of it will melt. We added the water to the ice and stirred it, ensuring that the ice was floating. We adjusted the height of the ice water container using the knob on the scissor to match the height of the boiling water. We adjusted the clamp on the retort stand to hold the thermometer with the rubber in place and ensured that the rubber was submereged in the water, but did not touch the glass bottom. With the second thermometer, we measured the temperatures of the hot and cold water, after the temperatures were around $95^{\circ} C$ and $0^{\circ} C$ respectively, we started our trials. 

### Trials
We took a total of 6 trials with varying periods $T = 60, 90, 120, 150, 225, 300$ seconds. For each distinct trial, we exchanged between the hot and cold baths 5 times (i.e start with hot, then cold, hot, cold, hot, and finally cold). 
Each 10 seconds, we would read out the temperature on the thermometer, changing baths from hot to cold and vice versa every $T$ seconds. The transfer was done simply by lifting the entire retort stand instead of adjusting the clamp. This minimizes the time it takes to transfer the rubber from one bath to the other and ensures that the temperature is read at the same time for each trial.



## Sources of Error
1) Temperature is not uniform throughout the water bath, so the temperature of the outer layer of rubber may not have been constant throughout trials. While convection currents in the water bath help to distribute the heat, there is heat loss or gain to/from the environment, which occurs most along the glass and air boundary. In the case of the hot bath, the bottom of the beaker was the hottest, while the top was the coolest. If the rubber was not placed at the same location each time, there would be inconsistencies in the temperature readings. For example, for the ice water, if the rubber was placed near the sides of the beaker with ice water, it would have been hotter than if it was placed in the center, or near the ice chips. To mitigate this, we could have drawn a mark on at the bottom of each beaker, ensuring that the rubber was placed at the same location each time.

2) The ice water was not perfectly at $0^{\circ} C$. The ice would melt away as the experiment took place, as a result of the heat lost from the hot bath. Although we measured the initial temperature to be $0^{\circ} C$, the temperature would have increased as the ice melted. To mitigate this, we could have better insulated the two baths from each other, perhaps by surrounding the ice bath with styrofoam.

3) The initial temperature of the rubber was not consistent between trials. The range of our initial tempreatures was from $41^{\circ} C$ to $26^{\circ} C$. This would have caused the temperature peaks to reach different values, as more or less heat would have been required to reach the maximum temperature. 

3) The rubber tube was not perfectly cylindrical, in fact it's geometry was skewed to one side.  In equation 2, we simplify the Laplacian by assuming that the temperature only changes in the radial direction since we assume cylindrical symmetry; however, due to the non-cylindrical shape of the rubber, the temperature could have changed in the z-direction as well. In addition, the inner and outer radii $r_1$ and $r_2$ varied along the length of the rubber tube. To mitigate this, we could have measured the radii at multiple points along the rubber tube and taken the average, or we could have used a rubber tube with a more uniform geometry (like the other lab group's). 

4) The rubber tube did not perfectly fit the thermometer. There was a small gap between the bulb of the thermometer and the rubber tube. As such, the measured tempearture of the inner rubber may have reacted to the changes in water baths much more quickly than if the thermometer was perfectly wrapped around the rubber. This would have caused the phase difference between the inner and outer radii to be smaller than it actually was, i.e. the thermal diffusivity would have been overestimated.

5) Human error in measuring thermometer readings at 5 and 10 second intervals. In this case, there are two possible human errors. One stems from the reading of the analog thermometer, and the other comes from the reading of the stopwatch. To avoid human error, in both readings, a video recording of the process could be taken. By analyzing the video, we would have the exact time at which the temperature was read and a better reading of the thermometer. 

6) Instrumental error with the thermometer. The digital thermometer was only accurate to the nearest whole number, so it had an uncertainty of $\pm 0.5^{\circ} C$. This would have caused the temperature peaks to be different, leading to a different phase difference between the two temperatueres, than that which actually occurred. To remedy this, we can can implement a digital thermometer with a higher degree of precision. Also referring to error 4, we could have had a digital thermometer that took values for us at shorter intervals, assuring that we had a more accurate reading of the temperature, and its behaviour with time. 

7) The timing of the trials was not perfect, as the time delay bewteen the transfer of water baths was not exactly $T$ seconds. There is no way to mitigate this error, as there will always be some time where the rubber and thermometer spends time outside of the water, in the air. 










 [1] Lightfoot, R. Byron Bird, Warren E. Stewart, Edwin N. (1960). Transport Phenomena. John Wiley and Sons, Inc. Eq. 8.1-7. ISBN 978-0-471-07392-5.
 [2] https://www.industrial-rubber.com/news/industrial-uses-of-rubber/
