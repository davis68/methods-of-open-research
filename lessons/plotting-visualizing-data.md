# Principles of Visualizing Data

##  Objectives
- Articulate a model of building effective plots.
- Distinguish types of plots and their utility (particularly print v. web products).
- Visualize unstructured and discrete data.

##  Software

You can build useful plots and data visualizations using:

- Microsoft Excel or another spreadsheet program
- R/`ggplot`
- Python/MatPlotLib, `plotnine`, `ggplot2`, and others
- Javascript/`d3.js`
- [Veusz](https://veusz.github.io/)

##  Readings
- [Jean-luc Doumont, _Trees, Maps, and Theorems_](https://www.principiae.be/book/)
- [Edward Tufte, _The Visual Display of Quantitative Information_](https://www.edwardtufte.com/tufte/books_vdqi)
- [Leland Wilkinson, _The Grammar of Graphics_](https://link.springer.com/book/10.1007\%2F0-387-28695-0)

##  Building Effective Plots

For many applications, tabular data are preferred as they allow fine-grained resolution of differences between values.  They are also particularly useful as lookup tables, such as when calculating downstream quantities.

The trouble with tabular data are that they can conceal dramatic differences in trend.

Consider, for instance, the following four data sets.

|   I  |       |  II  |      | III  |       |  IV  |       |
|------|-------|------|------|------|-------|------|-------|
|  $x$ |  $y$  | $x$  |  $y$ |  $x$ |  $y$  |  $x$ |  $y$  |
| 10.0 |  8.04 | 10.0 | 9.14 | 10.0 |  7.46 |  8.0 |  6.58 |
|  8.0 |  6.95 |  8.0 | 8.14 |  8.0 |  6.77 |  8.0 |  5.76 |
| 13.0 |  7.58 | 13.0 | 8.74 | 13.0 | 12.74 |  8.0 |  7.71 |
|  9.0 |  8.81 |  9.0 | 8.77 |  9.0 |  7.11 |  8.0 |  8.84 |
| 11.0 |  8.33 | 11.0 | 9.26 | 11.0 |  7.81 |  8.0 |  8.47 |
| 14.0 |  9.96 | 14.0 | 8.10 | 14.0 |  8.84 |  8.0 |  7.04 |
|  6.0 |  7.24 |  6.0 | 6.13 |  6.0 |  6.08 |  8.0 |  5.25 |
|  4.0 |  4.26 |  4.0 | 3.10 |  4.0 |  5.39 | 19.0 | 12.50 |
| 12.0 | 10.84 | 12.0 | 9.13 | 12.0 |  8.15 |  8.0 |  5.56 |
|  7.0 |  4.82 |  7.0 | 7.26 |  7.0 |  6.42 |  8.0 |  7.91 |
|  5.0 |  5.68 |  5.0 | 4.74 |  5.0 |  5.73 |  8.0 |  6.89 |

Let's use Pandas or R to quickly calculate their respective basic data statistics:


```python
x1 = [10, 8, 13, 9, 11, 14, 6, 4, 12, 7, 5]
y1 = [8.04, 6.95, 7.58, 8.81, 8.33, 9.96, 7.24, 4.26, 10.84, 4.82, 5.68]

x2 = [10, 8, 13, 9, 11, 14, 6, 4, 12, 7, 5]
y2 = [9.14, 8.14, 8.74, 8.77, 9.26, 8.10, 6.13, 3.10, 9.13, 7.26, 4.74]

x3 = [10, 8, 13, 9, 11, 14, 6, 4, 12, 7, 5]
y3 = [7.46, 6.77, 12.74, 7.11, 7.81, 8.84, 6.08, 5.39, 8.15, 6.42, 5.73]

x4 = [8, 8, 8, 8, 8, 8, 8, 19, 8, 8, 8]
y4 = [6.58, 5.76, 7.71, 8.84, 8.47, 7.04, 5.25, 12.50, 5.56, 7.91, 6.89]
```


```python
import pandas as pd

df1 = pd.DataFrame(zip(x1, y1), columns=('x','y'))
df2 = pd.DataFrame(zip(x2, y2), columns=('x','y'))
df3 = pd.DataFrame(zip(x3, y3), columns=('x','y'))
df4 = pd.DataFrame(zip(x4, y4), columns=('x','y'))
```


```python
df1.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>x</th>
      <th>y</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>11.000000</td>
      <td>11.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>9.000000</td>
      <td>7.500909</td>
    </tr>
    <tr>
      <th>std</th>
      <td>3.316625</td>
      <td>2.031568</td>
    </tr>
    <tr>
      <th>min</th>
      <td>4.000000</td>
      <td>4.260000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>6.500000</td>
      <td>6.315000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>9.000000</td>
      <td>7.580000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>11.500000</td>
      <td>8.570000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>14.000000</td>
      <td>10.840000</td>
    </tr>
  </tbody>
</table>
</div>




```python
df2.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>x</th>
      <th>y</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>11.000000</td>
      <td>11.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>9.000000</td>
      <td>7.500909</td>
    </tr>
    <tr>
      <th>std</th>
      <td>3.316625</td>
      <td>2.031657</td>
    </tr>
    <tr>
      <th>min</th>
      <td>4.000000</td>
      <td>3.100000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>6.500000</td>
      <td>6.695000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>9.000000</td>
      <td>8.140000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>11.500000</td>
      <td>8.950000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>14.000000</td>
      <td>9.260000</td>
    </tr>
  </tbody>
</table>
</div>




```python
df3.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>x</th>
      <th>y</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>11.000000</td>
      <td>11.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>9.000000</td>
      <td>7.500000</td>
    </tr>
    <tr>
      <th>std</th>
      <td>3.316625</td>
      <td>2.030424</td>
    </tr>
    <tr>
      <th>min</th>
      <td>4.000000</td>
      <td>5.390000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>6.500000</td>
      <td>6.250000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>9.000000</td>
      <td>7.110000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>11.500000</td>
      <td>7.980000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>14.000000</td>
      <td>12.740000</td>
    </tr>
  </tbody>
</table>
</div>




```python
df4.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>x</th>
      <th>y</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>11.000000</td>
      <td>11.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>9.000000</td>
      <td>7.500909</td>
    </tr>
    <tr>
      <th>std</th>
      <td>3.316625</td>
      <td>2.030579</td>
    </tr>
    <tr>
      <th>min</th>
      <td>8.000000</td>
      <td>5.250000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>8.000000</td>
      <td>6.170000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>8.000000</td>
      <td>7.040000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>8.000000</td>
      <td>8.190000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>19.000000</td>
      <td>12.500000</td>
    </tr>
  </tbody>
</table>
</div>



All four data sets are statistically identical with respect to the standard tests.  Let's plot them and see what shows up.


```python
import matplotlib.pyplot as plt
import matplotlib as mpl
mpl.rcParams['figure.figsize'] = (8,8)


fig, axes = plt.subplots(2, 2)
axes[0,0].plot(df1['x'], df1['y'], 'ro',)
axes[0,0].set_xlim(0,20)
axes[0,0].set_ylim(0,20)
axes[0,0].set_ylabel(r'$y$')
axes[0,0].set_title('df1')
axes[0,1].plot(df2['x'], df2['y'], 'bo',)
axes[0,1].set_xlim(0,20)
axes[0,1].set_ylim(0,20)
axes[0,1].set_title('df2')
axes[1,0].plot(df3['x'], df3['y'], 'go',)
axes[1,0].set_xlim(0,20)
axes[1,0].set_ylim(0,20)
axes[1,0].set_xlabel(r'$x$')
axes[1,0].set_ylabel(r'$y$')
axes[1,0].set_title('df3')
axes[1,1].plot(df4['x'], df4['y'], 'ko',)
axes[1,1].set_xlim(0,20)
axes[1,1].set_ylim(0,20)
axes[1,1].set_xlabel(r'$x$')
axes[1,1].set_title('df4')

fig.suptitle = 'Anscombe\'s Quartet'

plt.show()
```


![png](output_10_0.png)


What is a plot supposed to accomplish?  Per Tufte2001:

- Show the data
- Induce viewer to think about substance (rather than graphics etc.)
- Avoid distorting what the data have to say
- Present many numbers in a small space
- Make large data sets coherent
- Encourage the eye to compare different pieces of data
- Reveal the data at several levels of detail
- Serve a reasonably clear purpose:  description, exploration, tabulation, or decoration
- Be closely integrated with the statistical and verbal descriptions of a data set

One must also consider the purpose of any particular chart, which typically falls into one of three categories:

1. Storytelling/dramatic impact.
2. Pure information communication (scientific plots).
3. Reference graphic (steam table, etc.) designed to compactly express quantitative information.

Many plots fail to meet these criteria, and some plot types should be avoided altogether.  One of the great misfortunes of computer-based typesetting is that it has become easy to make bad plots, and they abound.  Let's look at what makes plots good, and a few great plots, before seeing what to avoid.

### Examples of Bad Plots

What makes a plot bad?  Failure to meet the criteria above.  In particular, plot designers can either fall in love with their own cleverness, or they can get distracted by all the options like a fast food menu.

Let's examine some bad plots and see if we can decide \*why* they're bad.

![](https://images.squarespace-cdn.com/content/v1/512b3ac1e4b01fa6748fff20/1471309585999-AIE91YHN1IB9CJOH65R2/image-asset.png?format=1000w)

![](https://images.squarespace-cdn.com/content/v1/512b3ac1e4b01fa6748fff20/1472573757109-ZHAP8T29IKJYI3F32WCC/U.S.+Annual+Percent+Change+in+Real+GDP?format=1000w)

- [“Fox Chart Fail”](https://analythical.com/blog/fox-chart-fail)

![](https://images.squarespace-cdn.com/content/v1/512b3ac1e4b01fa6748fff20/1472696019873-ZZNQRV87H9BKB1XV02PC/NBC+Zika+Virus+Chart+Fail?format=750w)

![](http://static3.businessinsider.com/image/50b62b796bb3f7084c00000e-548-411/fox-news-graph-fail.png)

![](http://static2.businessinsider.com/image/50b62bb46bb3f74050000000-644-476/fox-news-graph-fail.png)

![](http://static3.businessinsider.com/image/50b62bf0ecad04d16e000005-590-356/fox-news-graph-fail.jpeg)

![](https://i.imgur.com/sTVYOIH.jpg)

![](https://i.redd.it/qtqh9sfekun41.png)


![](http://static3.businessinsider.com/image/50b62c2669beddc340000005-470-272/fox-news-graph-fail.png)

![](https://raw.githubusercontent.com/davis68/is497/master/IMG_20220308_125105817.jpg)

![](https://raw.githubusercontent.com/davis68/is497/master/IMG_20220308_125045451.jpg)

![](https://raw.githubusercontent.com/davis68/is497/master/IMG_20220308_125055779.jpg)

##  Types of Plots

Functionally, a plot consists of the following elements (per _The Grammar of Graphics_):

1. `data`, a set of data operations that create variables from datasets,
2. `trans`, variable transformations,
3. `frame`, a set of variables, related by operators, that define a space,
4. `scale`, scale transformations,
5. `coord`, a coordinate system,
6. `graph`, graphs and their aesthetic attributes,
7. `guide`, one or more guides (axes, legends, etc.).

Wilkinson develops this into an extremely articulate object-oriented design pattern that underlies libraries like R's `ggplot2` and Python's `ggplot`.  Since we're not composing a graphics library ourselves, we don't need the deep level of sophistication the model affords, but it provides a useful framework for discussing chart specification and composition.

### `data`

Plots render datasets as variables in a spatial frame of reference, but how those variables are selected (from among the many possible) includes scaling the data, selecting or filtering the appropriate values, categorizing and cataloguing divisions, etc.

For instance, in a given plot, the `data` are the actual values underlying the points.

### `trans`

Variable transformations include model-level effects (such as an $R^{2}$ goodness-of-fit line or a spline effect).

### `frame`

The frame describes how the data are construed.  Frequently in a scatter plot this is simply an empty coordinate space, but it can be a 3D plot, a regional or world map, or anything else that governs the spatial layout of the data.

### `scale`

Data across large or fine scales must frequently be scaled by some transformation rule to make them legible.  For instance, a logarithmic transformation shows a wide range of orders of magnitude, while scaling by thousands or millions can simplify aspects of presentation and notation.

### `coord`

Many plots that we see are Cartesian $x$–$y$ plots, but other common formats include polar plots and discrete plots (e.g., bar graphs).

### `graph`

The graph includes the points and lines themselves (the data representation) as well as attributes such as color, marker shape, line format, etc.  Sometimes these include areas or ranges.

More on these in a moment.

### `guide`

Chart guides include visual aids to interpretation:

- axes (including ticks)
- grids
- legends
- labels
- origin
- compass rose

Basic graph types include:

- Good choices:

  - Scatterplot:
  
    ![](https://ia600700.us.archive.org/BookReader/BookReaderImages.php?zip=/7/items/cosmographiaapia00apia/cosmographiaapia00apia_jp2.zip&file=cosmographiaapia00apia_jp2/cosmographiaapia00apia_0060.jp2&id=cosmographiaapia00apia&scale=4&rotate=0)
    
    Peter Apian, _Cosmographia_ (1546).
    
    ![](https://raw.githubusercontent.com/davis68/is497/master/lick.png)
    
    Michael Seldner _et al._, _Lick Catalogue_ (1991)
    
    - When should we use points v. lines?


  - quiverplot (Edmond Halley 1686)
  
    ![](https://raw.githubusercontent.com/davis68/is497/master/halley.png)
  
    Edmond Halley, _An Historical Account of the Trade Winds, and Monsoons, Observable in the Seas Between and Near the Tropicks; With an Attempt to Assign the Phisical (sic) Cause of Said Winds_ (1686)
  
    ![](https://i.stack.imgur.com/PFSzu.png)
    
    Illustration of magnetic field in bipolar coordinate system.
  
  - time-series (Funkhauser 1936 → my chart of Galilean moons, weather summary; monotonic independent variable)
  
    ![](https://raw.githubusercontent.com/davis68/is497/master/funkhouser.png)
    
    Funkhouser's discovery of a tenth-century plot of planetary orbits.
    
    (look at papers)
    
    [D. A. Gurnett _et al._, “Plasma Wave Observations Near Jupiter:  Initial Results from Voyager 2” (1979)](https://www.science.org/doi/10.1126/science.206.4421.987)

    - See also [H. S. Bridge _et al._, “Plasma Observations Near Jupiter:  Initial Results from Voyager 2” (1979)](https://www.science.org/doi/10.1126/science.206.4421.972) for some excellent plots.

- Bad choices:

    - bar charts (Playfair rejects; p. 33)
    
      Their own inventor rejected them; he used it only because he needed to show single-year data when other years were missing.
    
    - pie charts (avoid! → prefer stacked bar charts)
    
      These offer very little information and fail to linearly order information.

- Never choices:

    - area chart (circular or proportional)
    
      ![](https://www.advsofteng.com/images/polararea_g.png)

    - bubble charts
    
      ![](https://desk.zoho.eu/DocsDisplay?zgId=20064576101&mode=inline&blockId=0rgpa324a3c26945c4099866bc7eac1dac5eb)

      These are extremely difficult to interpret; humans are not good at comparing areas, volumes, etc.—and what if it's the radius, not the area?

Dogmatically, most good chart designers prefer to minimize “chart junk” (Tufte's principle of ink-to-data ratio).

Almost all plots should be laid out horizontally and be near a golden-mean ratio, but there is a lot of leeway on this latter point.

- https://matplotlib.org/stable/tutorials/introductory/usage.html

When deciding on data representation, one must consider the salient features to be modeled.  (This requires some early exploratory plotting to figure out how to tell the data's story in the best light.)  For instance, determining factors may include:

- Discrete v. continuous variables ($x$ and $y$)
- Observations v. models
- Data categories (multiple series v. subplots)
- Space/dimension v. time series

Some final rules of thumb:

1. Graphs are not always necessary.  Use them when the qualitative features are too complex to convey verbally.

    Tables should also be considered when exact numerical values are necessary; there is no shame in including both tables and charts esp. in an appendix.

    - [A. S. C. Ehrenberg, “Rudiments of Numeracy” (1981)](http://www.mcrhrdi.gov.in/87fc/week4/Rudiments%20of%20Numeracy%20By%20Ehrenberg.pdf)
2. Never publish a plot without $x$ and $y$ axis labels and units.
3. Avoid excessive chart junk and features offered by your platform “just because they're there.”
4. Be attentive to color issues:  e.g. yellow on white, or colorblindness support (see [CUBEHELIX](https://jiffyclub.github.io/palettable/cubehelix/), for instance).
5. Make sure that a plot is high-resolution, 300 dpi or higher.  Assume it will be printed rather than viewed on a screen.

## Resources on Accessibility

- the colormap notebook
- https://it.wisc.edu/learn/accessible-content-tech/accessible-data-visualizations/
- https://www.usu.edu/math/symanzik/talks/2021_SouthwestMichiganChapter.pdf
