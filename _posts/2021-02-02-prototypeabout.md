---
title: sSAXS intro 
tags: lab-notebook, introduction
article_header:
  type: cover
   

  image:
    src: 
---
(pages 3-5.5 in notebook)
# Overview 
I MADE A RENDER!*UPDATE! :) 

<img class="image image--xl" src="/files/SSAXS.png"/>




I learned about the sSAXS prototype since we decided the old device was hopeless. It is polychromatic with an energy range of ... 


# Transcribed lab notes


The sSAXS device is not made for solution 

It is not put in a vacccum 

air vs sample =/ water vs sample. 

# Matlab analysis code notes
line 63: 1mA empty srynge 
line 64: 1mA caffine sample 

hxtV3Read reads binary .hxt files 
Format of .hxt file is 
[data 0, bins 0] 
data 0 --> (80X80X200)
bins 0 --> (200X1)
200 energy bins (80X80) pixels

0-200 keV bind width 1 keV
I wrote 0-200 keV in my notebook. It is 0-199 keV!
{:.error}

No matter what voltage... collects everything
Unsure what I meant here.
{:.info}

energy bins =bins 1
Referring to matlab code (bins 0 same as bins 1) I think I was confused 
{:.info}

line 87 goes through each beam 
this line (87-89) was just slicing the beam to the correct energy (30-45 keV)
{:.info}

transmission corraction [92-94]

correct data(sum data1)
spectra in each pixel 

```Matlab
87. data_correct2 = sum(data11,3) - sum(data00,3); 
```
line 148... saxspace like
In 201 --> binning --> binning proportional to energy level
I was just talking about creating the histogram binning for q range 
{:.info}

image11 just flipped image 

```Matlab
201. bins = q(:,:,k)>=q_hist(j) & q(:,:,k)<q_hist(j+1);

```

# Questions?
what is test_mask.mat 
It is the mask for the beam. This will be important when doing attenuation correction.
{:.info}

# HEXITEC

![Alt Text](/files/caffeinez.gif)



Turn on bias voltage--voltage drives charge (wow who knew) pixpos
turns on and off every few seconds 

166 AUD units correspond to 5 keV
gradient files - calibrates readings to energy

charge correction - corrects overlapping charges 
charge discriminator - takes highest count and resets all others ~~too~~

find paper (3X3) neigborinng pixels 
Bin=energy bin 
 
