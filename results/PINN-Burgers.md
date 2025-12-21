In this experiment 2 PINNs were trained using 'different' operators:  
* Burgers operator 1: $\hat{B}_1\circ u = \frac{\partial u}{\partial t} + \frac{\partial}{\partial x}(\frac{1}{2}u^2)$
* Burgers operator 2: $\hat{B}_2\circ u = \frac{\partial u}{\partial t} + u\frac{\partial u}{\partial x}$

However the results are almost equal, deviation seems to be same as deviation between 2 identical PINN solutions from different launches:

<p align="center">
  <img src="pictures/Burgers_PINN_solutions.png" width="500"><br>
  <em>PINN_1 used operator B_1 and PINN_2 used B_2</em>
</p>
