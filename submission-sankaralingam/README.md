<h1>Project 1: Visualizing Anscombe’s Quartet</h1>
<h2> Ashwin Sankaralingam </h2>


I have completed every Part present and a few bells and whistles. I ll elaborate my experience
and details of the sources.

<h3> Part1 </h3>
The file was successfully loaded and checked. The async function worked properly.

_Source:_ In class tutorial

<h3> Part2 </h3>
I created a function to handle both Part2 as well Part3 and 4. It takes in arguments for width, height,
id where the svg is to be inserted and the transition effect *Whiste* parameter which determines if the transition happens.
The x and y axis are zoomed into the extent as discussed in the class.

_Source:_ In class tutorial

<h3> Part3 </h3>
For plotting the line graph, I called the function I already created and added a boolean argument
which can distinguish scatterplot and line graph. If the argument is set, the path variable along with
the attr of the line will be added to the scatterplot.

For the purpose of sorting, I used the compare call back, which uses the x value of the object to sort and
overrid the sort function for array of objects.

_Source:_  [d3.js tutorial](https://bl.ocks.org/mbostock/3883245)


<h3> Part4 </h3>
For manipulating the 'p' tag in html,I used the mouseover and mousein. The intro to this was given in lecture and
I followed something similar. I had seperate function for hover and mouse click, to differentiate click.

_Source:_ In class tutorial

<h3> Part5 </h3>
For creating multiple graphs, I reduced the width and height of initial svg and it automatically fit 4 onto the
screen. This is a hacky manipulation to re-scale the graph to a new dimension (can also be used to increase the size of graph).


<h2> Bells and Whistles completed </h2>
<h3> Bells : Tooltips </h3>
This is similar to the mouse hover concept, but I had to create a new div and have a seperate css code which mentioned the
positioning to be absolute(so that it is present on the canvas). To get the x,y coordinate, used d3 event function to get the current X,Y of the mouse pointer and offset it so that it would be clearly visible. Updated the text to the point coordinates.

_Source:_  [d3.js mouseEvents](https://bl.ocks.org/mbostock/1087001) for getting the (x,y) of the mouse.

<h3> Whistle : Transition </h3>
Worked on uploading the required dataset. Once the dataset is loaded, I checked if it was the first time data selection.
If it was the first time I would simply display the data. If it was not the first time, I would add transition to the existing circles, path in the svg and transform them to new data points. I had a smooth transition for transformation. I also changed the x,y axis as the range of the domain also changed.

_Source:_  [inspiration](http://bl.ocks.org/enjalot/1429426)

<h3> Whistle : Replication </h3>
Used tableau for replication in similar fashion and the details can be found [here](../data/).
Using Tableau was very easy and it was simple drag and drop, but I did not understand many intricate details of the data
when I used drag-n-drop setting. For example, understanding the ordering data was not possible, as Tableau automatically
joined the points in correct fashion. I feel utilizing d3.js will give us more insights to the corner cases, than Tableau.
But definitely Tableau will be my first choice, if I were to visualize a large database before I start coding in d3.js.
