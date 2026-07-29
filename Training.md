
# COMPLETE MATPLOTLIB TRAINING

## Introduction

- A low level graph plotting library in python that serves as a visualization utility.
- It is used to create static, animated and interactive plots in python.
- It is open source and we can use it freely.
- Created by John D. Hunter.

## Installation of Matplotlib

If you have Python and pip already installed on your system, then installation of Matplotlib is very easy.

> Install it using this command:
>
>```bash
>C:\Users\Your Name>pip install matplotlib
>```

## Import Matplotlib

Once Matplotlib is installed, import it in your applications by adding the import module statement.

```python
import matplotlib
```

## Checking Matplotlib Version

The version string is stored under __version__ attribute.

### Example

```python
import matplotlib
print(matplotlib.__version__)
```

***

## Matplotlib Pyplot

The most commonly used module in matplotlib is pyplot.

```python
import matplotlib.pyplot as plt
```

Now the Pyplot package can be referred to as plt.

## Simple One Liner Graph

```python
import matplotlib.pyplot as plt

# x and y are the data points.
x = [1, 2, 3, 4, 5]
y = [10, 20, 30, 40, 50]

# plt.plot(x,y) is used to draw the line.
plt.plot(x,y)

# Parameter 1 is an array containing the points on the x-axis.
# Parameter 2 is an array containing the points on the y-axis.

# plt.show() is used to display the graph.
plt.show()
```

### Output

![One Liner](Assets\1.png)

## Plotting Without Line

To plot only the markers, you can use shortcut string notation parameter 'o', which means 'rings'.

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->
```python
import matplotlib.pyplot as plt

# x and y are the data points.
x = [1, 2, 3, 4, 5]
y = [10, 20, 30, 40, 50]

# plt.plot(x,y) is used to draw the line.
plt.plot(x,y, 'o')  # Note here: 'o' is added right after x and y

plt.show()
```
<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![only markers](Assets\2.png)

***

## Multiple lines in one graph

We can plot more than one line on the same graph to compare multiple datasets.

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt 
x  = [1, 2, 3, 4, 5]
y1 = [10, 20, 30, 40, 50]
y2 = [50, 40, 30, 20, 10]
y3 = [15, 25, 35, 45, 55]
y4 = [17, 83, 83, 66, 98]
plt.plot(x, y1)
plt.plot(x, y2)
plt.plot(x, y3)
plt.plot(x , y4)
plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->
![Multiple Lines](Assets\3.png)

***

## Matplotlib Markers

You can use the keyword argument marker to emphasize each point with a specified marker:
<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt
x  = [1, 2, 3, 4, 5]
y1 = [10, 20, 30, 40, 50]
plt.plot(x, y1 , marker = 'o')
plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->
![Marker](Assets\4.png)

## Marker Reference

You can choose any of these markers:

| Shape | Markers | Description |
| :---: | :---: | :--- |
| Circles | 'o' | Circle |
| Stars | '*' | Star |
| Points | '.' ',' | Point, Pixel |
| X shapes | 'x' 'X' | X, X (filled) |
| Plus | '+' 'P' | Plus, Plus (filled) |
| Squares | 's' | Square |
| Diamonds | 'D' 'd' | Diamond, Diamond (thin) |
| Triangles | 'v' '^' '<' '>' '1' '2' '3' '4' | All triangle variants |
| Others | 'p' 'H' 'h' '_' | Pentagon, Hexagon, Hline |

## Format Strings fmt

You can also use the shortcut string notation parameter to specify the marker.

This parameter is also called fmt, and is written with this syntax:

`
marker|line|color
`

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

y = [3, 8, 1, 10]

plt.plot(y, 'o:r')      
plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->
![Marker](Assets\5.png)

The marker value can be anything from the Marker Reference above.

The line value can be one of the following:

