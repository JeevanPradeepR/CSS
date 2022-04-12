# Grid
Grid

**Creating grid**
	_display:grid;_
By giving display: grid won’t make any change but it stands for initialisation.

**Create rows and column**
	_grid-template-rows:150px 150px;
 	grid-template-columns: 150px 150px 150px;_
Here for rows two 150px stands for each rows. For example if we give 150px three time then it would be three rows.
Same for column as well.
Instead of px we can give fr which stands for fractional unit specially used for grid measurements. 
It is mainly used to fill the grid along with the width of container.** grid-template-columns: 1fr 1fr 1fr;**
Instead of giving 1fr for 3 times we can also give **grid-template-columns: repeat(3, 1fr)**

**Create gaps**
            _grid-row-gap:30px;
            grid-column-gap:30px;
            grid-gap:30px 50px;_
Either 1&2 or 3. **Grid-gap: width height;** can also give **grid-gap: 30px**if both width and height has same value.

**Positioning Grid items**
For example we have 6 items under a container with 2 rows and 3 columns.
To position 1st item of grid to the 3rd column and 2nd row.
_.item1{
            background-color:orangered;
            grid-column: 2/3;
            grid-row:1/2  }_
Here grid-column: 2/3 means place me at 2nd column where 3 is the ending column and 2 is the staring column
Same to row.
**Grid Span**
_.item1 {
  grid-column: 1 / span 2;
}_
This is most important topic. It spans the cells.
For example 1/ span 2 means. Place me at the 1st cell and make my width elastic with 2nd row 
To extend till end of 1st row we can give grid-column 1/-1

**Naming grid areas**
Why we need to name the grid area?
Because it simplifies the content. For example instead of giving 1/ span2  we can stretch the area by just giving name.
Inside container   
          _grid-template-areas: "header header header header"
                                "sidebar main main main"
                                "sidebar main main main"
                                "sidebar box1 box2 box3"
                                "footer footer footer footer";_
