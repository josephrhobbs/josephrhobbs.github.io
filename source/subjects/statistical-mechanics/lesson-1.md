# Lesson 1: How Many States?

~

The universe is filled with large collections of things.  For example, 18 milliliters of water (just over 1 U.S. tablespoon) contains an Avogadro's number of water molecules.  Theoretically, if we understood the behavior of each water molecule exactly, we could fully characterize the properties of the collection of water molecules.  But of course, that's ridiculous... how could we ever measure the position and momentum of trillions and trillions of molecules instantaneously and with precision?  Perhaps we don't really need to make all those measurements... what if we could predict _microscopic_ behavior from _macroscopic_ observations, and then we could make _macroscopic_ predictions from our predicted _microscopic_ behaviors?

Enter statistical mechanics.  Statistical mechanics provides an extremely powerful toolbox for reasoning mathematically and physically about large collections of things.  It meshes seamlessly with the laws of physics to give us a way to think about these large collections of things.

## Big and Small

Before we begin, let's define the terms _microscopic_ and _macroscopic_.

The _microscopic_ behaviors of a system are associated with a system's _microstate_.  The microstate of a system is a complete characterization of every particle in the system.  For example, the microstate of our 18 milliliter sample of water is a list of the position and momentum of every water molecule in the entire sample.

The _macroscopic_ behaviors of a system are associated with a system's _macrostate_.  The macrostate of a system is an overall, high-level depiction of a system, in terms of things that we can observe at a high level.  For example, the macrostate of our 18 milliliter sample of water describes its temperature, density, and volume, among other variables.

Importantly, macrostate variables are _independent_ of a system's precise microstate.  Knowing the temperature of a system tells us some information about _all_ of the particles at once (their mean kinetic energy) but no information at all about any _particular_ particle (its individual kinetic energy).

## Counting States

Let's think about a very simple example to get us warmed up and accustomed to thinking in the terms of statistical mechanics.  Consider a single particle with mass \( m \) in a 3-dimensional cubic box with side length \( L \).  The microstate of this system consists of six variables: the position of the particle \( (x, y, z) \) within the box, and the momentum of the particle in three directions \( (p_x, p_y, p_z) \).  Given these six variables, we can completely characterize the entire system.

What do we know about the macrostate of this system?  One very common macrostate variable is _total energy_.  How much energy is contained in this system?  Because we only have one particle and its only energy is kinetic, we have

\[ \begin{align*} E &= \frac12 m v^2 \\ &= \frac12 m (v_x^2 + v_y^2 + v_z^2) \\ &= \frac12 m (\frac{p_x^2}{m^2} + \frac{p_y^2}{m^2} + \frac{p_z^2}{m^2}) \\ &= \frac{1}{2m} (p_x^2 + p_y^2 + p_z^2) . \end{align*} \]

Another very common macrostate variable is _volume_.  The volume of a cube with side length \( L \) is

\[ V = L^3 . \]

Our next question is quite unusual, but its answer forms the foundation of all statistical mechanics.  For a given macrostate (energy \( E \) and volume \( V \)), how many possible microstates can the system be in?

This is, of course, an impossible question to answer.  There are an uncountably infinite number of possible microstates!  But it turns out to be extraordinarily useful to quantify, in some way, "how many" microstates are available that correspond to a given macrostate.

## Phase Space

To answer this question, we will need to understand the concept of _phase space_.  Consider a six-dimensional space in which every dimension represents a microscopic variable.  This allows us to represent the X, Y, and Z coordinates and X, Y, and Z momenta independently.  This is what we call phase space.  For reasons that will become clear shortly, we'll focus on determining the (hyper)volume of phase space that corresponds to the range of energies between zero and \( E \).  If we allow energies between zero and \( E \) and we fix the volume at \( V \), there will be constraints on which microstates are _accessible_ in this phase space.  Considering only the momenta in a three-dimensional space,

\[ \begin{align*} E &= \frac{1}{2m} (p_x^2 + p_y^2 + p_z^2) \\ 2 m E &= p_x^2 + p_y^2 + p_z^2 \end{align*} \]

we see that \( p_x, p_y, p_z \) must lie inside a ball with radius \( \sqrt{2mE} \).  Considering only the positions in a three-dimensional space,

\[ V = L^3 . \]

Because we can consider momenta and positions independent, we can now write the accessible hypervolume of phase space corresponding to energies between zero and \( E \) as

\[ \int_S \, dp_x \, dp_y \, dp_z \, dx \, dy \, dz = \int_S \, dp_x \, dp_y \, dp_z \, dx \, dy \, dz . \]

## Density of States

We now have an integral over all accessible microstates with energies _between_ zero and \( E \).  However, what we want to do is measure the accessible microstates with energies of _exactly_ \( E \).  It turns out a good way to approach this is differentiating the volume of \( S \) with respect to \( E \).  Conceptually, taking a derivative takes a measurement of the space between \( E \) and \( E + dE \) as \( dE \) gets extremely small, so it's easy to see why this works.  Let's define this result as \( \Omega \).

\[ \Omega := \frac{\partial}{\partial E} \int_S \, dV \]

This result is so important that it has a special name in statistical mechanics... the _density of states_ function.  Though it may have a very strange definition, the ability to calculate it will serve us very well, as we'll see shortly.

## Integrate, Integrate, Integrate!

Let's compute the density of states function \( \Omega \) for our provided particle in a 3-dimensional box.  By the definition of the density of states,

\[ \begin{align*} \Omega &:= \frac{\partial}{\partial E} \int_S \, dV \\ &= \frac{\partial}{\partial E} \int_S \, dp_x \, dp_y \, dp_z \, dx \, dy \, dz \end{align*} \]

Remember when we said that considering the momentum was like integrating over a ball in 3-dimensions?

\[ \Omega = \frac{\partial}{\partial E} \int_S \frac{4}{3} \pi (2mE)^{3/2} \, dx \, dy \, dz \]

We now have an integral only in terms of spatial coordinates.  We recognize this as simply the volume of the box itself.

\[ \Omega = \frac{\partial}{\partial E} \frac{8 \sqrt{2}}{3} \pi (mE)^{3/2} V \]

Last step!  Let's differentiate with respect to total energy.

\[ \Omega = 4 \sqrt{2} m^{3/2} \pi V \sqrt{E} \]

Very interesting!  It would seem that, as we add energy to this system, the number of possible states in which it can exist increases with the square root of energy.  The proportionality factors out front will end up not mattering in the near future... what's critical here is that the density of states is proportional to the square root of energy for one particle.

In review, the density of states function is the _derivative_ with respect to _total energy_ of the volume of phase space contained by \( 0 \le \frac{1}{2m} \sum_i p_i^2 \le E \).  That's a lot to think about!  A non-rigorous but perfectly acceptable way to think about the density of states is as a "number" of accessible microstates, even though the density of states doesn't always evaluate to an integer.  In the next lesson, we'll extend our reasoning here to \( N \) particles in a box!

[Next Lesson](./lesson-1)