| Line Syntax | Description         |
| :---------: | :----------:        |
| `'-'`       | Solid line          |
| `':'`       | Dotted line         |
| `'--'`      | Dashed line         |
| `'-.'`      | Dashed/dotted line  |

__Note:__ If you leave out the line value in the fmt parameter, no line will be plotted.

The short color value can be one of the following:

## Color Reference

| Color Syntax | 'r' | 'g' | 'b' | 'c' | 'm' | 'y' | 'k' | 'w' |
| :----------: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| Description | Red | Green | Blue | Cyan | Magenta | Yellow | Black | White |

## Marker Size

You can use the keyword argument markersize or the shorter version ms, to set the size of the markers:

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt
x  = [1, 2, 3, 4, 5]
y1 = [10, 20, 30, 40, 50]
plt.plot(x, y1 , marker = 'o', markersize = 20)
plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->
![Marker](Assets\6.png)

## Marker Edge Color

You can use the keyword argument markeredgecolor or the shorter mec to set the color of the edge of the markers:

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt
x  = [1, 2, 3, 4, 5]
y1 = [10, 20, 30, 40, 50]
plt.plot(x, y1 , marker = 'o', 
         markeredgecolor = 'red', markersize = 20)
plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->
![Marker](Assets\7.png)

## Marker Face Color

You can use the keyword argument markerfacecolor or the shorter mfc to set the color inside the edge of the markers:

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt
x  = [1, 2, 3, 4, 5]
y1 = [10, 20, 30, 40, 50]
plt.plot(x, y1 , marker = 'o', 
         markeredgecolor = 'red', 
         markerfacecolor = 'yellow', 
         markersize = 20)
plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->
![Marker](Assets\8.png)

[colors]: https://www.w3schools.com/colors/colors_names.asp

For more color details [visit][colors]

***

## Matplotlib Legends

- You can add a legend to the plot to identify different lines and bars etc.
- label: used inside plot() to name each line
- plt.legend(): display the legend on the plot

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

x  = [80, 85, 90, 95, 100]
y1 = [640, 390, 60, 770, 980]
y2 = [370, 345, 410, 490, 530]

plt.title("Sales Comparison")
plt.xlabel("Products")
plt.ylabel("Sales")

plt.plot(x, y1,color = 'green' ,marker = 'o'
         , mfc='red', mec = 'yellow', 
         label = 'Product A')
plt.plot(x, y2, color = 'blue',marker = 'o'
         , mfc='red', mec = 'yellow',
         label = 'Product B')
plt.legend()
plt.show()
```
<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->
![Legend](Assets\17.png)

## Legend Position Options

| __VALUE__ | __POSITION__ | __VALUE__ | __POSITION__ |
| :-----: | :--------: | :-----: | :--------: |
| 'best' | Default | 'upper right' | Top right |
| 'upper left' | Top left | 'lower left' | Bottom left |
| 'lower right' | Bottom right | 'center right' | Middle right |
| 'center left' | Middle left | 'center' | Center of plot |

***

## Matplotlib Line

You can use the keyword argument linestyle, or shorter ls, to change the style of the plotted line:

| Style | 'solid' (default) | 'dotted' | 'dashed' | 'dashdot' | 'None' |
| :----: | :---------------: | :------: | :------: | :-------: | :----: |
| Or | `'-'` | `':'` | `'--'` | `'-.'` | `''` or `' '` |

## Dotted Line

```python
import matplotlib.pyplot as plt
x  = [1, 2, 3, 4, 5]
y1 = [10, 20, 30, 40, 50]

plt.plot(x, y1 , marker = 'o',
         markeredgecolor = 'red',
         markerfacecolor = 'yellow',
         markersize = 12,
         linestyle =":",
         label= 'Dotted line',
         color = 'pink',
         linewidth = 2)

plt.legend()
plt.show()
```
<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![Dotted line](Assets\9.png)

## Solid Line

```python
import matplotlib.pyplot as plt
x  = [1, 2, 3, 4, 5]
y1 = [10, 20, 30, 40, 50]

