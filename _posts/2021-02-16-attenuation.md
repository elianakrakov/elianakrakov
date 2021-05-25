title: Attenuation Correction
tags: lab-notebook, experiment 
article_header:
  type: cover
  image:
    src: 
    key: docs-image



---

# Attenuation Correction

Absorption occurs when an incident photon is  completely absorbed by an atom resulting in the ejection of an electron. The decrease in photon flux as a result of absorption is given by $$I(E)=I_0(E)e^{-\mu(E)T}$$ where $I_0$  is the photon count without a sample and $\mu(E)$ is the X-ray attenuation coefficient for a specific material. If $N_s(i,j,E)$ is the scattered photon count reaching the detector,  the unobstructed photon count, denoted by $N_t(i,j,E)$, can be expressed as
 $$N_t(i,j,E)=N_s(i,j,E)\int_0^{T} S(x,\theta _{ij},E)dx$$

To account for attenuation, I followed the procedure described by \citep{Dahal_2017}. We took two measurements of the sample, container, and two measurements of the background without the beamstop. All measurements were taken with an exposure of 150 s with the current set to .2 mA to avoid damaging the detector.  Each of these images is then averaged along each an energy index $E_i$ for $ 30 \leq i \geq 45$ resulting in a $1\times16$ array of averaged pixel values, denoted $I_0$. Once we obtained these values, we divided each energy index of the original sample by the corresponding average energy giving the attenuation corrected data. A mask of the beam area was also made - I ended up re-using it. 

In the analasis code I wrote, attenuation correction function is transmission_corrected(mask,transmission1,transmission2,sample) where the mask is the the mask image, transmission1 and transmission 2 are the the two measurments of the sample without the beamstop and sample is the measurment with the beamstop. 

The mask was determined prior to my research and is an 8x4 pixel array of 1 values at the beam center. I am not sure this is accurate. One thing I hope to work on in the future is coming up with a more accurate way to get only the primary beam photons (as this was the point of the mask. Here is an example.

<img src="/files/mask.png">

## Procedure
  beam stop was removed prior to measurments 
{:.info}
<img class="image image--xl" src="/files/beamstop.jpg"/>
 

 
changed threshold value on detector 116 to 916. This corresponds to 27 keV and above. These settings are in the HEXITEC software (HexitecGigE V1.1)
{:.info}
<img class="image image--xl" src="/files/processing_setup.PNG"/>
 *HEXITEC DETECTOR PROCESSING SETUP. CHANGE THRESHOLD TO 916*



X-ray and detector settings for following measurments 

| Current  | Voltage | exposure time | threshold | beamstop |
| --- | --- | --- | --- | --- |
|   .2 ma | 50 kVp | 150 s | 916 | no |


# Open beam
![ Alt text](/files/beam.gif) 
Took two measurments of open beam. 



| measurment # | file name |
| --- | --- |
|   I | 2021_feb16_0.2mA_150s_transmission_openbeam_I.hxt |
| II | 2021_feb16_0.2mA_150s_transmission_openbeam_II.hxt |


if oversaturates we can set beam to .1 mA but we were fine at .2 mA. 

<img src="/files/opennbeamtrans.png">
*averaged E_i values for open beam*
## PMMA sample
First collected 1 cm measurment. Used 2 blocks of .5 cm PMMA slabs.


# 1 cm
two .5 cm blocks

| measurment # | file name |
| --- | --- |
|   I | 2021_feb16_150s_0.2mA_transmission_PMMA_10mm_I.hxt |
| II | 2021_feb16_150s_0.2mA_transmission_PMMA_10mm_II.hxt |


<img src="/files/pmma10mm.png">
*averaged E_i values for 10mm PMMA*



# 3 cm

| measurment # | file name |
| --- | --- |
|     I | 2021_feb16_150s_0.2mA_transmission_PMMA_30mm_I.hxt |
| II | 2021_feb16_150s_0.2mA_transmission_PMMA_30mm_II.hxt |


<img src="/files/pmma30mm.png">
*averaged E_i values for 30mm PMMA*


Took two measurments at .2mA and 150s
two .5 cm blocks and one 2 cm block.


## Samples 
# Empty syringe 
<img src="/files/emptysrynge.png">

| measurment # | file name |
| --- | --- |
|  I | 2021_Feb16_0.2mA_150s_empty_syringe_I.hxt |
| II | 2021_Feb16_0.2mA_150s_empty_syringe_II.hxt |

<img src="/files/empty.png">
*averaged E_i values for 30mm PMMA*

# Caffeine 



| measurment # | file name |
| --- | --- |
|  I | 2021_Feb16_0.2mA_150s_caffeine_syringe_I.hxt |
| II | 2021_Feb16_0.2mA_150s_caffeine_syringe_II.hxt |

<img src="/files/caff12.png">
*averaged E_i values for caffeine sample*

# BSA


| measurment # | file name |
| --- | --- |
|  I | 2021_Feb16_0.2mA_150s_BSA_syringe_I.hxt |
| II | 2021_Feb16_0.2mA_150s_BSA_syringe_II.hxt |

<img src="/files/BSA.png">
*averaged E_i values for BSA sample*

# $\alpha$-synuclein

<img src="/files/nobeamstop_asyn.png">



| measurment # | file name |
| --- | --- |
|  I | 2021_Feb16_0.2mA_150s_alpha_aggregates_quartz_I.hxt |
| II | 2021_Feb16_0.2mA_150s_alpha_aggregates_quartz_II.hxt |

<img src="/files/ALPHA.png">
*averaged E_i values for $\alpha$-syn sample*


# amyloid-$\beta$
<img src="/files/ab_prof.png">



| measurment # | file name |
| --- | --- |
|  I | 2021_Feb16_0.2mA_150s_abBeta_aggregates_quartz_I.hxt |
| II | 2021_Feb16_0.2mA_150s_abBeta_aggregates_quartz_II.hxt |


<img src="/files/ALPHA.png">
*averaged E_i values for amyloid sample*

<img src="/files/amyloidtransmission (1).png">

Here you can see amyloid transmission overlayed with the open beam and sample. 






