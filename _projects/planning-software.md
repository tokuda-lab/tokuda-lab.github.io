---
title: "ML-Based Planning and Guidance for Prostate Intervention"
date: 2023-05-15T12:00:00+5:00
weight: 4
---

Exploring the potential of machine learning to empower image-guided and robot-assisted interventions.

Our group has been working closely with clinical experts in prostate MRI and MRI-guided interventions (e.g., biopsy, ablation, surgery). We investigated ML-based approaches to improve planning and navigation of those procedures. 

## Automatic segmentation of prostate and neurovascular bundles on MRI

We investigated a deep-learning (DL)-based automatic image segmentation for magnetic resonance imaging (MRI)-based surgical planning. 

MRI became a crucial diagnostic tool for prostate cancer care. Recent progress in multiparametric MRI (mpMRI) and the PI-RADS reporting system greatly improved radiologists’s ability to detect, evaluate, and report potential diseases. However, raw MRI data, along with a conventional free-text report, do not fully convey the radiologists’ findings, such as the tumor location and its proximity to critical structures, and thus are not a suitable format for the planning and navigation of surgical interventions (e.g., biopsy, ablations, radiation, and surgery), especially when those tasks are computerized. They must be segmented and labeled to create a patient-specific geometric model. 

![Example applications](/images/projects/prostate-segmentation-example.jpg)

To streamline the process of creating a patient-specific geometric model from prostate MRI data, we investigated a new machine-learning algorithm to automatically segment the prostate and surrounding critical structures, including the neurovascular bundles (NVBs) and the external urethral sphincter (EUS), on the images. We used labeled MRI data from our previous clinical study to train a convolutional neural network (CNN) model based on 3D U-Net. 

The specific challenge in this effort was that the label data for those structures were not widely available and were created only from MRI data obtained with a single imaging protocol at a single site. As network models trained on data from a single source suffer from quality loss due to the domain shift, we propose a semi-supervised domain adaptation (DA) method to refine the model's performance in the target domain. Our DA method combines transfer learning and uncertainty-guided self-learning based on deep ensembles. Experiments on the segmentation of the prostate, NVB, and EUS, show significant performance gains with the combination of those techniques compared to pure TL and the combination of TL with simple self-learning.

![Segmentation workflow](/images/projects/prostate-segmentation-workflow.jpg)

Results on a different task and data demonstrate our method's generic application capabilities. Our method has the advantage that it does not require any further data from the source domain, unlike the majority of recent domain adaptation strategies. This makes our method suitable for clinical applications where the sharing of patient data is restricted.

### References

{% bibliography --file tokuda_ref --query @*[pmid=34075061] %}

### Acknowledgements

The study was funded in part by the U.S. National Institutes of Health (R01EB020667, R01CA235134, P41EB015898, P41EB028741), and the EU and the federal state of Saxony-Anhalt, Germany (ZS/2016/08/80388). 


## Data-driven adaptive needle insertion assist for transperineal prostate interventions

Exploring the potential of machine learning to empower image-guided and robot-assisted interventions.

In this project, we investigated a data-driven model predictive control (MPC) for robot-assisted precision needle placement. 

Clinical outcomes of percutaneous prostate interventions, such as biopsy, thermal ablations, and brachytherapy, depend on accurate needle placement. However, placing a long needle (typically 150-200 mm in length) is challenging due to needle deviation induced by needle-tissue interaction. While robotic assistance can potentially address this challenge by compensating for needle deviation based on model-based prediction and/or real-time feedback, several technical hurdles exist, including 1) difficulty in modeling individual patients with accurate geometry and material properties and 2)  complexity of hardware (e.g., a steerable needle, a high-dexterity robot) to achieve accurate needle steering in the soft tissue. 

To overcome those hurdles, we investigated a robot-assisted collaborative needle insertion method that only requires a minimum of 2 degree-of-freedom (2 DOF) passive needle guide and a conventional needle. The method is designed to assist a physician in inserting a needle manually through a needle guide. If the needle deviates from the intended path, actuators shift the needle radially to steer the needle trajectory and compensate for needle deviation adaptively. 

The key technical challenge here is determining the amount of needle-guide shift required to induce needle steering to compensate for the deviation without modeling the patient. We developed a new data-driven MPC algorithm that figured out the needed shift adaptively based on feedback from the previous insertion steps. The method, therefore, does not require a priori information about the needle or tissue properties. 

The method was evaluated in experiments with both in vitro and ex vivo phantoms. The experiments in ex vivo tissue reported a mean final placement error of 0.36 mm with a reduction of 96.25% of placement error when compared to insertions without compensation. The results presented show that the proposed data-driven MPC can be successfully used to correct needle deflection during collaborative manual insertion, and it has the potential to be easily translated into clinical application.

### References

{% bibliography --file tokuda_ref --query @*[pmid=34075061] %}


## AI-Based Isotherm Prediction for Focal Cryoablation of Prostate Cancer

