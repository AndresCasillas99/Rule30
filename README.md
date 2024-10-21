# Rule30
An efficient algorithm for computing the $n$-th row of Wolfram's Rule 30. <br />

It works by handling each row of Rule30 in a compressed way by storing only the indexes of the columns with value $1$ (all other columns are assumed to have value $0$). This makes calculations much faster and reduces the space complexity of the output.<br />

For example:<br />

steps $= 100$ -> could be any integer larger than $0$. <br />
initial_condition $= [0]$ -> represents the initial condition with only column $0$ (assumed to be the central column) with value $1$. <br />
R30(steps, initial_condition) -> returns an array of indices which codify the $100$-th row on Rule30 after evolving from a single cell with value $1$. <br />

The first rows of Rule30 when starting from a single cell with the value $1$ (which we assume to have column index $0$) would read: <br />

row #0: 1 <br />
row #1: 111 <br />
row #2: 11001 <br />
row #3: 1101111 <br />
row #4: 110010001 <br />

in which case:

$R30(1,[0]) = [-1,0,1]$ <br />
$R30(2,[0]) = [-2,-1,2]$ <br />
$R30(3,[0]) = [-3,-2,0,1,2,3]$ <br />
$R30(4,[0]) = [-4,-3,0,4]$ <br />

