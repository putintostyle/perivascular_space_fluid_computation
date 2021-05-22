# Fluid Mechanism in Perivascular space

### Velocity field

We consider $U = (u_x,u_y, u_z)$ be the velocity of the fluid through the perivascular space.

We consider the cylindrical coordinate representation of $U = (u_r, u_\theta, u_z)$.

Consider the steady state of the Navier-Stoke equation with small Reynolds number.

We have 
$$
\nabla P = \mu\Delta U.
$$
The Laplacian operator in cylindrical representation is written as

$\nabla^2 \vec{U}=\displaystyle\left( \frac{\partial^2 u_r}{\partial r^2}+\frac{1}{r^2}\frac{\partial^2 u_r}{\partial \theta^2}+\frac{\partial^2 u_r}{\partial z^2}+\frac{1}{r}\frac{\partial u_r}{\partial r}-\frac{2}{r^2}\frac{\partial u_\theta}{\partial \theta} -\frac{u_r}{r^2}\right )\vec{e_r} \\ + \displaystyle\left (\frac{\partial^2 u_\theta}{\partial r^2}+\frac{1}{r^2}\frac{\partial^2 u_\theta}{\partial \theta^2}+\frac{\partial^2 u_\theta}{\partial z^2}+\frac{1}{r}\frac{\partial u_\theta}{\partial r}+\frac{2}{r^2}\frac{\partial u_r}{\partial \theta}-\frac{u_\theta}{r^2} \right )\vec{e_\theta} \\\displaystyle \left( \frac{\partial^2 u_z}{\partial r^2}+\frac{1}{r^2}\frac{\partial^2 u_z}{\partial \theta^2}+\frac{1}{r}\frac{\partial u_z}{\partial r}+\frac{\partial^2 u_z}{\partial z^2} \right)\vec{e_z}$.

