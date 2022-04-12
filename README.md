# Grid

#HTML
 ** div class="container"
        <div class="item item1">item1</div>
        <div class="item item2">item2</div>
        <div class="item item3">item3</div>
        <div class="item item4">item4</div>
        <div class="item item5">item5</div>
        <div class="item item6">item6</div>
        <div class="item item7">item7</div>
    /div**

    <style>
        .container{
            width:100%;
            height:90%;
            background-color:#ddd;
            margin: 40px auto;
            display:grid;
            grid-template-rows:1fr 1fr 1fr 1fr 1fr;
            grid-template-columns: 1fr 1fr 1fr 1fr;
            grid-template-areas:"header header header header"
                                "sidebar main main main"
                                "sidebar main main main"
                                "sidebar box1 box2 box3"
                                "footer footer footer footer";
            grid-row-gap:30px;
            grid-column-gap:30px;
            grid-gap:30px 50px
        }
        .item{
            padding:30px;
            font-size:30px;
            color:#fff;
        }
        .item1{
            background-color:orangered;
           /* grid-column: 1 / span 4; */
           grid-area: header;
            
        }
        .item2{
            background-color:olivedrab;
          /*  grid-row: 2 / span 4; */
          grid-area: sidebar;
        }
        .item3{
            background-color:royalblue;
          /*  grid-column: 2 / span 3;
            grid-row:2 / span 3;*/
            grid-area: main;
        }
        .item4{
            background-color:palevioletred;
            grid-area: box3;
        }
        .item5{
            background-color:goldenrod;
            grid-area: box1;
        }
        .item6{
            background-color:blueviolet;
            grid-area: box2;
        }
        .item7{
            background-color:pink;
           /* grid-column: 1 / span 4;*/
           grid-area: footer;
        }
    </style>
    
<!--<body>
    <div class="container">
        <div class="item item1">item1</div>
        <div class="item item2">item2</div>
        <div class="item item3">item3</div>
        <div class="item item4">item4</div>
        <div class="item item5">item5</div>
        <div class="item item6">item6</div>
        <div class="item item7">item7</div>
    </div>
</body> -->
