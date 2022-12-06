---
layout: post
title: "Countour Integration"
tag: Complex Analysis
toc: true
use_math: true
---

![Countour_Integration](/assets/Countour_Integration.pdf)

<div class="content-msg">
	$\int_{-\infty}^{\infty} e^{-x^{2}} d x$: analytical function: $f(z)=\frac{e^{-z^{2}}}{g(z)}$
</div>


$$\oint_C f(z) d z=\int_{\gamma_{1}}+\int_{\gamma_{2}}+\int_{\gamma_{3}}+\int_{\gamma_{4}}
= 2 \pi i \sum {Res}[f(z)] $$

<div class="content-msg">
	Choice of $g(z)$: $1+e^{-2 z \tau}$ - $\tau$: $\sqrt{\pi i}$
</div>


$$\begin{aligned} 
    & \int_{\gamma_{1}}+\int_{\gamma_{3}}=2 \pi i\sum \operatorname{Res}[f(z)] \\ 
  \ \ \Longrightarrow \ \ & \int_{-R}^{R} f(z) d z+\int_{R+i b}^{-R+i b} f(z) d z=\int_{-R}^{R} f(z) d z-\int_{-R}^{R} f(z+i b) d z\\
  \mathrel{\mathop{\ \ \Longrightarrow \ \ }\limits^{\lim _{R \rightarrow \infty}}_{}} &\int_{-\infty}^{\infty} [f(z)-f(z+i b) ]d z=2 \pi i\sum \operatorname{Res}[f(z)]
\end{aligned}$$

Choose $g(z)$ such that $f(z)-f(z+i b)=e^{-z^2}$, however, when the above holds, it must be that $b$ is a complex number. So, we choose $\tau$ such that $f(z)-f(z+\tau)=e^{-z^2}$. That is, $\frac{e^{-z^{2}}}{g(z)}-\frac{e^{-(z+\tau)^{2}}}{g(z+\tau)}=e^{-z^{2}}$. Generally, $g(z)$ is hard to find. To simplify our analysis, it is assumed that $y$ is periodic in $\tau$, we come to:

$$\begin{aligned} 
      & \frac{e^{-z^{2}}}{g(z)}-\frac{e^{-(z+\tau)^{2}}}{g(z)}=e^{-z^{2}} \\ 
    \Longrightarrow& \frac{e^{-z^{2}}}{g(z)}-\frac{e^{-z^{2}} e^{-2 z \tau-\tau^{2}}}{g(z)}=e^{-z^{2}} \\
    \Longrightarrow& g(z)=1-e^{-2 z \tau-\tau^{2}}
\end{aligned}$$

Because it is assumed that $y$ is periodic in $\tau$, we have

$$\begin{aligned}
& g(z)=g(z+\tau) \\
\Leftrightarrow & 1-e^{-2 z \tau-\tau^{2}}=1-e^{-2(z+\tau) \tau-\tau^{2}} = 1-e^{-2 z \tau-\tau^{2}}e^{-2 \tau^{2}}\\
\Leftrightarrow & e^{-2 \tau^{2}} = 1 = e^{2\pi i k}, k \in \mathbb{N}\\
\Leftrightarrow & -2 \tau^{2} =2 \pi i k\\
\Rightarrow & \tau^{2} =\pi i k\\
\Rightarrow & \tau =\sqrt{\pi i k} \quad \text{ let k = 1}\\
\Rightarrow & \tau =\sqrt{\pi i}\\
\end{aligned}$$

<div class="content-msg">
	Poles of $f(z)$		
</div>

Poles: 
$$\begin{aligned} 
			 1+e^{-2 z \tau} &=0 \\ 
			 e^{-2 z \tau} &=-1=e^{i \pi(2 k+1)} \quad k \in \mathbb{Z}\\
			  -2 z \sqrt{i \pi} & =i \pi(2 k+1)\\
			  z&=\frac{\tau}{2}(2 k+1), k=0\\
			  z&=\frac{\tau}{2}
		\end{aligned}$$

<div class="content-msg">
	$\left\rvert\int_{\gamma_2} f(z) d z\right\rvert \rightarrow 0$
</div>

$$\left\rvert\int_{\gamma_{2}} f(z) d z\right\rvert=\left\rvert \int_{\gamma_2} \frac{e^{-z^{2}}}{1+e^{-2 z \tau}} d z \right\rvert, \quad \quad \begin{array} 
			{l}z=R+i t \\ 
			 d z=i d t
		\end{array},  \quad t \in [0,\sqrt{\frac{\pi}{2}}]$$