plt.plot(x, y1 , marker = 'o',
         markeredgecolor = 'red',
         markerfacecolor = 'yellow',
         markersize = 12,
         linestyle ="-",            # controls the style of line
         label= 'Solid line',       # sets the color of line
         color = 'black',           # sets the thickness of line
         linewidth = 2)

plt.legend()                        # Show Legend
plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![Solid line](Assets\10.png)

## Dashed Line

```python
import matplotlib.pyplot as plt
x  = [1, 2, 3, 4, 5]
y1 = [10, 20, 30, 40, 50]

plt.plot(x, y1 , marker = 'o',
         markeredgecolor = 'red',
         markerfacecolor = 'yellow',
         markersize = 12,
         linestyle ="--",           # controls the style of line
         label= 'Dashed line',
         color = 'black',           # sets the color of line
         linewidth = 2)             # sets the thickness of line

plt.legend()                        # Show Legend
plt.show()
```
<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![Dashed line](Assets\11.png)

## Dash-Dot Line

```python
import matplotlib.pyplot as plt
x  = [1, 2, 3, 4, 5]
y1 = [10, 20, 30, 40, 50]

plt.plot(x, y1 , marker = 'o',
         markeredgecolor = 'red',
         markerfacecolor = 'yellow',
         markersize = 12,
         linestyle ="-.",        # controls the style of line
         label= 'Dash-Dot line',
         color = 'black',        # sets the color of line
         linewidth = 2)          # sets the thickness of line

plt.legend()                     # Show Legend
plt.show()
```
<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![Dash-Dot line](Assets\12.png)

***

## Matplotlib Labels and Title

- With Pyplot, you can use the xlabel() and ylabel() functions to set a label for the x- and y-axis.
- With Pyplot, you can use the title() function to set a title for the plot.

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

x = [80, 85, 90, 95, 100, 105, 110, 115, 120, 125]
y = [240, 250, 260, 270, 280, 290, 300, 310, 320, 330]

plt.plot(x, y, marker = 'o', markersize = 7,
        markerfacecolor = 'yellow',
        markeredgecolor= 'red')

plt.title("Average Pulse Calorie Burnage")
plt.xlabel("Pulse")
plt.ylabel("Calorie")

plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![X, Y labels](Assets\13.png)

## Set Font Properties for Title and Labels

You can use the fontdict parameter in xlabel(), ylabel(), and title() to set font properties for the title and labels.

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

x = [80, 85, 90, 95, 100, 105, 110, 115, 120, 125]
y = [240, 250, 260, 270, 280, 290, 300, 310, 320, 330]

font1 = {'family':'oswald','color':'green','size':20}
font2 = {'family':'Times New Roman','color':'red','size':15}

plt.title("Average Pulse Calorie Burnage", fontdict = font1)
plt.xlabel("Average Pulse", fontdict = font2)
plt.ylabel("Calorie Burnage", fontdict = font2)

plt.plot(x, y, marker = 'o', mfc='red', mec = 'yellow')
plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![Font Properties for Title and Labels](Assets\14.png)

## Position the Title

- You can use the loc parameter in title() to position the title.
- Legal values are: 'left', 'right', and 'center'. Default value is 'center'.

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->
```python
import matplotlib.pyplot as plt

x = [80, 85, 90, 95, 100, 105, 110, 115, 120, 125]
y = [240, 250, 260, 270, 280, 290, 300, 310, 320, 330]

font1 = {'family':'oswald','color':'green','size':20}
font2 = {'family':'Times New Roman','color':'red','size':15}

plt.title("Sports Watch Data", fontdict = font1, loc = 'right')
plt.xlabel("Average Pulse", fontdict = font2)
plt.ylabel("Calorie Burnage", fontdict = font2)

plt.plot(x, y, marker = 'o', mfc='red', mec = 'yellow')
plt.show()
```
<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![Position the title](Assets\15.png)

