# SEEG-contact detection and skull measurement
<img src="https://github.com/EpiReC-ISARG/SEEG-contact-detection-and-skull-measurement/blob/3354594a9b4f2276b5a70dba3bfaa640a99796b9/main_scene.PNG" width="300" ALIGN=RIGHT> Stereoelectroencephalography (SEEG) is an established invasive diagnostic technique for use in patients with drug-resistant focal epilepsy evaluated before resective epilepsy surgery. The factors that influence the accuracy of electrode implantation are not fully understood. Adequate accuracy prevents the risk of major surgery complications. Precise knowledge of the anatomical positions of individual electrode contacts is crucial for the interpretation of SEEG recordings and subsequent surgery. We developed an image processing pipeline to localize implanted electrodes and detect individual contact positions using computed tomography (CT), as a substitute for time-consuming manual labeling. The algorithm automates measurement of parameters of the electrodes implanted in skulls (bone thickness, implantation angle and depth) for use in modeling predictive factors influencing implantation accuracy. Fifty-four patients evaluated by SEEG were analyzed. A total of 662 SEEG electrodes with 8,745 contacts were stereotactically inserted. The automated detector localized all contacts with better accuracy than manual labeling (p < 0.001). Conclusion: Designed algorithm reliable detected and measured SEEG electrodes thereby allowed assessment implantation accuracy of used frame-stereotaxy, and revealed factors to predict implantation accuracy. The novel automated image processing is a potentially clinically important assistive tool for increasing the yield, efficiency, and safety of epilepsy surgery planning and treatment.


# MATLAB pipeline
Requirements: MATLAB (tested in 2020a), [SPM12 toolbox](https://www.fil.ion.ucl.ac.uk/spm/software/spm12/), GPU with CUDA (NVIDIA) recommended. Use [3D Slicer](https://www.slicer.org/) viewer for visualization and initial labeling.

**SEEG tolbox m-files, tutorial and testing data are available [here](https://drive.google.com/file/d/1hhC1KgZVDjc6lCF1aYOC-MZYcz3VYYvi/view?usp=sharing)**.

The archive contains all processed and created files as well as final 3D Slicer scene (.mrb). The first use requires only MR, CT with electrodes, and preimplantation CT (optional for planning measurement):

volume_data/
- 603553_T1KL.nii (MR)
- 603553_CT.nii (CT with electrodes)
- 603553_CTNAV.nii (optional, CT with Luminant frame)

The main function is MAIN_SEEG_v???.m, functions are in "mfiles_seeg_epirec" folder.

<img src="https://github.com/EpiReC-ISARG/SEEG-contact-detection-and-skull-measurement/blob/e372f7cf2a40ce5e2c88f517fb17344a2466f1e0/luminant.png" width="300" ALIGN=LEFT> The template of Luminant® MR/CT localizer for Cosman–Robert–Wells (CRW® Precision Arc) of 61 patients is [here](https://drive.google.com/file/d/1ovqf5m0-_9x3Z7ETZm3lRu5JBsNo2UbC/view?usp=sharing). We recommend two-phase registration: 1) coregister pacient's CT (with Luminant frame) to averaged template *tpm_CTNAV_61_v2.nii*, 2) use fine-coregistration of CT to simple cage *model tpm_cage_v2.nii*.     

# Tutorial
Follow the tutorial [PDF](https://github.com/EpiReC-ISARG/SEEG-contact-detection-and-skull-measurement/blob/main/SEEG%20Tutorial%20v099.pdf) which contain example patient implantaion scheme. 

## Publication
Janca, R., Tomasek, M., Kalina, A., Marusic., P., Krsek P., Lesko, R. Automated Identification of Stereoelectroencephalography Contacts and Measurement of Factors Influencing Accuracy of Frame Stereotaxy (unpublished) [pre-print](https://github.com/EpiReC-ISARG/SEEG-contact-detection-and-skull-measurement/blob/19c93ccf1f8a0db21c523bf92fa73452045e2c9a/Manuscript_SEEG_TBME_v17.pdf)
