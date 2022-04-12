# Grid

**Creating grid**<br />
	_display:grid;_<br />
By giving display: grid won’t make any change but it stands for initialisation.<br />
<br />
**Create rows and column**<br />
	_grid-template-rows:150px 150px;<br />
 	grid-template-columns: 150px 150px 150px;_<br />
Here for rows two 150px stands for each rows. For example if we give 150px three time then it would be three rows.
Same for column as well.<br />
Instead of px we can give fr which stands for fractional unit specially used for grid measurements.<br /> 
It is mainly used to fill the grid along with the width of container.**grid-template-columns: 1fr 1fr 1fr;** <br />
Instead of giving 1fr for 3 times we can also give **grid-template-columns: repeat(3, 1fr)** <br />
<br />
**Create gaps**<br />
            _grid-row-gap:30px;<br />
            grid-column-gap:30px;<br />
            grid-gap:30px 50px;_<br />
Either 1&2 or 3. **Grid-gap: width height;** can also give **grid-gap: 30px**if both width and height has same value.<br />
<br />
**Positioning Grid items**<br />
For example we have 6 items under a container with 2 rows and 3 columns.<br />
To position 1st item of grid to the 3rd column and 2nd row.<br />
_.item1{<br />
            background-color:orangered;<br />
            grid-column: 2/3;<br />
            grid-row:1/2  }_<br />
Here grid-column: 2/3 means place me at 2nd column where 3 is the ending column and 2 is the staring column<br />
Same to row.<br />
**Grid Span**<br />
_.item1 {<br />
  grid-column: 1 / span 2;<br />
}_<br />
This is most important topic. It spans the cells.<br />
For example 1/ span 2 means. Place me at the 1st cell and make my width elastic with 2nd row <br />
To extend till end of 1st row we can give grid-column 1/-1<br />

**Naming grid areas**<br />
Why we need to name the grid area?<br />
Because it simplifies the content. For example instead of giving 1/ span2  we can stretch the area by just giving name.<br />
Inside container   <br />
          _grid-template-areas: "header header header header"<br />
                                "sidebar main main main"<br />
                                "sidebar main main main"<br />
                                "sidebar box1 box2 box3"<br />
                                "footer footer footer footer";_<br />