***

## Matplotlib Adding Grid Lines

- You can add grid line With Pyplot, to make it easier to read the values.
- you can use the grid() function to add grid lines to the plot.
- Grid lines are very useful When you want to match values on both axes.

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

x = [80, 85, 90, 95, 100, 105, 110, 115, 120, 125]
y = [240, 250, 260, 270, 280, 290, 300, 310, 320, 330]

font1 = {'family':'oswald','color':'green','size':20}
font2 = {'family':'Times New Roman','color':'red','size':15}

plt.title("Average Pulse Calorie Burnage", fontdict = font1, loc = 'center')
plt.xlabel("Average Pulse", fontdict = font2)
plt.ylabel("Calorie Burnage", fontdict = font2)

plt.plot(x, y, marker = 'o', mfc='red', mec = 'yellow')
plt.grid(alpha = 0.1, linestyle = '--', color = 'gray', linewidth = 0.7)

# alpha = 1 (solid grid) and alpha = 0(invisible)

plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![Grid](Assets\16.png)

***

## Matplotlib Scatter

- You can create scatter plot to show relationship between two continuous variables.
- With Pyplot, you can use the scatter() function to draw a scatter plot.
- The scatter() function plots one dot for each observation. It needs two arrays of the same length, one for the values of the x-axis, and one for values on the y-axis.
  
<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt 

# Sample Data
x = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
y = [2, 4, 5, 4, 7, 8, 7, 9, 9, 11]

# Scatter Plot
plt.scatter( x , y, color = 'purple', marker = 'o', s = 80)
# You can change the size of the dots with the s argument.

plt.title('Scatter Plot Example')
plt.xlabel('X Values')
plt.ylabel('Y Values')
plt.grid(alpha = 0.7, linestyle = '--')
plt.show()
```
<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![Scatter Plot](Assets\18.png)

## Color Each Dot

You can even set a specific color for each dot by using an array of colors as value for the c argument.

__Note:__ You cannot use the color argument for this, only the c argument.

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

# Sample Data
x = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
y = [2, 4, 5, 4, 7, 8, 7, 9, 9, 11]

colors = ["red","green","blue","yellow",
        "pink","black","orange","purple",
        "beige","brown"]

# Scatter Plot
plt.scatter( x , y, c = colors, marker = 'o', s = 80)
plt.title('Scatter Plot Example')
plt.xlabel('X Values')
plt.ylabel('Y Values')
plt.grid(alpha = 0.7, linestyle = '--')
plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![color dots](Assets\19.png)

## Size of dots

- You can change the size of the dots with the s argument.
- Just like colors, make sure the array for sizes has the same length as the arrays for the x- and y-axis.

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

# Sample Data
x = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
y = [2, 4, 5, 4, 7, 8, 7, 9, 9, 11]

colors = ["red","green","blue","yellow","pink",
        "black","orange","purple","beige","brown"]

sizes = [19, 50, 70, 100, 150, 125, 200, 400, 350, 240]

# Scatter Plot
plt.scatter( x , y, c = colors, marker = 'o', s = sizes)
plt.title('Color Each Dot')
plt.xlabel('X Values')
plt.ylabel('Y Values')
plt.grid(alpha = 0.7, linestyle = '--')
plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![Size dots](Assets\20.png)

## Alpha

You can adjust the transparency of the dots with the alpha argument.

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

# Sample Data
x = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
y = [2, 4, 5, 4, 7, 8, 7, 9, 9, 11]

colors = ["red","green","blue","yellow","pink",
        "black","orange","purple","beige","brown"]

sizes = [19, 50, 70, 100, 150, 125, 200, 400, 350, 240]

# Scatter Plot
plt.scatter( x , y, c = colors, marker = 'o',
            s = sizes , alpha = 0.5)

plt.title('alpha = Transperancy')
plt.xlabel('X Values')
plt.ylabel('Y Values')
plt.grid(alpha = 0.7, linestyle = '--')
plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![alpha](Assets\21.png)

***

## Matplotlib Bars

Bar charts are best for comparing values across different categories.

### Vertical Bar Chart

You can create vertical bar charts using plt.bar().

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

categories = ['Jan', 'Feb', 'Mar', 'Apr', 'May']
sales = [20, 35, 30, 45, 40]

plt.bar(categories, sales, color = 'skyblue',
        edgecolor = 'black', width = 0.7)

plt.title('Monthly Sales Bar chart')
plt.xlabel('Month')
plt.ylabel('Sales(in 1000s)')
plt.grid(axis = 'y' , linestyle = '--', alpha = 0.9)    # horizontal only
plt.grid(axis = 'x', visible = False)  # force vertical off

plt.show()
```

