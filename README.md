# DSI Studio Cloud

<img src="https://user-images.githubusercontent.com/275569/166306915-3253113f-fe69-48bb-91a9-000cf5ae6822.png" width=500>

[DSI Studio Cloud](https://github.com/frankyeh/DSI-Studio-Cloud) is a repository that uses GitHub's cloud computing resource to process OpenNeuro diffusion MRI data and share them in the release.  

DSI Studio Cloud makes use of the GitHub-hosted runner, a virtual machine hosted by GitHub, to run topup/eddy and reconstruct GQI and QSDR. The GitHub-Action scripts in the DSI Studio Cloud get data from OpenNeuro to the GitHub runners and processe them using DSI Studio.

## OpenNeuro DWI Data List 

|	Link	|	DS ID | DWI COUNT	|
|----------------------|--------------------------|-------------------------------|
| [The generality of self-control](https://openneuro.org/datasets/ds000009/) | ds000009 | 24 | 
| [UCLA Consortium for Neuropsychiatric Phenomics LA5c Study](https://openneuro.org/datasets/ds000030/) | ds000030 | 262 | 
| [Myconnectome](https://openneuro.org/datasets/ds000031/) | ds000031 | 23 | 
| [Forrest Gump](https://openneuro.org/datasets/ds000113/) | ds000113 | 20 | 
| [A test-retest fMRI dataset for motor language and spatial attention functions](https://openneuro.org/datasets/ds000114/) | ds000114 | 20 | 
| [Multisubject multimodal face processing](https://openneuro.org/datasets/ds000117/) | ds000117 | 11 | 
| [The Stockholm Sleepy Brain Study: Effects of Sleep Deprivation on Cognitive and Emotional Processing in Young and Old](https://openneuro.org/datasets/ds000201/) | ds000201 | 76 | 
| [DWI Traveling Human Phantom Study](https://openneuro.org/datasets/ds000206/) | ds000206 | 55 | 
| [Individual Brain Charting](https://openneuro.org/datasets/ds000244/) | ds000244 | 12 | 
| [NKI-sample](https://openneuro.org/datasets/ds001021/) | ds001021 | 1 | 
| [BTC_preop](https://openneuro.org/datasets/ds001226/) | ds001226 | 36 | 
| [Examining effects of arousal on responses to salient and non-salient stimuli in younger and older adults](https://openneuro.org/datasets/ds001242/) | ds001242 | 52 | 
| [SCA2 Diffusion Tensor Imaging](https://openneuro.org/datasets/ds001378/) | ds001378 | 50 | 
| [thoughtExperiment](https://openneuro.org/datasets/ds001419/) | ds001419 | 1 | 
| [BOLD5000](https://openneuro.org/datasets/ds001499/) | ds001499 | 2 | 
| [Feature Discrimination](https://openneuro.org/datasets/ds001590/) | ds001590 | 32 | 
| [Test dataset for XCP software](https://openneuro.org/datasets/ds001595/) | ds001595 | 1 | 
| [Unilateral Glaucoma 3T dMRI](https://openneuro.org/datasets/ds001743/) | ds001743 | 12 | 
| [InterTVA. A multimodal MRI dataset for the study of inter-individual differences in voice perception and identification](https://openneuro.org/datasets/ds001771/) | ds001771 | 40 | 
| [Bilingualism and the brain](https://openneuro.org/datasets/ds001796/) | ds001796 | 64 | 
| [TheVirtualBrain Macaque MRI](https://openneuro.org/datasets/ds001875/) | ds001875 | 9 | 
| [Longitudinal Brain Correlates of Multisensory Lexical Processing in Children](https://openneuro.org/datasets/ds001894/) | ds001894 | 113 | 
| [ANT: Healthy aging and Parkinson's disease](https://openneuro.org/datasets/ds001907/) | ds001907 | 16 | 
| [Spinal Cord MRI Public Database (Multi-subjects)](https://openneuro.org/datasets/ds001919/) | ds001919 | 236 | 
| [Functional Connectivity of Music-Induced Analgesia in Fibromyalgia](https://openneuro.org/datasets/ds001928/) | ds001928 | 40 | 
| [Auditory localization with 7T fMRI](https://openneuro.org/datasets/ds001942/) | ds001942 | 10 | 
| [BTC_postop](https://openneuro.org/datasets/ds002080/) | ds002080 | 29 | 
| [Datasets with and without deliberate head movements for detection and imputation of dropout in diffusion MRI](https://openneuro.org/datasets/ds002087/) | ds002087 | 1 | 
| [Human Olfaction Without Apparent Olfactory Bulbs](https://openneuro.org/datasets/ds002185/) | ds002185 | 22 | 
| [Dense Investigation of Variability of Affect (DIVA)](https://openneuro.org/datasets/ds002278/) | ds002278 | 2 | 
| [individual_dMRI_fMRI](https://openneuro.org/datasets/ds002307/) | ds002307 | 19 | 
| [Neuroimaging predictors of creativity in healthy adults](https://openneuro.org/datasets/ds002330/) | ds002330 | 66 | 
| [3AM straight reproducibility phantoms](https://openneuro.org/datasets/ds002374/) | ds002374 | 1 | 
| [Spinal Cord MRI Public Database (Single-subject)](https://openneuro.org/datasets/ds002393/) | ds002393 | 19 | 
| [Learning Inhibitory Control and Perception](https://openneuro.org/datasets/ds002543/) | ds002543 | 48 | 
| [The Reading Brain Project L2 Adults](https://openneuro.org/datasets/ds002602/) | ds002602 | 56 | 
| [IBC](https://openneuro.org/datasets/ds002685/) | ds002685 | 13 | 
| [AOMIC-PIOP1](https://openneuro.org/datasets/ds002785/) | ds002785 | 211 | 
| [AOMIC-PIOP2](https://openneuro.org/datasets/ds002790/) | ds002790 | 226 | 
| [Cognitive Training](https://openneuro.org/datasets/ds002843/) | ds002843 | 262 | 
| [Social Processes Initiative in Neurobiology of the Schizophrenia(s) Traveling Human Phantoms](https://openneuro.org/datasets/ds003011/) | ds003011 | 30 | 
| [plp_nf1_dMRI_fMRI](https://openneuro.org/datasets/ds003027/) | ds003027 | 36 | 
| [SUDMEX_TMS: The Mexican dataset of an rTMS clinical trial on cocaine use disorder patients](https://openneuro.org/datasets/ds003037/) | ds003037 | 149 | 
| [DTI data from 'Fiber architecture in the ventromedial striatum and its relation with the bed nucleus of the stria terminalis'](https://openneuro.org/datasets/ds003047/) | ds003047 | 18 | 
| [AOMIC-ID1000](https://openneuro.org/datasets/ds003097/) | ds003097 | 925 | 
| [Tidying Up White Matter: Neuroplastic Transformations in Sensorimotor Tracts following Slackline Skill Acquisition](https://openneuro.org/datasets/ds003138/) | ds003138 | 159 | 
| [Modeling an auditory stimulated brain under altered states of consciousness using the generalized ising model](https://openneuro.org/datasets/ds003171/) | ds003171 | 17 | 
| [SUDMEX_CONN: The Mexican dataset of cocaine use disorder patients](https://openneuro.org/datasets/ds003346/) | ds003346 | 136 | 
| [Ascending arousal network connectivity during recovery from traumatic coma](https://openneuro.org/datasets/ds003367/) | ds003367 | 49 | 
| [MASiVar: Multisite Multiscanner and Multisubject Acquisitions for Studying Variability in Diffusion Weighted Magnetic Resonance Imaging](https://openneuro.org/datasets/ds003416/) | ds003416 | 169 | 
| [Identification of an Amygdala-Thalamic Circuit That Acts as a Central Gain Mechanism in Taste Perception](https://openneuro.org/datasets/ds003424/) | ds003424 | 28 | 
| [dStreamUpgrade](https://openneuro.org/datasets/ds003495/) | ds003495 | 48 | 
| [VEPCON: Source imaging of high-density visual evoked potentials with multi-scale brain parcellations and connectomes](https://openneuro.org/datasets/ds003505/) | ds003505 | 20 | 
| [Language Learning Aptitude dataset](https://openneuro.org/datasets/ds003508/) | ds003508 | 55 | 
| [Data from: Comprehensive ultrahigh resolution whole brain in vivo MRI dataset as a human phantom](https://openneuro.org/datasets/ds003563/) | ds003563 | 4 | 
| [White matter deficits in cocaine use disorder V1.0](https://openneuro.org/datasets/ds003599/) | ds003599 | 133 | 
| [A longitudinal neuroimaging dataset on language processing in children ages 5 7 and 9 years old](https://openneuro.org/datasets/ds003604/) | ds003604 | 362 | 
| [The Reading Brain Project L2 Adults](https://openneuro.org/datasets/ds003872/) | ds003872 | 56 | 
| [TractoInferno: A large-scale open-source multi-site database for machine learning dMRI tractography](https://openneuro.org/datasets/ds003900/) | ds003900 | 284 | 
| [Soma and Neurite Density MRI (SANDI) of the in-vivo mouse brain](https://openneuro.org/datasets/ds003959/) | ds003959 | 12 | 
| [The Reading Brain Project L1 Adults](https://openneuro.org/datasets/ds003974/) | ds003974 | 52 | 
| [The Reading Brain Project L2 Adults](https://openneuro.org/datasets/ds003988/) | ds003988 | 56 | 
| [Structural diffusion and rs-functional MRI data in Macaque Monkeys](https://openneuro.org/datasets/ds003989/) | ds003989 | 3 | 
| [TMS-EEG-MRI-fMRI-DWI data on paired associative stimulation and connectivity (Shirley Ryan AbilityLab, Chicago, IL)](https://openneuro.org/datasets/ds004024/) | ds004024 | 7 | 
| [A synchronized multimodal neuroimaging dataset to study brain language processing](https://openneuro.org/datasets/ds004078/) | ds004078 | 12 | 
| [An open-access accelerated adult equivalent of the ABCD Study neuroimaging dataset (a-ABCD)](https://openneuro.org/datasets/ds004097/) | ds004097 | 40 | 
| [Queensland Twin Adolescent Brain (QTAB)](https://openneuro.org/datasets/ds004146/) | ds004146 | 718 | 
| [Turone Sheep Chronic Stress (TSCS)](https://openneuro.org/datasets/ds004161/) | ds004161 | 48 | 
| [The NIMH Healthy Research Volunteer Dataset](https://openneuro.org/datasets/ds004215/) | ds004215 | 154 | 
| [Characterizing habit learning in the human brain at the individual and group levels: a multi-modal MRI study](https://openneuro.org/datasets/ds004299/) | ds004299 | 247 | 
| [Mapping neuroinflammation in vivo with diffusion-MRI in rats given a systemic lipopolysaccharide challenge](https://openneuro.org/datasets/ds004305/) | ds004305 | 32 | 
| [Rat_diffusion_STZ](https://openneuro.org/datasets/ds004441/) | ds004441 | 28 | 
| [Perinatal Stroke](https://openneuro.org/datasets/ds004498/) | ds004498 | 7 | 
| [The energetic costs of the human connectome](https://openneuro.org/datasets/ds004513/) | ds004513 | 29 | 
| [Brain Differences in Monolingual and Highly Proficient Multilingual Speakers](https://openneuro.org/datasets/ds004581/) | ds004581 | 29 | 
| [Emotion and Development Branch Phenotyping and DTI (2012-2017)](https://openneuro.org/datasets/ds004605/) | ds004605 | 132 | 
| [DTI readouts for designing a preclinical stem-cell therapy trial in experimental stroke](https://openneuro.org/datasets/ds004632/) | ds004632 | 27 | 
| [Sustaining wakefulness: Brainstem connectivity in human consciousness](https://openneuro.org/datasets/ds004640/) | ds004640 | 2 | 
| [EDDEN: Evaluation of Diffusion MRI DENoising](https://openneuro.org/datasets/ds004666/) | ds004666 | 3 | 
| [ON-Harmony: A resource for development and comparison of multimodal brain 3T MRI harmonisation approaches](https://openneuro.org/datasets/ds004712/) | ds004712 | 80 | 
| [Utilizing Amide Proton Transfer Technique to Characterise Diffuse Gliomas Based on WHO 2021 Classification of CNS Tumors](https://openneuro.org/datasets/ds004717/) | ds004717 | 42 | 
| [CS-DSI](https://openneuro.org/datasets/ds004737/) | ds004737 | 20 | 
| [White matter tract](https://openneuro.org/datasets/ds004742/) | ds004742 | 1 | 
| [White matter tract and peaks](https://openneuro.org/datasets/ds004744/) | ds004744 | 17 | 
| [language fMRI](https://openneuro.org/datasets/ds004765/) | ds004765 | 46 | 
| [Aphasia Recovery Cohort (ARC) Dataset](https://openneuro.org/datasets/ds004884/) | ds004884 | 613 | 
| [Stroke Outcome Optimization Project (SOOP)](https://openneuro.org/datasets/ds004889/) | ds004889 | 1715 | 
| [An open relaxation-diffusion MRI dataset in neurosurgical studies](https://openneuro.org/datasets/ds004910/) | ds004910 | 134 | 
| [Probability Decision-making Task with ambiguity](https://openneuro.org/datasets/ds004917/) | ds004917 | 45 | 
| [The FreeSurfer Maintenance Dataset](https://openneuro.org/datasets/ds004958/) | ds004958 | 33 | 
| [MRI dataset evaluating the effect of head down tilt 15Â° on cerebral perfusion in acute ischemic experimental stroke](https://openneuro.org/datasets/ds004962/) | ds004962 | 28 | 
| [Hearing loss Connectome](https://openneuro.org/datasets/ds005026/) | ds005026 | 82 | 
| [CR DBS](https://openneuro.org/datasets/ds005063/) | ds005063 | 1 | 
| [Social Reward and Aging: An Interim Multi-echo fMRI and Diffusion Dataset](https://openneuro.org/datasets/ds005123/) | ds005123 | 108 | 
| [Sequence test for multiband DWI and magnetization transfer sequence](https://openneuro.org/datasets/ds005134/) | ds005134 | 1 | 
| [BOLD variability during cognitive control for an adult lifespan sample](https://openneuro.org/datasets/ds005270/) | ds005270 | 153 | 
| [Maternal Brain Project](https://openneuro.org/datasets/ds005299/) | ds005299 | 25 | 