$$\begin{aligned} 
  & \left\rvert\int_{\gamma_2} f(z) d z\right\rvert\\
  = & \left\rvert\int_{0}^{\sqrt{\frac{\pi}{2}}} \frac{e^{-(R+i t)^{2}}}{1+e^{-2(R+i t) \tau}} i d t\right\rvert\\
  \leq & \int_{0}^{\sqrt{\frac{\pi}{2}}} \frac{\left\rvert e^{-R^{2}-2 R i t+t^{2}}\right\rvert}{\left\rvert 1+e^{-2 \tau(R+i t)} \right\rvert}dt, \quad \rvert a-b\rvert \geq \rvert\rvert a\rvert-(b)\rvert\\
  \leq & \int_{0}^{\sqrt{\frac{\pi}{2}}} \frac{e^{-R^{2}+t^{2}}}{\rvert-\rvert e^{-2 \tau R} e^{-2 \tau i t} \mid\mid } d t\\
  =&\int_{0}^{ \sqrt{\frac{\pi}{2}}} \frac{e^{-R^{2}+t^{2}}}{\left\rvert 1-e^{-2 \sqrt{\frac{\pi}{2}}R} e^{2 \sqrt{\frac{\pi}{2}} t}\right\rvert} d t \rightarrow 0\\
\end{aligned}$$

<div class="content-msg">
	$\left\rvert\int_{\gamma_4} f(z) d z\right\rvert \rightarrow 0$
</div>

$$\left\rvert\int_{\gamma_{4}} f(z) d z\right\rvert=\left\rvert \int_{\gamma_4} \frac{e^{-z^{2}}}{1+e^{-2 z \tau}} d z \right\rvert, \quad \quad \begin{array} 
			{l}z=-R+i t \\ 
			 d z=i d t
		\end{array},  \quad t \in [0,\sqrt{\frac{\pi}{2}}]$$
  
$$\begin{aligned} 
    & \left\rvert\int_{\gamma_4} f(z) d z\right\rvert\\
    = & \left\rvert-\int_{0}^{\sqrt{\frac{\pi}{2}}} \frac{e^{-(-R+i t)^{2}}}{1+e^{-2(-R+i t) \tau}} i d t\right\rvert\\
    \leq & \int_{0}^{\sqrt{\frac{\pi}{2}}} \frac{\left\rvert e^{-R^{2}+2 R i t+t^{2}}\right\rvert}{\left\rvert 1+e^{2 \tau(R-i t)} \right\rvert}dt, \quad \rvert a-b\rvert \geq \rvert\rvert a\rvert-(b)\rvert\\
    \leq & \int_{0}^{\sqrt{\frac{\pi}{2}}} \frac{e^{-R^{2}+t^{2}}}{\rvert-\rvert e^{2 \tau R} e^{-2 \tau i t} \mid\mid } d t\\
    =&\int_{0}^{ \sqrt{\frac{\pi}{2}}} \frac{e^{-R^{2}+t^{2}}}{\left\rvert 1-e^{2 \sqrt{\frac{\pi}{2}}R} e^{2 \sqrt{\frac{\pi}{2}} t}\right\rvert} d t \rightarrow 0\\
  \end{aligned}$$

<div class="content-msg">
	$\int_{-\infty}^{\infty} e^{-x^{2}} d x$
</div>

$$\begin{aligned} 
	 & \int_{\gamma_{1}} + \int_{\gamma_{3}}=\int_{-\infty}^{\infty} e^{-x^{2}} d x=2 \pi i \operatorname{Res}[f(z)] \\ 
	=& 2 \pi i \lim _{z \rightarrow \tau / 2}(z-\tau / 2) \frac{e^{-z^{2}}}{1+e^{-2 z \tau}} \\
	=& 2 \pi\left(\lim _{z \rightarrow \tau / 2} \frac{z-\tau / 2}{1+e^{-2 z \tau}}\right)\left(\lim _{z \rightarrow \tau/{2}} e^{-z^{2}}\right)\\
	=& 2 \pi\left(\lim _{z \rightarrow \tau / 2} \frac{1}{-2 \tau e^{-2 z \tau}}\right) e^{-\tau^{2} / 4}=2 \pi i \frac{e^{-\tau^{2} / 4}}{-2 \tau e^{-2 \tau^2 / 2}} =-\frac{\pi i}{\tau} \frac{e^{-\tau^{2}/4}}{e^{-\tau^{2}}}\\
	=& =\frac{\pi i}{\sqrt{\pi i}} e^{3 \tau^{2} / 4} =-\sqrt{\pi i} e^{i 3 \pi / 4}=-\sqrt{\pi} \sqrt{i} e^{i 3\pi / 4}\\
	=& -\sqrt{\pi} e^{i \pi / 4} e^{i \pi / 4}=-\sqrt{\pi} e^{i \pi}=-\sqrt{\pi}(-1) = \sqrt{\pi}
\end{aligned}$$