## Explanation

- color: sets the fill color of bar
- edgecolor: gives border colors to bars
- width: controls the width of bars
- grid(axis = 'y'): horizontal grid only
- grid(axis = 'x', visible = False): forces vertical grid off

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![vertical bar](Assets\22.png)

### Horizontal Bar Chart

You can create horizontal bar charts using plt.barh().

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

products = ['Laptop', 'Mobile', 'Smartwatch', 'Tablet']
sales = [550, 750, 300, 450]

plt.barh(products, sales, color = 'lightgreen',
        edgecolor = 'black', height = 0.4)

plt.title('Product Sales (Horizontal)')
plt.xlabel('Sales(in units)')
plt.ylabel('Products')
plt.grid(axis = 'x' , linestyle = '--', alpha = 0.9)    # vertical only
plt.grid(axis = 'y', visible = False)  # force horizontal off

plt.show()
```
<!-- markdownlint-disable MD024 -->
## Explanation
<!-- markdownlint-enable MD024 -->
- For horizontal bars, use height instead of width.
- grid(axis = 'x'): vertical grid only
- grid(axis = 'x', visible = False): forces horizontal grid off

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![horizontal bar](Assets\23.png)

***

## Matplotlib Histograms

- A histogram is a graph showing frequency distributions.
- You can create histogram to show the distribution of a continuous data.
- It is a graph showing the number of observations within each given interval.

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->
 Say you ask for the height of 250 people, you might end up with a histogram like this:

![example](Assets\24.png)

You can read from the histogram that there are approximately:

- 2 people from 140 to 145cm
- 5 people from 145 to 150cm
- 15 people from 151 to 156cm
- 31 people from 157 to 162cm
- 46 people from 163 to 168cm
- 53 people from 168 to 173cm
- 45 people from 173 to 178cm
- 28 people from 179 to 184cm
- 21 people from 185 to 190cm
- 4 people from 190 to 195cm

## Create Histogram

- Use the hist() function to create histograms.
- The hist() function will use an array of numbers to create a histogram.

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import numpy as np
import matplotlib.pyplot as plt

# Generate some random data
np.random.seed(0)   # for reproducibility
data = np.random.normal(loc=50, scale=10, size=1000)

# plot-histogram
plt.hist(data, bins=15, color='lightgreen', edgecolor='black')

# Titles and Labels
plt.title('Normal Distribution: mean=50, std=10')
plt.xlabel('Values')
plt.ylabel('Frequency')

# Horizontal grid only
plt.grid(axis = 'y', linestyle = '--', alpha = 0.7)
plt.grid(axis = 'x', visible=False)
plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![histogram](Assets\25.png)
<!-- markdownlint-disable MD024 -->
## Explanation
<!-- markdownlint-enable MD024 -->
`data = np.random.normal(loc = 50, scale = 10, size = 1000)`

__Breaking it down:__

| Parameter | What it means | Your value |
| :-------- | :------------ | :--------: |
| `loc` | The mean/average of the distribution. Center of the bell curve | 50 |
| `scale` | The standard deviation. Controls how spread out the data is | 10 |
| `size` | How many random numbers to generate | 1000 |
<!-- markdownlint-disable MD024 -->

***

## Matplotlib Pie Charts

- Pie-charts are best used when you want to show the percentage contribution of categories in whole.
- You can create pie-charts using plt.pie().

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

labels = ['Phthon', 'Excel', 'SQL', 'Power Bi', 'Other']
sizes = [35, 25, 20, 15, 5]
colors = ['#4CAF50', '#2196F3', '#FFC107', '#9C27B0', '#FF5722']
plt.pie(sizes, labels = labels, colors = colors,
         autopct= '%1.1f%%', startangle=90,
         shadow=True, explode = (0, 0, 0.1, 0, 0))

plt.title('Skills Distribution')
plt.axis('equal')   # equal aspect ratio ensures circle shape
plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->

![pie-chart](Assets\26.png)
<!-- markdownlint-disable MD024 -->
## Explanation
<!-- markdownlint-enable MD024 -->
- labels: Names shown for each slice.
- sizes: Values for each category.
- colors: Colors for the slices.
- autopct: Show percentage on each slice.
- startangle: Sets the starting angle of pie chart or rotates the pie-chart.
- shadow: Adds a shadow effect to the pie-chart.
- explode: Separates (explodes) the slice(s). It is used to highlight important slice(s).
- axis('equal'): Ensures pie-chart is drawn as a circle (not oval).

***

## DONUT-CHART

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

labels = ['Phthon', 'Excel', 'SQL', 'Power Bi', 'Other']
sizes = [35, 25, 20, 15, 5]
plt.pie(sizes, labels = labels, wedgeprops={'width': 0.6},
         autopct= '%1.1f%%')

plt.title('Skills Distribution')
# plt.axis('equal')   # equal aspect ratio ensures circle shape
plt.show()
```
<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->
![Donut-chart](Assets\27.png)

