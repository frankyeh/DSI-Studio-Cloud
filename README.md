# DSI Studio Cloud

<img src="https://user-images.githubusercontent.com/275569/166306915-3253113f-fe69-48bb-91a9-000cf5ae6822.png" width=500>

[DSI Studio Cloud](https://github.com/frankyeh/DSI-Studio-Cloud) is a GitHub repository that uses GitHub's cloud computing resource to analyze diffusion MRI data. It can construct tractography and analyze its diffusion and shape metrics. The code can be extended to accomplish any command line functions provided in DSI Studio.

DSI Studio Cloud makes uses of the GitHub-hosted runner, a virtual machine hosted by GitHub, to process dMRI data. The GitHub-Action scripts in the DSI Studio Cloud get data from OpenNeuro to the GitHub runners and processe them using DSI Studio.

## Advantages

- **Free computation resources**: GitHub action provides 20 concurrent jobs with 2-core each. The computation power is equal to a 40-core workstation, much faster than running it on most laptops/desktops.
- **Faster data transfer**: The raw dMRI data are usually huge and can be up to several GB per scan, but tractography and related metrics are substantially smaller at MB size. Using DSI Studio Cloud, the amount of data transfer can be dramatically reduced. 

## Requirements 

- dMRI data stored on [OpenNeuro](https://openneuro.org/)
- A [GitHub](https://github.com/) account (free)

## Limitations

- **Not more than 256 scans data**: There is a maximum of 256 jobs per workflow run. DSI Studio will still generate SRC and FIB files for downloading, but fiber tracking cannot be executed due to the this limit.

## Examples Dataset

- [(OpenNeuro ds002087) Datasets with and without deliberate head movements for detection and imputation of dropout in diffusion MRI](https://openneuro.org/datasets/ds002087/versions/1.0.0)
- [(OpenNeuro ds001378) SCA2 Diffusion Tensor Imaging](https://openneuro.org/datasets/ds001378/versions/1.0.0)

## Pipeline

The DSI Studio Cloud pipeline includes preprocessing (eddy correction and align ac-pc), quality check, automatic fiber tracking, region-based analysis, and connectivity matrix.
![image](https://user-images.githubusercontent.com/275569/167920232-68b2e6d8-88db-48ab-9950-7e0f5f85d6bf.png)


## Steps

1. **Fork the repository**: Click on the `Fork` button in the upper right corner.

<img src="https://user-images.githubusercontent.com/275569/157307065-a172c393-a4db-4cf3-92c8-b4482619a0e7.png" width=500>

2. **Enable Actions**: Click on the `Actions` menu and confirm `I understand my workflows, go ahead and enable them`. 

<img src="https://user-images.githubusercontent.com/275569/157596167-7d9ee687-2633-4d48-ba5f-c12c62b04b35.png" width=500>

3. **Run Actions**: Under the same `Actions` menu, click on `Auto-Track (OpenNeuro)` on the left and click run `workflow` on the right. 

*Setup Parameters*:

|Parameters | Descriptions |
|-----------|---------------|
| OpenNeuro Accession Number | the DS number of the OpenNeuro data. (e.g. ds001378) |
| Preprocessing: Eddy Correction | specify whether to correct DWI data using FSL eddy. |
| Preprocessing: Align AC-PC | specify whether to resample DWI to align ac-pc. |
| Pipeline: Region Analysis | the region analysis pipeline calculates the averages value of metrics in the atlas regions. | 
| Pipeline: Connectivity Matrix | the connectivity matrix pipeline calculates the whole-brain connectivity matrix using the atlas parcellations. | 
| Pipeline: Automatic Fiber Tracking | the automatic fiber tracking pipeline maps tracts of interests and calculates their diffusion and shape metrics. | 
| Options: Atlases | specify the atlases to be used in region analysis or connectivity matrix. [Full list of atlases](https://github.com/frankyeh/DSI-Studio-atlas/tree/main/ICBM152)  |
| Options: Tracts of Interest | specify the tracts to be mapped used in automatic fiber tracking. Partial name accepted. [Full list of tracts](https://github.com/frankyeh/DSI-Studio-atlas/blob/main/ICBM152/ICBM152.tt.gz.txt)|

Click on `Run workflow` to start. 

4. **Download Results**: 

Once completed, the FIB files, tract files, and tract metrics can be downloaded from the Release on the right of the repository.

![image](https://user-images.githubusercontent.com/275569/169601907-eb2c040f-78f4-4f38-931a-85c320b99b08.png)


## OpenNeuro DWI Data List 

|	DS NUMBER	|	DWI COUNT	|		NAME		|
|----------------------|--------------------------|-------------------------------|
|	ds000009	|	24	|	[The generality of self-control](https://openneuro.org/datasets/ds000009)
|	ds000030	|	262	|	[UCLA Consortium for Neuropsychiatric Phenomics LA5c Study](https://openneuro.org/datasets/ds000030)
|	ds000031	|	44	|	[MyConnectome](https://openneuro.org/datasets/ds000031)
|	ds000113	|	20	|	[Forrest Gump](https://openneuro.org/datasets/ds000113)
|	ds000114	|	1	|	[A test-retest fMRI dataset for motor, language and spatial attention functions. ](https://openneuro.org/datasets/ds000114)
|	ds000117	|	11	|	[Multisubject multimodal face processing](https://openneuro.org/datasets/ds000117)
|	ds000201	|	76	|	[The Stockholm Sleepy Brain Study: Effects of Sleep Deprivation on Cognitive and Emotional Processing in Young and Old](https://openneuro.org/datasets/ds000201)
|	ds000206	|	319	|	[DWI Traveling Human Phantom Study](https://openneuro.org/datasets/ds000206)
|	ds000221	|	228	|	[ds000221_R1.0.0](https://openneuro.org/datasets/ds000221)
|	ds000244	|	12	|	[Individual Brain Charting](https://openneuro.org/datasets/ds000244)
|	ds001021	|	1	|	[NKI-sample](https://openneuro.org/datasets/ds001021)
|	ds001226	|	72	|	[BTC_preop](https://openneuro.org/datasets/ds001226)
|	ds001242	|	52	|	[Examining effects of arousal on responses to salient and non-salient stimuli in younger and older adults](https://openneuro.org/datasets/ds001242)
|	ds001378	|	50	|	[SCA2 Diffusion Tensor Imaging](https://openneuro.org/datasets/ds001378)
|	ds001419	|	1	|	[thoughtExperiment](https://openneuro.org/datasets/ds001419)
|	ds001499	|	4	|	[BOLD5000](https://openneuro.org/datasets/ds001499)
|	ds001590	|	45	|	[Feature Discrimination](https://openneuro.org/datasets/ds001590)
|	ds001595	|	1	|	[Test dataset for XCP software](https://openneuro.org/datasets/ds001595)
|	ds001743	|	12	|	[Unilateral Glaucoma 3T dMRI](https://openneuro.org/datasets/ds001743)
|	ds001771	|	80	|	[InterTVA. A multimodal MRI dataset for the study of inter-individual differences in voice perception and identification.](https://openneuro.org/datasets/ds001771)
|	ds001796	|	64	|	[Bilingualism and the brain](https://openneuro.org/datasets/ds001796)
|	ds001875	|	27	|	[TheVirtualBrain Macaque MRI](https://openneuro.org/datasets/ds001875)
|	ds001894	|	113	|	[Longitudinal Brain Correlates of Multisensory Lexical Processing in Children](https://openneuro.org/datasets/ds001894)
|	ds001907	|	81	|	[ANT: Healthy aging and Parkinson's disease](https://openneuro.org/datasets/ds001907)
|	ds001919	|	266	|	[Spinal Cord MRI Public Database (Multi-subjects)](https://openneuro.org/datasets/ds001919)
|	ds001928	|	40	|	[Functional Connectivity of Music-Induced Analgesia in Fibromyalgia](https://openneuro.org/datasets/ds001928)
|	ds001942	|	60	|	[Auditory localization with 7T fMRI](https://openneuro.org/datasets/ds001942)
|	ds002080	|	58	|	[BTC_postop](https://openneuro.org/datasets/ds002080)
|	ds002087	|	2	|	[Datasets with and without deliberate head movements for detection and imputation of dropout in diffusion MRI](https://openneuro.org/datasets/ds002087)
|	ds002185	|	22	|	[Human Olfaction Without Apparent Olfactory Bulbs](https://openneuro.org/datasets/ds002185)
|	ds002307	|	37	|	[individual_dMRI_fMRI](https://openneuro.org/datasets/ds002307)
|	ds002330	|	132	|	[Neuroimaging predictors of creativity in healthy adults](https://openneuro.org/datasets/ds002330)
|	ds002366	|	33	|	[Emotion regulation in the Ageing Brain, University of Reading, BBSRC](https://openneuro.org/datasets/ds002366)
|	ds002374	|	1	|	[3AM straight reproducibility phantoms](https://openneuro.org/datasets/ds002374)
|	ds002393	|	19	|	[Spinal Cord MRI Public Database (Single-subject)](https://openneuro.org/datasets/ds002393)
|	ds002543	|	96	|	[Learning, Inhibitory Control, and Perception](https://openneuro.org/datasets/ds002543)
|	ds002602	|	56	|	[The Reading Brain Project L2 Adults](https://openneuro.org/datasets/ds002602)
|	ds002634	|	40	|	[Project_larynx](https://openneuro.org/datasets/ds002634)
|	ds002685	|	23	|	[IBC](https://openneuro.org/datasets/ds002685)
|	ds002785	|	422	|	[AOMIC-PIOP1](https://openneuro.org/datasets/ds002785)
|	ds002790	|	453	|	[AOMIC-PIOP2](https://openneuro.org/datasets/ds002790)
|	ds002843	|	262	|	[Cognitive Training](https://openneuro.org/datasets/ds002843)
|	ds003011	|	30	|	[Social Processes Initiative in Neurobiology of the Schizophrenia(s) Traveling Human Phantoms](https://openneuro.org/datasets/ds003011)
|	ds003027	|	36	|	[plp_nf1_dMRI_fMRI](https://openneuro.org/datasets/ds003027)
|	ds003047	|	18	|	[DTI data from 'Fiber architecture in the ventromedial striatum and its relation with the bed nucleus of the stria terminalis'](https://openneuro.org/datasets/ds003047)
|	ds003097	|	3670	|	[AOMIC-ID1000](https://openneuro.org/datasets/ds003097)
|	ds003171	|	17	|	[Modeling an auditory stimulated brain under altered states of consciousness using the generalized ising model](https://openneuro.org/datasets/ds003171)
|	ds003346	|	137	|	[SUDMEX_CONN: The Mexican dataset of cocaine use disorder patients.](https://openneuro.org/datasets/ds003346)
|	ds003367	|	50	|	[Ascending arousal network connectivity during recovery from traumatic coma](https://openneuro.org/datasets/ds003367)
|	ds003416	|	3934	|	[MASiVar: Multisite, Multiscanner, and Multisubject Acquisitions for Studying Variability in Diffusion Weighted Magnetic Resonance Imaging](https://openneuro.org/datasets/ds003416)
|	ds003424	|	56	|	[Identification of an Amygdala-Thalamic Circuit That Acts as a Central Gain Mechanism in Taste Perception](https://openneuro.org/datasets/ds003424)
|	ds003495	|	48	|	[dStreamUpgrade](https://openneuro.org/datasets/ds003495)
|	ds003505	|	64	|	[VEPCON: Source imaging of high-density visual evoked potentials with multi-scale brain parcellations and connectomes](https://openneuro.org/datasets/ds003505)
|	ds003508	|	110	|	[Language Learning Aptitude dataset](https://openneuro.org/datasets/ds003508)
|	ds003563	|	8	|	[Data from: Comprehensive ultrahigh resolution whole brain in vivo MRI dataset as a human phantom](https://openneuro.org/datasets/ds003563)
|	ds003599	|	133	|	[White matter deficits in cocaine use disorder V1.0](https://openneuro.org/datasets/ds003599)
|	ds003604	|	377	|	[A longitudinal neuroimaging dataset on language processing in children ages 5, 7, and 9 years old](https://openneuro.org/datasets/ds003604)
|	ds003813	|	1	|	[Fitlins - Example ](https://openneuro.org/datasets/ds003813)
|	ds003959	|	12	|	[Soma and Neurite Density MRI (SANDI) of the in-vivo mouse brain](https://openneuro.org/datasets/ds003959)
|	ds003974	|	52	|	[The Reading Brain Project L1 Adults](https://openneuro.org/datasets/ds003974)
|	ds003988	|	56	|	[The Reading Brain Project L2 Adults](https://openneuro.org/datasets/ds003988)
|	ds003989	|	3	|	[Structural, diffusion and rs-functional MRI data in Macaque Monkeys](https://openneuro.org/datasets/ds003989)
|	ds004024	|	7	|	[TMS-EEG-MRI-fMRI-DWI data on paired associative stimulation and connectivity (Shirley Ryan AbilityLab, Chicago, IL)](https://openneuro.org/datasets/ds004024)
|	ds004069	|	2872	|	[Queensland Twin Adolescent Brain (QTAB)](https://openneuro.org/datasets/ds004069)
|	ds004078	|	24	|	[A synchronous multimodal neuroimaging dataset to study brain language processing](https://openneuro.org/datasets/ds004078)
|	ds004097	|	40	|	[An open-access accelerated adult equivalent of the ABCD Study neuroimaging dataset (a-ABCD)](https://openneuro.org/datasets/ds004097)

