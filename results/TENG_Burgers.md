In this experiment 2 TENGs were tested using 'different' operators:  
* Burgers operator 1: $\hat{B}_1\circ u = \frac{\partial u}{\partial t} + \frac{\partial}{\partial x}(\frac{1}{2}u^2)$
* Burgers operator 2: $\hat{B}_2\circ u = \frac{\partial u}{\partial t} + u\frac{\partial u}{\partial x}$  

However, the bump seems to cause instability in method's behaviour: there were number of experiments with different mesh resolutions, ways to approximate $u_{target}$ (by solution of linear system or using optimizer), activation functions($\tanh$ or $\sin$) and in all cases instability eventually occured and amplified.  

<p align="center">
  <img src="pictures/Burgers_TENG_solution.png" width="500"><br>
  <em>TENG_1 based on operator B_1 and TENG_2 based on B_2</em>
</p>
