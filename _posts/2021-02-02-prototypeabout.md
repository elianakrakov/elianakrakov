---
title: sSAXS intro 
tags: lab-notebook introduction
article_header:
  type: cover
   

  image:
    src: 
---
(pages 3-5.5 in notebook)
# Overview 
I MADE A RENDER!*UPDATE! :) 

 
![](/files/ssaxs5.png)

All measurements will now be taken on a prototype spectral small-angle X-ray scattering device designed by the Eshan. This device uses a polychromatic X-ray source (tungsten anode, MXR-160/22, COMET) and records data on a 2D spectroscopic detector (HEXITEC, Quantum Detectors Ltd, Oxfordshire, UK) made from Cadmium telluride (CdTe). Unlike the CCD camera used in the previous setup, this detector can measure the energy and position of individual photons. The output is an $80 \times 80 \times 200$ array with the number of photons incident at each position for each energy level. Each pixel in the detector is $250\; \mu$m. Because the detector counts individual photons, a cross-sharing charge discrimination algorithm was implemented into the detector design. 

The polychromatic X-rays were generated using a tube voltage of 50 kVp with a current of 1 mA. The beam was collimated with two lead pinhole collimators of 2.5 mm (P1) then 5 mm (P2) diameter 160 mm apart. The detector was placed 214 mm from P2. A lead beam stop was placed in front of the detector to block non-scattered events and to avoid spectral degradation. 

We placed the sample directly in front of and against the pinhole. There is no vacuum seal and no set slot for the sample---therefore, the exact placement of the container is not consistent. Once the sample is placed,  operator left the room and sets the desired acquisition time and current. For most of the sample measurments, we duscussed useing an acquisition time of 300 seconds and having the current set 1 mA. The X-ray is then turned on, and the data is collected. The data is stored in a .hex file and read using a Python script.



# random notes (pg 3-6 in notebook)



I learned about the sSAXS prototype since we decided the old device was hopeless. Sadness...

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
 
