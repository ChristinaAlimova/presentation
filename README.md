# transcription  
## (Slide #2 - Introduction)  
CSS Grid Layout, is a two-dimensional grid-based layout system that aims to do nothing less than completely change the way we design grid-based user interfaces. CSS has always been used to lay out our web pages, but it's never done a very good job of it. First we used tables, then floats, positioning and inline-block, but all of these methods were essentially hacks and left out a lot of important functionality (vertical centering, for instance). Flexbox helped out, but it's intended for simpler one-dimensional layouts, not complex two-dimensional ones. Grid is the very first CSS module created specifically to solve the layout problems we've all been hacking our way around for as long as we've been making websites.
***
## (Slide #3 - terminology)  
Before diving into the concepts of Grid it's important to understand the terminology.  
˅  
So The first element  is a grid container. Grid container is the direct parent of all the grid items.  
˅  
Next, it’s a grid item. This element is the direct children of the grid container.  
˅  
Also grid has dividing lines. The dividing lines make up the structure of the grid. They can be either vertical or horizontal and reside on either side of a row or column.  
˅  
Grid track is The space between two adjacent grid lines. You can think of them like the columns or rows of the grid.  
˅  
Another term is a grid cell.  The grid cell is The space between the grid lines. Here is the grid cell line between the grid lines 1 and 2, and the column grid lines 2 and 3.  
˅  
Finally, the last term is grid area. It’s The total space surrounded by four grid lines. A grid area may be comprised of any number of grid cells.  
˅  
Now you can see the whole picture of the above elements. Pay particular attention to the location of items such as grid track row and grid track column. In the following, it is important to understand what are columns and what are rows.  And now we go to the next slide.
***
## (Slide #4 - grid properties)  
Now we will talk about the grid properties.  
˅  
Grid properties are divided into two logical blocks. There are properties for the grid container and   
˅  
Properties for the grid items. Note that the properties are in the form of links, so you can go to the slide you need.
***
## (Slide #5 - properties for the grid container)  
Let's look at the properties for the grid container first.
***
## (Slide #6 - display property)  
The first property is display. Display defines the element as a grid container and establishes a new grid formatting context for its contents. Also display property has several values. It’s grid, inline-grid and subgrid. Often we use grid value. Below Note the syntax of this property.
***
## (Slide #7 - grid-template-columns/grid template-rows)  
Next we look at two properties at once – There are grid-template-columns and grid template-rows. These properties are very important for understanding, as we use them to determine the number and size of columns and rows.   
V  
Let's look at an example. With grid-template-columns property, we set up five columns. Each column has its own size and also three rows. Pay special attention to the item “auto”. When you leave an empty space between the track values, the grid lines are automatically assigned numerical names.
***
## (Slide #8 - grid-template-areas property)  
Next, we analyze such a property as grid-template-areas. This property defines a grid template by referencing the names of the grid areas which are specified with the grid-area property. Repeating the name of a grid area causes the content to span those cells. This property can be hard to understand. We will look at the example below.  
V  
Note the code. That'll create a grid that's four columns wide by three rows tall. The entire top row will be comprised of the header area. The middle row will be comprised of two main areas, one empty cell, and one sidebar area. The last row is all footer.  
V  
And now look at what should be the result. header and footer occupied the whole row, while main occupied only two cells and sidebar occupied only one cell. 
***
## (Slide #9 - grid-column-gap/grid-row-gap properties)  
Some more interesting properties – So now we look at grid-column-gap and grid-row-gap.   
V  
This properties create the gutters between the columns and rows. Keep in mind that the gutters are only created between the columns and rows, not on the outer edges.
***
## (Slide #10 - justify-items property)  
We continue. The property justify items is very easy to understand. It aligns the content inside a grid item along the column axis.  
V  
Alignment occurs on the left edge. Value is start.   
V  
Value “end” corresponds to the right alignment.  
V  
And also we have value “center”. Here everything is clear on an intuitive level.  
V  
And the last value is stretch. This value stretches over the entire container.
***
## (Slide #11 - align-items property)  
The following property align-items is similar to the previous one – justify-items, the only difference is that align-item aligns the content inside a grid item along the row axis. All values have the same name as the previous ones. Let's look at the implementation of this property.   
V  
In the first picture, we see the pressing elements up.  
V  
Pressing elements down.  
V  
Placing items in the center.  
V  
And stretching all over the area.
***
## (Slide #12 - justify-content property)  
This property – justify-content - is similar to the previous one, the only difference is that here we move not the individual elements, but the entire container.     
V  
This property has several additional values. There are space-around, space-between and space-evenly. These values will be discussed in the following examples.  
V  
You can see the implementation of start value.  
V  
End value.  
V  
Center value.  
V  
Stretch value.  
V  
Now consider the values that have not previously met us. The first It’s space-around. This value places an even amount of space between each grid item, with half-sized spaces on the far ends.  
V  
Space-between places an even amount of space between each grid item, with no space at the far ends.   
V  
And finally the last. The value space-evenly places an even amount of space between each grid item, including the far ends.
***
## (Slide #14 - grid property)  
Let's now see how to optimize the recording of all our properties. Grid property helps us to do this.   
V  
You can pay attention to the existing values of this property. You can see them yourself. And we will look at a brief entry example using the grid property.  
V  
The first example is a brief entry, and the lower example is an analogous entry to the upper example, only all properties are written entirely. Display property will help you reduce the amount of code and improve its readability.
***
## (Slide #15 - grid items properties)  
Finally we got the properties for the grid items. Let's start to get acquainted with them.
***
## (Slide #16 - grid-column-start/grid-column-end/grid-row-start/grid-row-end properties)  
The first properties that we consider will be grid-column-start, grid-column-end, grid-row-start and grid-row-end. This properties determine a grid item's location within the grid by referring to specific grid lines.  
Let's deal with these properties in the examples.  
V  
As you can see grid-column-start and grid-row-start is the line where the item begins. In the example we set our element from the second column and finish it on the 5th column.  
And grid-column-end and grid-row-end is the line where the item ends. In the our example, we set our element from the first line to the third.  
V  
This example is similar to the previous one. You can see by this example alone.
***
## (Slide #17 - grid-area property)  
The grid-area property gives an item a name so that it can be referenced by a template created with the grid-template-areas property. Let's look at an example.  
V  
We can see four values for grid-area property. The first value “number 1” corresponds to “row-start”. In the picture you can see that the blue bar really starts in the first row.  
Second value – “col4-start” corresponds “column-start”. In the picture you see that the blue bar begins with the fourth column.  
Third value – “last line” corresponds “row-end”. Indeed, the blue bar ends in the last row.  
And the last value is “number 6” which corresponds “column-end. How you can see, the blue line in the picture comes to the sixth column.  
I hope you understand the essence of this property.
***
## (Slide #18 - justify-self property)  
This property is very easy to understand, so we will consider it very quickly. Justify-self aligns the content inside a grid item along the column axis. We are already familiar with all the values of this property, so let's just review some examples of the implementation of the justify-self property.  
V  
start - aligns the content to the left end of the grid area  
V  
end - aligns the content to the right end of the grid area  
V  
center - aligns the content in the center of the grid area  
V  
stretch - fills the whole width of the grid area
***
## (slide #19 - align-self property)  
align-self property is similar to the previous one, only the alignment goes horizontally. You can familiarize yourself with this property.
***
## (Slide #20 - practice)  
We are done with theories, let's practice a little now. Repeat after me!
***
## (Slide #22 - html/CSS code)  
Create a div container in which you should place the following items: header, main, two asides and footer. Each element must have its own class. Div container also should have own class.    
V  
You should get this markup. Let's now implement our grid. But first add some styles for better visualization.  
V  
Now you can see the basic styles, they do not belong to grid. We set the color for our blocks, font size and text alignment. Let's see what our markup now looks like.  
V  
Not bad, right? And now let's proceed directly to grid.  
V  
First we set the symbolic names to our blocks using the grid-area property. The established names we can use in the future.  
V  
We have moved to the most important part of our practice.  
With the “display: grid” property we set the rule for working with grid.  
Grid-template-columns and grid-template-rows - sets the size of our blocks.  
Grid-template-areas - uses our symbolic names to indicate where the blocks should located.  
So  
The header occupies one row and all three columns on top.  
The footer occupies one row and all three columns below.  
Navigation, main and aside occupy one row and three columns.  
Let's look at the implementation.  
V  
As you can see all the elements are located in the desired position.
***
## (Slide #23 - finish)  
We finished the study Grid. I hope you have acquired the knowledge you need. Thanks for attention.
