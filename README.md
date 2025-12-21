# Equations under consideration

## Simplest PDE

$$\frac{\partial u}{\partial t} - \frac{\partial u}{\partial x} = 0$$
Initial condition:  
$$u(x,0) = \sin\left(x\right)$$
Solution:
$$u(x,t) = \sin\left(x+t\right)$$

## Burgers equation

$$\frac{\partial u}{\partial t} + \frac{\partial (f(u))}{\partial x} = 0,\quad  \text{where}\ f(u) = \frac{u^2}{2}$$
Shock initial condition:
$$u(x,0) = 
\begin{cases}
1 & \text{if}\ x < 0 \\
\frac{1}{2} & \text{if}\ x > 0
\end{cases}$$
Shock propagation speed:
$$s = \frac{f(1)-f(\frac{1}{2})}{1-\frac{1}{2}} = \frac{3}{4}$$
Solution:
$$u(x,t) = 
\begin{cases}
1 & \text{if}\ x < st \\
\frac{1}{2} & \text{if}\ x > st
\end{cases}$$

2 cases are considered:
* Burgers operator 1: $\hat{B}_1\circ u = \frac{\partial u}{\partial t} + \frac{\partial}{\partial x}(\frac{1}{2}u^2)$
* Burgers operator 2: $\hat{B}_2\circ u = \frac{\partial u}{\partial t} + u\frac{\partial u}{\partial x}$

## Higher order equations

### Second order
$$\frac{\partial u}{\partial t} - \frac{\partial u}{\partial x} - \lambda \frac{\partial^2 u}{\partial x^2} = 0,\quad \text{where}\ \lambda=-\frac{1}{2}$$

Initial condition:
$$u(x,0) = \sin(kx),\quad \text{where}\ k=2$$

Solution:
$$u(x,t) = e^{-\lambda k^2 t}\sin(k(x+t))$$

(In this equation FD scheme would be even less stable, since we need take $\Delta t \propto (\Delta x)^2$)

### Third order
$$\frac{\partial u}{\partial t} - \frac{\partial u}{\partial x} - \lambda \frac{\partial^3 u}{\partial x^3} = 0,\quad \text{where}\ \lambda=-\frac{1}{2}$$

Initial condition:
$$u(x,0) = \sin(kx),\quad \text{where}\ k=2$$

Solution:
$$u(x,t) = \sin(k(x+t)-\lambda k^3 t)$$

### Fourth order
$$\frac{\partial u}{\partial t} - \frac{\partial u}{\partial x} - \lambda \frac{\partial^4 u}{\partial x^4} = 0,\quad \text{where}\ \lambda=-\frac{1}{2}$$

Initial condition:
$$u(x,0) = \sin(kx),\quad \text{where}\ k=2$$

Solution:
$$u(x,t) = e^{\lambda k^4 t}\sin(k(x+t))$$

# Results

|  Equation  |   PINN   |   TENG   |
|------------|----------|----------|
|  Simplest  | [works](results/PINN-Simplest.md)  | [works](results/TENG-Simplest.md)  |
|  Burgers   | [works](results/PINN-Burgers.md)  | [not stable](results/PINN-Simplest.md)  |
|Higher order| [not accurate](results/PINN-HigherOrder.md)  | TBD  |
