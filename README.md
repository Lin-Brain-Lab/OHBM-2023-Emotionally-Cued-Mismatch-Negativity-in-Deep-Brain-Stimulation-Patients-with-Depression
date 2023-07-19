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
  - Occular correction carried out through application of a semi-automatic ICA where the apparent VEOG componant was removed (IMAGE)
  - Segmentated around each stimuli marker of interest (Neutral in sad conditions, neutral in angry condition, sad, and angry) from -500ms to 1000ms 
  - Baseline correction was applied using the 500ms pre-stimulus interval for each segment
  - Semi automatic artifact rejection was carried out (least segments for any participant/condition was 44)
  - Segments were averaged
  - Each participant's MMN was calculated by comparing the emotional ERP - the neutral ERP
  - Initial grand averages were calculated for each visit, and condition (including MMNs)
  - ERP and MMN data was exported to Matlab for futher calculations

</details>

## Matlab Analysis
Data imported to Matlab for peak determination and calculation and non-parametric statistical analysis of the main effects of condition and visit as well as their interraction.
<details>
  <summary> Full details available here
  </summary>
    
  - Range of interests were determined for MMN data by visually inspecting the GA data (IMAGE) and selecting the timepoints with negative-going wave forms that most closely aligned with previous designated MMN (200-300ms post-stimulus) and late MMN latencies (350-450mas post stimulus)
  - The minimum peak for each participant/visit/condition was then determined from within the range of interest and the average amplitude +/- 25ms was calculated for the final value used
  - data was compared using a non-parametric [Scheirer-Ray-Hare test](https://www.mathworks.com/matlabcentral/fileexchange/96399-non-parametric-alternative-of-2-way-anova-scheirerrayhare)

</details>

## Data Depictions
Data has been depcited using GraphPad Prism 10 and BrainProducts Analyzer.
