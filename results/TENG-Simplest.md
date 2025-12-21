In this experiment TENG was also given same mesh of points as for unstable FD scheme.

However the results dont show any instability:  

<p align="center">
  <img src="../pictures/Simple_TENG_solution.png" width="1000"><br>
  <em>Figure 1: TENG solution</em>
</p>

It is interesting to compare it with FD scheme:  

<p align="center">
  <img src="../pictures/Simple_FD_solution.png" width="1000"><br>
  <em>Figure 2: FD solution</em>
</p>

TENG seems to be unconditionally stable because it does not amplify sharp local deviations that occur during computations.
Below there are figures with 6 consequent slices of both schemes. 
Deviations from exact solution are artificially displayed larger than they are in reality:   
'd.a. 20 times' means that instead of $u$ we use $u_{da} = u_{exact} + 20*(u-u_{exact})$  

<p align="center">
  <img src="../pictures/Simple_TENG_deviation_1.png" width="1000"><br>
  <em>Figure 3: TENG deviation</em>
</p>

<p align="center">
  <img src="../pictures/Simple_FD_deviation.png" width="1000"><br>
  <em>Figure 4: FD deviation</em>
</p>
