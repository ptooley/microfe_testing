# Handbuilt cube demo.  

Unfortunately the file formats for this don't seem to allow internal comments (epic fail), so I
will attempt to document here.

### handbuilt.d

This is intended to be a 2x2x2 cube of elements, initially arranged in a completely regular grid,
the node layout is as follows:

    ### Z = 0

     y 0   1   2
    x 
    0  1---2---3
       |   |   |
    1  4---5---6
       |   |   |
    2  7---8---9 


    ### Z = 1

     y 0   1   2
    x 
    0  10--11--12
       |   |   |
    1  13--14--15
       |   |   |
    2  16--17--18 


    ### Z = 2

     y 0   1   2
    x 
    0  19--20--21
       |   |   |
    1  22--23--24
       |   |   |
    2  25--26--27 


The element layout then follows numbered in the pattern:

  ### Layer 1

    1---2
    |   |
    3---4

  ### Layer 2

    5---6
    |   |
    7---8


### handbuilt.bnd

This fixes the nodes in the bottom layer, i.e for N=1-9

  N 1 1 1

### handbuild.fix

This displaces the top layer of nodes by -0.1 in Z ie for N=19-27

  N 3 -0.1

### handbuild.lds

This is not set, but I put in a single line as directed for node 13:

  13 0 0 0

### handbuilt.dat

This is the tricky one, I might have things wrong here right now, but I tried to understand and
crib from the demo file as best I could.

  
