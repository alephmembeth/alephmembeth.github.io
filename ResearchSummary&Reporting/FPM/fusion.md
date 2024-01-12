## Introduction to  Image Fusion + FPM


**Disclaimer:** This image is presented solely for illustrative purposes. No fine-tuning of algorithm parameters has been conducted, and it does not represent the optimal outcome. It serves as a visual aid and may not precisely reflect the results presented in the final published article. 

I employed a fully convolutional image fusion network for intensity-domain image fusion. The model aids in recovering intensity and significantly facilitates phase recovery, as depicted in the results below (the FPM algorithm referred to in the text is the FPM-WSI algorithm).<a href='https://clustrmaps.com/site/1by5c' title='Visit tracker'><img src='//clustrmaps.com/map_v2.png?cl=ffffff&w=1&t=tt&d=M0Nnn2BQ-3Zbl4Fh-NLZ-QenH_11qB67h9_qnCMgqxY' width='1' height='1'/></a>

  
![](./usaf.png)


Subsequent images illustrate the recovery results for USAF under conditions of stray light using the FPM algorithm for different exposure times, along with the results of neural network data preprocessing.

![](./hdrusafa.png)

![](./hdrusafp.png)

Following that, the images demonstrate the recovery results for biological samples under conditions of stray light using the FPM algorithm for different exposure times, along with the results of neural network data preprocessing. The five images correspond to the central bright-field image, intensity map recovered by FPM, intensity map recovered by neural network preprocessing followed by FPM, phase map recovered by FPM, and phase map recovered by neural network preprocessing followed by FPM, respectively.

+ central bright-field image


![](./hdrswyb0a.png)

+ intensity map recovered by FPM
![](./hdrswyb1a.png)

+ intensity map recovered by neural network preprocessing followed by FPM
![](./hdrswyb2a.png)

+ phase map recovered by FPM
![](./hdrswyb1p.png)

+ phase map recovered by neural network preprocessing followed by FPM
![](./hdrswyb2p.png)
