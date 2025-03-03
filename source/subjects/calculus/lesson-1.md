# Lesson 1: What is a Derivative?

~

## Definition of the Derivative

The _derivative operator_ \( \frac{d}{dx} \) is defined on the function \( f \) as

\[ \frac{d}{dx} f(x) = \lim_{h \rightarrow 0} \frac{f(x + h) - f(x)}{h} . \]

## Example

Calculate the derivative of the function \( f(x) = x^2 \).

\[ \frac{d}{dx} f(x) = \lim_{h \rightarrow 0} \frac{(x+h)^2 - x^2}{h} \]

\[ \frac{d}{dx} f(x) = \lim_{h \rightarrow 0} \frac{x^2 + 2xh + h^2 - x^2}{h} \]

\[ \frac{d}{dx} f(x) = \lim_{h \rightarrow 0} \frac{2xh + h^2}{h} \]

\[ \therefore \frac{d}{dx} f(x) = \lim_{h \rightarrow 0} \left( 2x + h \right) = 2x . \]