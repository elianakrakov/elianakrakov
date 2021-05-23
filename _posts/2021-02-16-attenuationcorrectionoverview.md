---
title: Attenuation Correction Overview
tags: experiment, research 
article_header:
  type: cover
  image:
    src: 
---

# Attenuation Correction

Absorption occurs when an incident photon is  completely absorbed by an atom resulting in the ejection of an electron. The decrease in photon flux as a result of absorption is given by $$I(E)=I_0(E)e^{-\mu(E)T}$$ where $I_0$  is the photon count without a sample and $\mu(E)$ is the X-ray attenuation coefficient for a specific material. If $N_s(i,j,E)$ is the scattered photon count reaching the detector,  the unobstructed photon count, denoted by $N_t(i,j,E)$, can be expressed as
 $$N_t(i,j,E)=N_s(i,j,E)\int_0^{T} S(x,\theta _{ij},E)dx$$

To account for attenuation, I followed the procedure described by \citep{Dahal_2017}. We took two measurements of the sample, container, and two measurements of the background without the beamstop. All measurements were taken with an exposure of 150 s with the current set to .2 mA to avoid damaging the detector.  Each of these images is then averaged along each an energy index $E_i$ for $ 30 \leq i \geq 45$ resulting in a $1\times16$ array of averaged pixel values, denoted $I_0$. Once we obtained these values, we divided each energy index of the original sample by the corresponding average energy giving the attenuation corrected data. A mask of the beam area was also made - I ended up re-using it. 

In the analasis code I wrote, attenuation correction function is transmission_corrected(mask,transmission1,transmission2,sample) where the mask is the the mask image, transmission1 and transmission 2 are the the two measurments of the sample without the beamstop and sample is the measurment with the beamstop. 

Here are some example images of mask, transmission and sample as a reminder of what they look like. These are for $\beta$ amyloid 


<img src="/files/mask.png">
<img src="/files/nobeamstop_asyn.png">
<img src="/files/ab_prof.png">
## empty srynge
<img src="/files/emptysrynge.png">
## open beam 
<img src="/files/openbeam.png">


Just plotting the 


<img src="/files/amyloidtransmission.png">






