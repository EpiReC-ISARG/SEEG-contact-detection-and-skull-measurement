# SEEG-contact-detection-and-skull-measurement
Stereoelectroencephalography (SEEG) is an established invasive diagnostic technique for use in patients with drug-resistant focal epilepsy evaluated before resective epilepsy surgery. The factors that influence the accuracy of electrode implantation are not fully understood. Adequate accuracy prevents the risk of major surgery complications. Precise knowledge of the anatomical positions of individual electrode contacts is crucial for the interpretation of SEEG recordings and subsequent surgery. We developed an image processing pipeline to localize implanted electrodes and detect individual contact positions using computed tomography (CT), as a substitute for time-consuming manual labeling. The algorithm automates measurement of parameters of the electrodes implanted in skulls (bone thickness, implantation angle and depth) for use in modeling predictive factors influencing implantation accuracy. Fifty-four patients evaluated by SEEG were analyzed. A total of 662 SEEG electrodes with 8,745 contacts were stereotactically inserted. The automated detector localized all contacts with better accuracy than manual labeling (p < 0.001).Conclusion: Designed algorithm reliable detected and measured SEEG electrodes thereby allowed assessment implantation accuracy of used frame-stereotaxy, and revealed factors to predict implantation accuracy. The novel automated image processing is a potentially clinically important assistive tool for increasing the yield, efficiency, and safety of epilepsy surgery planning and treatment.

# MATLAB pipeline
Requirements: MATLAB (tested in 2020a), [SPM12 toolbox](https://www.fil.ion.ucl.ac.uk/spm/software/spm12/), GPU with CUDA (NVidia) recommended.

All m-files, tutorial and testing data are in [Google Drive](https://drive.google.com/file/d/1hhC1KgZVDjc6lCF1aYOC-MZYcz3VYYvi/view?usp=sharing)
The archive contains all processed and created files. The first use requires only MR, CT with electrodes, and preimplantation CT (optional for planning measurement):
volume_data/
603553_T1KL.nii (MR)
603553_CT.nii (CT with electrodes)
603553_CTNAV.nii (optional, CT with Luminant frame)

The main function is MAIN_SEEG_v???.m, tools are in "mfiles_seeg_epirec" folder.

# Tutorial
Follow the tutorial [PDF](https://github.com/EpiReC-ISARG/SEEG-contact-detection-and-skull-measurement/blob/main/SEEG%20Tutorial%20v099.pdf) which contain example patient implantaion scheme. 

## Publication
Janca, R., Tomasek, M., Kalina, A., Marusic., P., Krsek P., Lesko, R. Automated Identification of Stereoelectroencephalography Contacts and Measurement of Factors Influencing Accuracy of Frame Stereotaxy (in peer-review)
