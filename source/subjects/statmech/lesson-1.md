# Lesson 1: How Many States?

~

The universe is filled with large collections of things.  For example, 18 milliliters of water (just over 1 U.S. tablespoon) contains an Avogadro's number of water molecules.  Theoretically, if we understood the behavior of each water molecule exactly, we could fully characterize the properties of the collection of water molecules.  But of course, that's ridiculous... how could we ever measure the position and momentum of trillions and trillions of molecules instantaneously and with precision?  Perhaps we don't really need to make all those measurements... what if we could predict _microscopic_ behavior from _macroscopic_ observations, and then we could make _macroscopic_ predictions from our predicted _microscopic_ behaviors?

Enter statistical mechanics.  Statistical mechanics provides an extremely powerful toolbox for reasoning mathematically and physically about large collections of things.  It meshes seamlessly with the laws of physics to give us a way to think about these large collections of things.

## Big and Small

Before we begin, let's define the terms _microscopic_ and _macroscopic_.

_Microscopic_ behaviors are associated with a system's _microstate_.  The microstate of a system is a complete characterization of every particle in the system.  For example, the microstate of our 18 milliliter sample of water is a list of the position and momentum of every water molecule in the entire sample.

_Macroscopic_ behaviors are associated with a system's _macrostate_.  The macrostate of a system is an overall, high-level depiction of a system, in terms of things that we can observe at a high level.  For example, the macrostate of our 18 milliliter sample of water describes its temperature, density, and volume, among other variables.

Importantly, macrostate variables are _independent_ of a system's precise microstate.  Knowing the temperature of a system tells us some information about _all_ of the particles at once (their mean kinetic energy) but no information at all about any _particular_ particle (its individual kinetic energy).

## Counting States

Let's think about a very simple example to get us warmed up and accustomed to thinking in the terms of statistical mechanics.  Consider a single particle with mass \( m \) in a 2-dimensional square box with side length \( L \).  The microstate of this system consists of four variables: the position of the particle \( (x, y) \) within the box, and the momentum of the particle in both the X and Y directions \( (p_x, p_y) \).  Given these four variables, we can completely characterize the entire system.

What do we know about the macrostate of this system?  One very common macrostate variable is _total energy_.  How much energy is contained in this system?  Because we only have one particle and its only energy is kinetic, we have

\[ \begin{align*} E &= \frac12 m v^2 \\ &= \frac12 m (v_x^2 + v_y^2) \\ &= \frac12 m (\frac{p_x^2}{m^2} + \frac{p_y^2}{m^2}) \\ &= \frac{1}{2m} (p_x^2 + p_y^2) \end{align*} . \]