## Legend in Pie-Charts

To add a list of explanation for each slice, use the legend() function:

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

y = [35, 25, 25, 15]
mylabels = ["Apples", "Bananas", "Cherries", "Dates"]

plt.pie(y, labels = mylabels)
plt.legend()
plt.show() 
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->
![Legend in Pie-chart](Assets\28.png)

## Legend With Header

To add a header to the legend, add the title parameter to the legend function.

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

y = [35, 25, 25, 15]
mylabels = ["Apples", "Bananas", "Cherries", "Dates"]

plt.pie(y, labels = mylabels)
plt.legend(title = "Four Fruits:")
plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->
![Legend in Pie-chart](Assets\29.png)

## When to use Pie-Charts

- When you want to show parts of a whole.
- When total number of categories are small (preferably less than 6 or 7).
- Applications: Market share, Budget allocation, Survey results.

***

## Matplotlib Figure Size

You can change the size of entire figure (width, height) using figsize parameter in plt.figure().

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

y = [35, 25, 25, 15]
mylabels = ["Apples", "Bananas", "Cherries", "Dates"]
plt.figure( figsize=(4,3))      # Sets size of figure in inches
plt.pie(y, labels = mylabels)
plt.show()    
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->
![Figure Size](Assets\30.png)

***

## Matplotlib Subplots

- You can create multiple plots in a single figure using subplots.
- It is very useful for comparing different data side by side.
- You can combine Line, Bar, Scatter and Histogram in subplots.
- Always use tight_layout() for a neat look.
  
## Subplot Syntax

`plt.subplot(nrows, ncols, index)`

- nrows = No. of rows
- ncols = No. of columns
- index = Position of the plot ( start from 1)

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

# Data for plots
x  = [1, 2, 3, 4, 5]
y1 = [10, 20, 30, 40, 50]
y2 = [50, 40, 30, 20, 10]
y3 = [5, 10, 15, 20, 25]

