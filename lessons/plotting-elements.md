# Plotting

## Elements of Plots

- just show a few and ask what looks good, what looks bad

## MatPlotLib

- that old notebook I have is good here

## Publication-Quality Plots

Have you ever seen a journal article or book with a pixelated graph?  It's a pretty cringey mistake to see through into print, and quite avoidable—although sometimes difficult to see on a screen.

Whenever you produce a plot, you must take into account how the plot will be used and represented.  Plots may be designed for use in a variety of scenarios, primarily:

If your plot looks like the defaults, it looks bad.  (There was a decade of grey backgrounds on plots from Excel thanks to defaults that wanted to show off what you could do.)

One problem with coding instead Excel is that it's a lot of work to get things to look the way you want.  Of course, once you've gotten it right, it's trivial to repeat the same style for all of your graphs.


**Form Factors**

1.  Screen (Static)
2.  Screen (Interactive)
3.  Print

**Purposes**

1.  Subjective communication (emotional appeal)
2.  Objective communication (facts and relationships)
3.  Information lookup

Per this schema there are nine different interactions of considerations:

1.  Subjective communication, static screen

2.  Subjective communication, interactive screen

3.  Subjective communication, print

These three together are the _demesne_ of journalism and public relations.  You commonly see these employed in magazines, in Twitter thumbnails, and similar locations optimized for rapid shallow perusal.  Subjective communication is fundamentally a _pitch_.

4.  Objective communication, static screen

5.  Objective communication, interactive screen

6.  Objective communication, print

These three encompass standard scientific plots in journal articles.  (We set aside for the time being the question of how objective, in fact, such plots are.)  Typically the standards of judgment for these should take into account:

- Clarity of primary details of interest
- Conventions of field and venue (such as plot orientation, aspect ratio, units)
- Ink-to-data ratio
- Typeface (sans-serif preferred on-screen, serif in print)

These type of plots are frequently used to make decisions.  I highly recommend Edward Tufte's _The Visual Display of Quantitative Information_ and Jean-luc Doumont's _Trees, Maps, and Theorems:  Effective Communication for Rational Minds_.

7.  Information lookup, static screen

The resolution of plots on screen is frequently not very high, particularly on legacy monitors:  on the order of 72–120 pixels per inch (PPI) on older non-Retina displays and up to 400 PPI or so today.  Downsampling and upsampling frequently occurs, and so the final viewing conditions may vary a fair amount.  Color configuration can also differ a lot across different monitors and observing conditions.

8.  Information lookup, interactive screen

This can be an extremely fruitful pairing, if interactive graphics allow for active querying of data points and automatic display of relationships.  The same caveats about resolution apply.

9.  Information lookup, print

Classically, one of the major purposes of scientific and engineering reference books was to provide tables and plots of data for consultation.  Tables are preferred when several significant figures of precision are required, and when quantity evolution is reasonably representable.  Examples include tables of logarithms, trigonometric functions, and so forth.

Plots are preferred when many quantities are displayed in tandem and only a couple of sigificant figures are necessary.  Examples include graphs of the thermodynamics of steam.

If you produce reference diagrams for print, you should keep in mind that ink colors tend to be rather limited on non-commercial printers and that the gold standard resolution of your plot should be 600 dots per inch (DPI).  (The default output for MatPlotLib looks to be about 100 DPI.)  You should also make sure that your typeface is legible at the sizes and fineness of printing:  serif fonts should produce visible serifs when printed.
