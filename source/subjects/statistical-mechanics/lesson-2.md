# Lesson 2: Another Dimension, Another Dimension

~

In the last lesson, we derived the density of states function for a single particle in a 3-dimensional box.  This is an immense step forward in our journey through statistical mechanics.  Unfortunately, we are quite limited by the fact that we often don't deal with single particles.  Often, problems in science and engineering require reasoning about trillions upon trillions of particles, such as a sample of matter composed of atoms.  How can we generalize for \( N \) particles in a box?

## Density of States

Remember the density of states function?

\[ \omega_E(E) = 4 \pi \sqrt{2} m^{3/2} \sqrt{E} \]

Let's think about how we can get here again, but with N particles in a box.  Assuming we still have total energy \( E \) that exists purely in the form of kinetic energy (no potential energy), we can write the phase space relation

\[ E = \frac{1}{2m} (p_{1x}^2 + p_{1y}^2 + p_{1z}^2 + \cdots) \]

and sum the momentum terms over every single particle in the box.  Our phase space is no longer 3-dimensional... it's now \( 3N \) dimensional.  But our original reasoning still holds... because we have a sum over squared terms, this equation represents a hypersphere in \( 3N \) dimensions with a radius of \( \sqrt{2mE} \).  We can now use this handy equation to calculate the hypervolume contained inside a \( k \)-dimensional sphere.

\[ V = \frac{\pi^{k/2}}{\Gamma(\frac{k}{2} + 1)} R^k \]

Our phase space volume \( \Omega_E \) can be written using \( k = 3N \) and \( R = \sqrt{2mE} \).

\[ \Omega_E = \frac{(2 \pi)^{3N/2}}{\Gamma(\frac{3N}{2} + 1)} m^{3N/2} E^{3N/2} \]

Last step!  Let's take the derivative of this with respect to \( E \) to get our density of states.

\[ \begin{align*} \omega_E &= \frac{d\Omega_E}{dE} \\ &= \frac{3N}{2} \frac{(2 \pi)^{3N/2}}{\Gamma(\frac{3N}{2} + 1)} m^{3N/2} E^{3N/2 - 1} \end{align*} \]

This is the density of states equations for \( N \) particles in a box!  It can be easily shown that this is equivalent to our original result when \( N = 1 \).