# Create Subplots ( 2rows, 2 columns)
plt.subplot(2,2,1)
plt.plot(x, y1, color = 'blue', marker = 'o')
plt.title('Plot 1')
plt.xlabel('X')
plt.ylabel('Y')

plt.subplot(2,2,2)
plt.plot(x, y2, color = 'red', marker = 's')
plt.title('Plot 2')
plt.xlabel('X')
plt.ylabel('Y')

plt.subplot(2,2,3)
plt.plot(x, y3, color = 'green', marker = '*')
plt.title('Plot 3')
plt.xlabel('X')
plt.ylabel('Y')

plt.subplot(2,2,4)
plt.bar(x, y3, color = 'orange')
plt.title('Plot 4 (Bar-Chart)')
plt.xlabel('X')
plt.ylabel('Y')


plt.tight_layout()  # adjusts spacing b/w plots automatically
plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->
![subplots](Assets\31.png)

## Subplots (OBJECT ORIENTED)

plt.subplots() : Object oriented way to create subplots

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 2*np.pi, 100)
y1 = np.sin(x)
y2 = np.cos(x)
y3 = np.tan(x) / 3
y4 = np.sqrt(x)

# Create figure and 2x2 subplots
fig, axes = plt.subplots(2, 2, figsize=(10, 7))

axes[0, 0].plot(x, y1, color='blue')    # first row, first column
axes[0, 0].set_title('sin(x)')
axes[0, 0].set_ylabel('y')
axes[0, 0].grid(True, linestyle='--', alpha=0.6)

axes[0, 1].plot(x, y2, color='red')     # first row, second column
axes[0, 1].set_title('cos(x)')
axes[0, 1].grid(True, linestyle='--', alpha=0.6)

axes[1, 0].plot(x, y3, color='green')   # second row, first column
axes[1, 0].set_title('tan(x)/3')
axes[1, 0].set_ylabel('y')
axes[1, 0].grid(True, linestyle='--', alpha=0.6)

axes[1, 1].plot(x, y4, color='purple')  # second row, second column
axes[1, 1].set_title('sqrt(x)')
axes[1, 1].grid(True, linestyle='--', alpha=0.6)

fig.suptitle('Multiple Plots using Subplots', fontsize=14)
fig.tight_layout(rect=[0, 0, 1, 0.95]) # adjust layout
plt.show()
```

<!-- markdownlint-disable MD024 -->
### Output
<!-- markdownlint-enable MD024 -->
![subplots](Assets\32.png)

## Important Notes

- Indices starts from 0. Example: axes[0,1] --> first row, second column.
- Use suptitle() for main title of the entire figure.
- You can customize each subplot individually.

***

## Save Figure

You can save your plot as an image file using plt.savefig().

<!-- markdownlint-disable MD024 -->
### Example
<!-- markdownlint-enable MD024 -->

```python
import matplotlib.pyplot as plt

# x and y are the data points.
x = [1, 2, 3, 4, 5]
y = [10, 20, 30, 40, 50]

# plt.plot(x,y) is used to draw the line.
plt.plot(x,y)
plt.savefig('Test.png', dpi = 300, bbox_inches='tight')
plt.show()

# File saved as 'Test.png' in the current directory
```

<!-- markdownlint-disable MD024 -->
## Explanation
<!-- markdownlint-enable MD024 -->
- plt.savefig('file_name.png') --> Saves the current figure in the current working directory.
- dpi = 300 --> Sets high resolution ( dots per inch)
- Higher dpi --> Better quality
- bbox_inches='tight' --> Removes extra white spaces

***

## Common File Formats
<!-- markdownlint-enable MD024 -->
- PNG --> Good for presentation
- JPG --> Good for web (smaller size)
- PDF --> Best for Documents ( vector format)
- SVG --> Scalable vector graphics

***
__Prepared By:__ Faooq Hassnain Sheikh
