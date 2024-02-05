## Introduction to  Image Fusion + FPM


**Disclaimer:** This image is presented solely for illustrative purposes. No fine-tuning of algorithm parameters has been conducted, and it does not represent the optimal outcome. It serves as a visual aid and may not precisely reflect the results presented in the final published article. 

I employed a fully convolutional image fusion network for intensity-domain image fusion. The model aids in recovering intensity and significantly facilitates phase recovery, as depicted in the results below (the FPM algorithm referred to in the text is the FPM-WSI algorithm).<a href='https://clustrmaps.com/site/1by5c' title='Visit tracker'><img src='//clustrmaps.com/map_v2.png?cl=ffffff&w=1&t=tt&d=M0Nnn2BQ-3Zbl4Fh-NLZ-QenH_11qB67h9_qnCMgqxY' width='1' height='1'/></a>


The following is a preliminary schematic diagram of the images prepared for inclusion in the paper. Below are more detailed explanations for several subsequent images.


![MEIF-FPM full pipeline](./pip.pdf)

*Figure 1: MEIF-FPM full pipeline (a): Overview of the entire pipeline, illustrating the process of capturing multi-exposure images, grouping them based on illumination angles, performing MEIF on sets of multi-exposure images with the same illumination angle, and finally obtaining the MEIF results for FPM reconstruction. (b): Model of raw data acquisition, where samples are illuminated at different angles by an LED array, and the imaging system collects multiple intensity images. For MEIF-FPM, multi-exposure image acquisition is crucial for MEIF. (c): Traditional FPM reconstruction approach incorporating modulus constraints, support constraints, conducting Fourier space updates iteratively. (d): Reconstruction strategy of FD-FPM, involving iterative recovery of information extracted after feature extraction, resembling the princi


![Comparison between raw data from normal exposure and MEIF results](./rd.pdf)

*Figure 2: Comparison between raw data from normal exposure and MEIF results. (a) Stitched image of raw data from normal exposure based on illumination angles. (b) Stitched image of MEIF results based on illumination angles. (c1-c2-c3) Comparison of representative illumination angles between normal exposure (left) and MEIF images (right), with relative positions marked by colored rectangles in (a) and (b).*

![Comparison between FD-FPM reconstruction results from the USAF resolution calculator and original data](./usaf.pdf)

*Figure 3: Comparison between FD-FPM reconstruction results from the USAF resolution calculator and original data. (a) FD-FPM reconstruction without slicing and stitching. (b) Original data in the same region. (c1-c2) Zoomed intensity and phase of MEIF data reconstruction results. (d1-d2), (e1-e2), (f1-f2), (g1-g2), and (h1-h2) showcase the zoomed intensity and phase reconstruction results for EV-1, EV0, EV+1, EV+2, and EV+4, respectively. The line plot on the right illustrates the numerical values corresponding to the pixels in the highlighted region. The phase is depicted in red within a range of 0-1, while intensity is represented in blue. Notably, for (d1-h1), the intensity range spans from 0.2 to 0.7, and for (c1), the range extends from 0 to 0.9.*


![Unstitched onion epidermis FD-FPM reconstruction results](./swyb.pdf)

*Figure 4: Unstitched onion epidermis FD-FPM reconstruction results. (a) Overall sample recovery with MEIF. (b1,b2) Directly captured raw data for ROI near the center, using 4× 0.1 NA and 20× 0.4 NA objectives, respectively; (c1,c2) Directly captured raw data for ROI near the edge; (d1) Intensity and (d2) phase reconstruction results for the ROI near the center with MEIF. (e1) Intensity and (e2) phase reconstruction results for the ROI near the center without MEIF, using raw data from a normal exposure. (f1-f2-g1-g2) Display the intensity and phase reconstruction results for ROIs near the edge with and without MEIF, in the same order as the central ROIs.*


![FD-FPM reconstruction results of animal connective tissue](./beijing.pdf)

*Figure 5: FD-FPM reconstruction results of animal connective tissue: (a1-a4) Stitching-free reconstruction results after MEIF processing, where (a1) and (a4) represent the whole block recovery of intensity and phase results, respectively. (a2, a4) Zoomed-in results of the region of interest (ROI), which is circled in the images. Similarly, (b1), (b4), (b2), and (b3) depict the stitching-free recovery results for intensity and phase, along with zoomed-in ROI results. c3 presents the results directly captured by a higher-resolution objective (20×/0.75NA). The reconstruction data is acquired using a lower-resolution (4×/0.1NA, Nikon) objective.*



![Reconstruction results of a local region in onion epidermis samples using MEIF, HDR, and single-exposure images](./vshdr.pdf)

*Figure 6: Reconstruction results of a local region in onion epidermis samples using MEIF, HDR, and single-exposure images. The numbers 1 and 2 represent the intensity and phase of the reconstructed results, respectively. (a) Reconstruction with MEIF. (b) Reconstruction with C-HDR, involving a process that truncates overexposed and underexposed regions before weighted averaging. (c) Reconstruction with M-HDR, directly averaging all exposure results. (d) Reconstruction with single-exposure raw data.*
