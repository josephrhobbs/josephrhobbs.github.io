# Lesson 2: More Particles

~

In the last lesson, we derived the density of states function for a single particle in a 3-dimensional box.  This is an immense step forward in our journey through statistical mechanics.  Unfortunately, we are quite limited by the fact that we often don't deal with single particles.  Often, problems in science and engineering require reasoning about trillions upon trillions of particles, such as a sample of matter composed of atoms.  How can we generalize for \( N \) particles in a box?

## Density of States

Remember the density of states function for a single particle?

\[ \Omega = 4 \sqrt{2} m^{3/2} \pi V \sqrt{E} \]

Let's think about how we can get here again, but with \( N \) particles in a box.  Assuming we still have total energy \( E \) that exists purely in the form of kinetic energy (no potential energy), we can write the phase space relation

\[ E = \frac{1}{2m} (p_{1x}^2 + p_{1y}^2 + p_{1z}^2 + \cdots) \]

and sum the momentum terms over every single particle in the box.  According to our original reasoning, because we have a sum over squared terms, this equation represents a hypersphere in \( 3N \) dimensions with a radius of \( \sqrt{2mE} \).  We can now use this handy equation to calculate the hypervolume contained inside a \( k \)-dimensional ball.  Here, we use the symbol \( \Gamma \) to represent [Euler's gamma function](https://en.wikipedia.org/wiki/Gamma_function).

\[ V = \frac{\pi^{k/2}}{\Gamma(\frac{k}{2} + 1)} R^k \]

Our phase space volume \( \Omega \) can be written using \( k = 3N \) and \( R = \sqrt{2mE} \).  Starting with the definition of the density of states,

\[ \Omega := \frac{\partial}{\partial E} \int_S \, dV \]

we can break up our differential hyper-volume element into \( 6N \) variables... \( 3N \) for the position of \( N \) particles, and \( 3N \) for the momentum of \( N \) particles.

\[ \Omega := \frac{\partial}{\partial E} \int_S \, dp_{1x} dp_{1y} dp_{1z} \cdots dx_1 dy_1 dz_1 \cdots \]

\[ \therefore \Omega = \frac{\partial}{\partial E} V^N \int_S \, dp_{1x} dp_{1y} dp_{1z} \cdots \]

We can now substitute known values and differentiate to obtain a final result.

\[ \begin{align*} \Omega &= \frac{\partial}{\partial E} \frac{(2 \pi)^{3N/2}}{\Gamma(\frac{3N}{2} + 1)} m^{3N/2} V^N E^{3N/2} \\ &= \frac{3N}{2} \frac{(2 \pi m)^{3N/2}}{\Gamma(\frac{3N}{2} + 1)} V^N E^{3N/2 - 1} \end{align*} \]

This is the density of states equation for \( N \) particles in a box!  It can be easily shown that this is equivalent to our original result when \( N = 1 \).