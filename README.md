# OHBM-2023-Emotionally-Cued-Mismatch-Negativity-in-Deep-Brain-Stimulation-Patients-with-Depression
Extended and ongoing data relating to the OHBM 2023 poster entitled Emotionally-Cued Mismatch Negativity in Deep Brain Stimulation Patients with Depression

Note: Data here reported is from 3 female participants with TRD ages 22, 70, and 64 and was collected at two visits occuring 2- and 4-weeks post DBS implantation.

## Brain Vision Analysis
Initial preprocessing was carried out in BrainVision Analyzer and included DC detrend, bandpass and notch filters, rereferencing to TP9 mastoid electrode and occular correction.
<details>
  <summary> Full pipeline details available here
  </summary>
    
  - Detrend
  - Bandpass filter (1-40hz) with a notch filter at 60hz
  - Rereferenced to mastoid electrode TP9
  - Occular correction carried out through application of a semi-automatic ICA where the [apparent VEOG componant](/Images/pt-007_eeg-2_ic-2d.png) was removed
  - Segmentated around each stimuli marker of interest (Neutral in sad conditions, neutral in angry condition, sad, and angry) from -500ms to 1000ms 
  - Baseline correction was applied using the 500ms pre-stimulus interval for each segment
  - Semi automatic artifact rejection was carried out (least segments for any participant/condition was 44)
  - Segments were averaged
  - Each participant's MMN was calculated by comparing the emotional ERP - the neutral ERP
  - Initial grand averages were calculated for each visit, and condition (including MMNs)
  - ERP and MMN data was exported to Matlab for futher calculations

</details>

## Matlab Analysis
Data imported to Matlab for z-scare difference analysis (to mimic previous analysis method), and non-parametric Scheirer-Ray-Hare statistical analysis of the main effects of condition and visit as well as their interraction.

<details>
  <summary> Full details about the z-score difference analysis available here
  </summary>
    
  - The group average MMN for sad and angry conditions were calculated for each visit separately.
  - The difference between the average sad and average angry MMNs were calculated and transformed into a Z-score time series.
  - The significance time series was calculated from the z-score time series with the significance level adjusted by a false-discovery rate with a significance of 0.05.

</details>

<details>
  <summary> Full details about the non-parametric Scheirer-Ray-Hare statistical analysis available here
  </summary>
    
  - Range of interests were determined for MMN data by visually inspecting the [GA data at electrode Fz](/Images/GA_V1V2_allCond.png) and selecting the timepoints with negative-going wave forms that most closely aligned with previously designated MMN (200-300ms post-stimulus) and late MMN (350-450mas post stimulus) latencies
  - The minimum peak for each participant/visit/condition was then determined from within the range of interest and the [average amplitude +/- 25ms](/Images/Fz_pt-007_eeg2-A.png) was calculated for the final value used 
  - data was compared using a non-parametric [Scheirer-Ray-Hare test](https://www.mathworks.com/matlabcentral/fileexchange/96399-non-parametric-alternative-of-2-way-anova-scheirerrayhare)

</details>

## Results
Note: Data depictions created with BrainVision Analyzer and GraphPad Prism 9.

### Z-score Difference Analysis

### Non-Parametric Scheirer-Ray-Hare Analysis
A depiction of the MMN Grand Averages at Fz for each condition at each visit was created to determine the timepoints of interest for further analysis

![](/Images/GA_V1V2_allCond.png)

The highlighted portions of the graph were determined as timepoints of interest due to the significant negative waveforms present during the expected timepoints of the MMN (200-300ms post stimulus; light blue) and the late MMN (350-450 ms post stimulus; pink). 
In the MMN timerange of interest, a negative going waveform was observed for both conditions and visits while during the late MMN timerange only the angry condition showed a negative going waveform while the GA for the sad condition was generally positive.
The full baseline timerange (500ms pre-stimulus) has been included in this image.


A Scheirer-Ray-Hare test was use to assess the statistical significance of the condition and timepoint main effects as well as their interaction.

![](/Images/V1vsV2_Stats.png)

Depicted here are the angry (red) and sad (blue) means, standard deviation, and each individual participant's calculated average amplitudes (diamond and circle, respectively) for both time points. The test resulted in no statistically significant effects.

## Discussion

Although the time course depicted above depicts visual differentiation between the conditions and perhaps time ranges (particularly during the late MMN time range), these apparent differences did not reach statistical significance. This is perhaps due to the limited sample size (3 participants).
