This is a project I embarked on when first learning Java.
I recommend it to new programmers with an interest in mathematics as it is fairly quick to do (2-3 hours) but has a big
payoff in terms of having a cool thing to show off once it's finished.

The Mandlebrot Set en.wikipedia.org/wiki/Mandelbrot_set
is a set of complex numbers c for which f(z) = z^2 + c does not diverge when iterated from zero.

Pretty fractal patterns can be obtained by coloring the parts of the complex plane which diverge after n iterations
in different colors.

FEATURES:

- Pretty Colors:
    I spend most of the time on this project tinkering with the colors to get the patterns to look just so.
    the solution i ended up with can be found in the ColorFetcher Class. to achieve it i used the HSV model of colour.
    with each iteration i make a big jump in Hue, and slowly increase the saturation to produce a nice rainbow effect.

- Concurrency:
    This is one of the first projects in which I introduced concurrency. Calculating the set at high iterations is
    quite processor heavy and so by splitting up the display into n strips and having each of n threads calculate a strip
    we can better utilise multi-CPUs to reduce the time to refresh the image.