We neglect the change in $\theta$ and $r$ directions, therefore we have the following equations in the perivascular space.
$$
\begin{equation}
(D.E)\left\{\begin{array}{ccc}
	\displaystyle\frac{1}{r}\frac{\partial }{\partial r}\left(r\frac{\partial u}{\partial r}\right) &=& \displaystyle\frac{1}{\mu}\frac{d P_{in}}{dz} \mbox{ for }r\in(r_1, r_2)\\
	\displaystyle\frac{\bar{\mu}}{r}\frac{\partial }{\partial r}\left(r\frac{\partial \hat{u}}{\partial r}\right) -\frac{\mu}{k}\hat{u} &=& \displaystyle\frac{1}{\mu}\frac{d P_{out}}{dz }\mbox{ for }r\in(r_2, \infty)\\
	
\end{array}\right.
\end{equation}\label{eq:velocity_eq}
$$


$$
\begin{equation}
	(B.C)\left
		\{\begin{array}{cclc}
            u &=& 0&\hspace{5pt}\mbox{ for } r=r_1\\
            \displaystyle\hat{u} &=& u &\hspace{5pt}\mbox{ for } r=r_2\\
            \displaystyle\mu\frac{\partial}{\partial r} u &=& \displaystyle\bar{\mu}\frac{\partial}{\partial r} \hat{u}&\hspace{5pt}\mbox{ for } r=r_2\\
            %\displaystyle\frac{\partial}{\partial r} (\rho u) &=& k_f(\nabla \bar{p}-\sigma \bar{\Pi})&\hspace{5pt}\mbox{ for } r=r_2\\
            \displaystyle\lim_{r\rightarrow\infty}\hat{u} &=& \displaystyle\frac{-k}{\mu}\frac{d P_{out}}{dx}
		\end{array}
	\right.
\end{equation}
$$



The general solutions of $\eqref{eq:velocity_eq}$ are:
$$
\begin{equation}\left\{\begin{array}{ccl}    
u &=& \displaystyle\frac{r^2}{4\mu}\frac{dP_{in}}{dx}+C\ln(r)+D\\
\hat{u} &=& \displaystyle\frac{-k}{\mu}\frac{dP_{out}}{dx}+C_1I_0\left(\sqrt{\frac{\mu_0}{k}}r\right)+C_2K_0\left(\sqrt{\frac{\mu_0}{k}}r\right),
\end{array}\right.\end{equation}
$$
where $I_0, K_0$ are **modified Bessel functions**, $\mu_0 = \displaystyle\frac{\mu}{\bar{\mu}}$.

$K_0(x) = \displaystyle\int_0^{\infty}e^{-x\cosh(t)}dt$.

We first consider the condition of $\hat{u}$ where $\displaystyle\lim_{r\rightarrow\infty}\hat{u} = \displaystyle\frac{-k}{\mu}\frac{d P_{out}}{dx}$ drives $C_1 = 0$ since $I_0$ is exponentially growing, and $K_0$ decays exponentially instead.

Next, with the rest boundary conditions, we have the following equations:
$$
\begin{equation}
	\left\{
		\begin{array}{ccl}
			\displaystyle u(r_1) = 0&\Rightarrow&\displaystyle  \frac{r_1^2}{4\mu}\frac{dP_{in}}{dx}+C\ln(r_1)+D = 0\\
			\displaystyle u(r_2) = \hat{u}(r_2)  &\Rightarrow&\displaystyle \frac{r_2^2}{4\mu}\frac{dP_{in}}{dx}+C\ln(r_2)+D = \frac{-k}{\mu}\frac{dP_{out}}{dx}+C_2K_0\left(\sqrt{\frac{\mu_0}{k}}r_2\right) \\
            \displaystyle\mu\frac{\partial}{\partial r}\bigg\vert_{r=r_2} u = \displaystyle\bar{\mu}\frac{\partial}{\partial r}\bigg\vert_{r=r_2} \hat{u}&\Rightarrow&\displaystyle\frac{r_2}{2}\frac{dP_{in}}{dx}+C\frac{\mu}{r_2} = C_2\bar{\mu}\sqrt{\frac{\mu_0}{k}}K_0'\left(\sqrt{\frac{\mu_0}{k}}r_2\right)\\
            %\displaystyle\frac{\partial}{\partial r}\bigg\vert_{r=r_2} (\rho u) = k_f(\nabla \bar{p}-\sigma \bar{\Pi})&\Rightarrow&\displaystyle \frac{r_2}{2\mu}\frac{dP_{in}}{dx}+C\frac{1}{r_2} = \frac{k_f}{\rho}(\nabla \bar{p}-\sigma \bar{\Pi}) 
		\end{array}
	\right.
\end{equation}
$$
We have 
$$
\begin{equation}
	\left\{
		\begin{array}{ccc}
			C &=& \displaystyle\frac{r_2\left(-2K_{0,\mu_0}r_2-K_{1, \mu_0}\frac{dP_{in}}{dx}\left(r_2^2-r_1^2\right)+M_1K_{1, \mu_0}\right)}{M_0}\\
			D &=& \displaystyle\frac{K_{0, \mu_0}\frac{dP_{in}}{dx}(2r_2^2\ln(r_1)-r_1^2)+r_2\frac{dP_{in}}{dx}K_{1, \mu_0}(r_1^2\ln(r_2)-r_2^2\ln(r_1))-M_1K_{1, \mu_0}(r_2\ln(r_1))}{M_0}\\
			C_2 &=& \displaystyle \frac{\mu_0\left(\frac{dP_{in}}{dx}(r_2^2-r_1^2)+2r_2^2\left(\frac{dP_{in}}{dx}\right)\ln(\frac{r_2}{r_1})+M_1\right)}{M_0}
		\end{array}
	\right.
\end{equation}
$$
where 

$M_1 = \displaystyle4k\frac{dP_{out}}{dx}$

$K_{0,\mu_0} = K_0\left(\sqrt{\frac{\mu_0}{k}}r_2\right)\mu_0$

$K_{1, \mu_0} = \sqrt{\frac{\mu_0}{k}}K_1\left(\sqrt{\frac{\mu_0}{k}}r_2\right)$

$M_0 = 4\mu \left(K_0\left(\sqrt{\frac{\mu_0}{k}}r_2\right)+r_2\sqrt{\frac{\mu_0}{k}}K_1\left(\sqrt{\frac{\mu_0}{k}}r_2\right)\ln\left(\frac{r_1}{r_2}\right)\right)$

### Concentration

