---
title: Data collection
tags: experiment, research 
article_header:
  type: cover
  image:
    src: 
    key: docs-image


| Type | Class Names |
| ---- | ---- |
| **base**  | image |
| **size**  | image\-\-md (default), image\-\-xs, image\-\-sm, image\-\-lg, image\-\-xl |

---
# Overview 
Today we collected scattering patterns of BSA, $$\alpha$$-$$syn$$, caffeine, $$\tau au$$, and amyloid-beta using the prototype SAXS system. We were able to see clear scattering peaks for BSA and caffeine, possible peaks for $$\alpha$$-$$syn$$, and no peaks for amyloid-beta or $$\tau au$$. Following initial measurements,  we placed $$\tau au$$, $$\alpha$$-$$syn$$, and amyloid-beta in an incubator to induce aggregation. We will take more measurements of the samples next week.

# SAXS prototype


Because of the issues we had with SAXSpace, we decided to use the prototype version. It is a polychromatic version of the SAXSpace and much more intuitive to use. Because it is polychromatic, it is significantly higher energy and can be used to probe much thicker samples (even though that is not relevant for our setup). However, for the same reason, it can only probe solid samples. 

The X-ray is an open system requiring the operator 

## Sample measurments BSA and Caffine 
For each sample, we took two measurements, each with an exposure time of 300 seconds. All samples were placed in a plastic syringe by (find company name). We also took background measurements of the syringe at the same exposure time. 


## Caffeine
2020_feb_1ma_300s_caffine_I.hxt (first measurments)
2020_feb_1ma_300s_caffine_II.hxt (second measurment) 
<ol>
<li>collect offsset (blank with X-ray off) taken into account in program</li>
<li>Set present time for 400 seconds b/c bias refresh</li>
<li>Take measurment for 300 seconds only</li>
</ol>
The 
{:.warning}
<img class="image image--md" src="/files/dataacqusition.PNG"/>
*shutter controll*

<img class="image image--md" src="/files/shuttercontroll.JPG"/>
*shutter controll*





## BSA
Should expect same bragg peaks as amyloid-$\beta$ 

2021_feb2_1mA_300s_bsa_I.hxt (first measurments)
2021_feb2_1mA_300s_bsa_II.hxt (second measurment) 


Originally accidentally named finals 2021_feb2_1mA_300s_syringe_empty.hxt & 2021_feb2_1mA_300s_syringe_empty2.hxt (changed them to I and II for consistency) 
{:.warning}


2021_feb2_1mA_300s_syringe_emptyI.hxt (first measurment)
2021_feb2_1mA_300s_syringe_emptyII.hxt (second measurment)
<ol>
<li>2 measurments signal</li>
<li>2 measurments background (syringe only)h</li>
<li>Take measurment for 300 seconds </li>
</ol>


## Tau 383/Amyloid-$\beta$/$\alpha$-syn
we ran into some problems...


# Tau 383
rPeptide is to protein samples as T-mobile is to celular plans.
{:.error}
We purchased Tau 383 from rPeptide because it was cheaper than sigma aldrich. I ordered 500 $$\mu g$$ of the protein in the form of white lyophilized powder. [See data sheet here](https://www.rpeptide.com/_code/_dyn_images/products/data-sheet/T-1005-Tau-383-Revised.pdf).  Here is what we got. 

<img class="image image--md" src="/files/lies.png">




Both viles were supposed to have the same amount of powder in them. We received 4 viles, each (supposedly) containing 125 $$\mu g$$. I scraped enough of the powder out to fill a vile. 


measurments 
2021_feb2_1mA_300s_tau383_original_I.hxt (first measurment) 
Originally we thought we saw scattering at 13 nm$^{-1}$ from the tau sample, but it turned out that it was just scattering off of the tip. 


2021_feb2_1mA_300s_syringe_empty2_neartip.hxt (background near tip) 

#  amyloid-$\beta$-42
amyloid sample from Sigma-Aldrich. Had 1000 $$\mu g$$ of sample stored in refrigerator in lab. Unsure how long it was there. Transfered sample to srynge. Oddly the sample looked a little fluffy? Why is this? 

2021_feb2_1mA_300s_AB42_original_I.hxt
saw nothing. Just scattering from syringe. Took just one measurment. 

# $\alpha$ synuclein 
1000 $$\mu g$$ alpha synuclein from Sigma-Aldrich purchased with Tau. Sample had powder like consistency as expected. Transfered to plastic srynge.  

2021_feb2_1mA_300s_asyn_original_I.hxt (first measurment)
Think we saw two peaks at 6.04$nm^{-1}$ and 13 nm^{-1}. Why if it is before aggregation though?
{:.success}

2021_feb2_1mA_300s_asyn_original_II.hxt (second measurment) 
Second trial was consistent! 


We made sure we were not getting scattering off of tip by adjusting the sample so the pinhole was further away. 
{:.info} 
