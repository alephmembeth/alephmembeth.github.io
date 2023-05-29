Last week, I focused on three articles, one on the installation, use, and some examples of Simpa, and the other two on the study and modeling of the properties of photoacoustic pressure. In the following section, I will mainly introduce my understanding and thoughts on the three articles.



### SIMPA: an open-source toolkit for simulation and image processing for photonics and acoustics



This article describes the uses, details, capabilities and significance of SIMPA, and how to install it. It also includes two extension tools, MCX and k-Wave.

##### MCX(MCXCL)

MCX relies on CUDA support, which my hardware does not meet. Fortunately, the official website also introduces an alternative, the MCXCL version, which utilizes OpenCL. However, my usual computer has an AMD CPU with limited OpenCL support. Thankfully, after switching to another computer (NUC8), I was able to successfully run MAC-STUDIO test samples.

##### K-Wave

Installing the K-wave Matlab toolkit was a seamless process, and it was also emphasized as the most important file by my teacher. I followed the instructions provided on the official website, made some parameter modifications, and attempted to run it on Matlab. Through this process, I gained a better understanding of the meaning and influence of certain parameters.

##### SIMPA

I attempted to run some files provided on GitHub and successfully configured the environment as instructed.

When running the "full_simulation" script, I encountered the following issue:

![](C:\Users\w3397\AppData\Roaming\Tencent\QQ\Temp\5T~J{GG~@8$LOIATCX6@K]D.png)

An error message "MCXCL ERROR(5): Out of resources in unit mcx_host.cpp:772" was displayed, which I suspect is due to insufficient hardware performance.

When running some other files, I removed the CUDA dependency and ran them, and it appears that they ran successfully:

![d3e14b6691ac474f3c30207bee25a132](C:\Users\w3397\AppData\Roaming\Tencent\QQ\Temp\d3e14b6691ac474f3c30207bee25a132.JPG)

Based on my experience, if I use MCX or MMC instead of MCXCL, the results are even worse, with some cases not working at all. Therefore, I would like to inquire if the aforementioned problem is indeed caused by inadequate hardware performance. If so, I would appreciate some guidance on the typical configuration for successful cases.



I would like to consult Professor Gao regarding how to address this issue and whether it is necessary to resolve it.



### Understanding the near-field photoacoustic spatiotemporal profile from nanostructures 

The article proposes that based on numerical simulations and analysis, there is an existence of anisotropy in the photoacoustic amplitude under certain environments. Furthermore, they attempt to utilize this anisotropy for achieving focusing.



##### 

Consider a gold nanorod immersed in re-water :$p(\vec r,t)$ satisfied
$$
\left(\nabla^2-\frac{1}{v_s^2} \frac{\partial}{\partial t^2}\right) p(\mathbf{r}, t)=-\frac{\beta}{\kappa v_s^2} \frac{\partial^2 T(\mathbf{r}, t)}{\partial t^2}
$$


where,
$$
\frac{\partial^2 T}{\partial t^2}=\frac{1}{C_{n r} m_{n r}} \frac{\partial H}{\partial t}
$$


beacuse process is thermally confined,



Neglecting the acoustic scattering at the nanorod/water interface, We can solve this equation easily by convolving with Green's function.$G\left (\mathbf r, t, \mathbf{r}^{\prime}, t^{\prime}\right)=\frac{\delta\left(t-t^{\prime}-\frac{\mid \mathbf{r}-\mathbf{r}_s \mathbf{\prime}}{v_s}\right)}{4 \pi\left|\mathbf{r}-\mathbf{r}^{\prime}\right|}$
$$
\begin{aligned}p(\mathbf{r}, t)&=\left ( -\frac{\beta}{\kappa v_s^2} \frac{\partial^2 T(\mathbf{r}, t)}{\partial t^2}\right )\ast G\left (\mathbf r, t, \mathbf{r}^{\prime}, t^{\prime}\right)\\&=\left.\frac{\beta}{4 \pi \kappa v_s^2} \int d \mathbf{r}^{\prime} \frac{1}{\left|\mathbf{r}-\mathbf{r}^{\prime}\right|} \frac{\partial^2 T\left(\mathbf{r}^{\prime}, t^{\prime}\right)}{\partial t^{\prime} 2}\right|_{t^{\prime}=t-\frac{\left|\mathbf{r}-\mathbf{r}^{\prime}\right|}{v_s}}\end{aligned}
$$
Under the far-field and wide-pulse approximations,
$$
p_{s p h}(\mathbf{r}, t)=\frac{\beta}{4 \pi \kappa v_s^2} \frac{1}{|\mathbf{r}|} \int d \mathbf{r}^{\prime} \frac{\partial^2 T\left(\mathbf{r}^{\prime}, t\right)}{\partial t^{\prime} 2}
$$
However, the equation becomes ineffective under other conditions. Therefore, the authors employ a simulation approach where different equations are used in different regions to increase computational efficiency.

The distribution patterns of the PA amplitude and a comparison of several numerical simulations can be found in Figure 2.

The article also defines several physical quantities to illustrate the relationships between various simulations, which are well represented in the figures.

Further investigation was conducted to explore the impact of pulse width.

Furthermore, the article provides an example regarding the control of photoacoustic distribution using three nanoparticles，which demonstrates the universality of the ideas presented in the article.

In the end, the authors concluded that there is a possibility of precisely controlling the amplitude distribution using nanostructures. Under certain conditions, the concepts of "focus" and "focusing" were observed, indicating the ability to achieve precise control and manipulation of acoustic energy distribution. Therefore, it is important to select the optimal pulse width to achieve better "resolution" in order to maximize the ability to distinguish and resolve fine details in the imaging process.



### Modeling photoacoustic pressure generation in colloidal suspensions at different volume fractions based on a multi-scale approach

The article explains that the dependence on volume fraction($\eta$) is an important and complex factor. However, many articles do not discuss this aspect. Therefore, the authors propose four models to investigate this issue.

The article combines some models and thus calculates the volume fraction dependence of some physics quantities.

 The reading of the article is not yet complete, and there will be further updates on the research approach and personal insights in the future.

