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

Our next question is quite unusual, but its answer forms the foundation of all statistical mechanics.  For a given energy \( E \), how many possible unique microstates can this system be in?

This seems like an impossible question to answer.  The energy can be distributed across the X, Y, and Z momenta in an uncountably infinite number of ways.  Certainly it can't make sense to ask about "how many" unique microstates there are.  But is there any way we can quantify the question we're asking?

Imagine a 3-dimensional coordinate space where X, Y, and Z momenta correspond to the X, Y, and Z directions.  Notice the energy equation that we have above

\[ \begin{align*} E &= \frac{1}{2m} (p_x^2 + p_y^2 + p_z^2) \\ p_x^2 + p_y^2 + p_z^2 = 2 m E \end{align*} \]

is the equation for a sphere with radius \( \sqrt{2mE} \) in this space!  We call this space _phase space_, and it is a powerful tool for relating microstate variables (like momentum) to macrostate variables (like total energy).  We're now a little closer to answering the question... every possible microstate can be represented by a point on this sphere.  Obviously, if we make the sphere bigger by adding more energy (which increases the radius), there are "more points" on the sphere and therefore more possible microstates.

Let's make this mathematically rigorous.  From now on, we'll use the term "number of microstates" very loosely... just remember that we're not _actually_ counting the microstates one at a time, because that's not really possible.  Call the volume of the ball (the volume bounded by the sphere) \( \Omega_E \).  Rigorously, \( \Omega_E \) is the _volume of phase space_ bounded by all possible microstates with energy between zero and \( E \).  We can write \( \Omega_E \) as the volume of the ball with radius \( \sqrt{2mE} \) as mentioned previously.

\[ \begin{align*} \Omega_E &= \frac43 \pi \cdot (\sqrt{2mE})^3 \\ &= \frac{8 \sqrt{2}}{3} \pi m^{3/2} E^{3/2} \end{align*} \]

If you'll remember though, this corresponds to the number of microstates with energies _between_ zero and \( E \).  But we wanted to know the number of microstates corresponding to an energy of exactly \( E \).  Perhaps we can take the derivative of \( \Omega_E \), which would give us the "number of microstates" (again, very loosely) between \( E \) and \( E + dE \) for a very small \( dE \).  We'll call this \( \omega_E \).

\[ \begin{align*} \omega_E &= \frac{d\Omega_E}{dE} \\ &= \frac{8 \sqrt{2}}{3} \pi m^{3/2} \cdot \frac{d}{dE} E^{3/2} \\ &= 4 \pi \sqrt{2} m^{3/2} \sqrt{E} \end{align*} \]

Very interesting!  It would seem that, as we add energy to this system, the number of possible states in which it can exist increases with the square root of energy.  This function \( \omega \) is so important to statistical mechanics that we will give it a special name... the _density of states_ function.