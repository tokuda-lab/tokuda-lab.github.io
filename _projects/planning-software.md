---
title: "ML-Based Planning and Guidance for Prostate Intervention"
date: 2023-05-15T12:00:00+5:00
weight: 4
---

ML assistance for image-guided and robot-assisted prostate internvetions .

Our group has been working closely with clinical experts in prostate MRI and MRI-guided interventions (e.g., biopsy, ablation, surgery). We investigated ML-based approaches to improve planning and navigation of those procedures. 

## Automatic segmentation of prostate and neurovascular bundles on MRI

We investigated a deep-learning (DL)-based automatic image segmentation for magnetic resonance imaging (MRI)-based surgical planning. 

MRI became a crucial diagnostic tool for prostate cancer care. Recent progress in multiparametric MRI (mpMRI) and the PI-RADS reporting system greatly improved radiologists’s ability to detect, evaluate, and report potential diseases. However, raw MRI data, along with a conventional free-text report, do not fully convey the radiologists’ findings, such as the tumor location and its proximity to critical structures, and thus are not a suitable format for the planning and navigation of surgical interventions (e.g., biopsy, ablations, radiation, and surgery), especially when those tasks are computerized. They must be segmented and labeled to create a patient-specific geometric model. 

![Example applications](/images/projects/prostate-segmentation-example.jpg)

To streamline the process of creating a patient-specific geometric model from prostate MRI data, we investigated a new machine-learning algorithm to automatically segment the prostate and surrounding critical structures, including the neurovascular bundles (NVBs) and the external urethral sphincter (EUS), on the images. We used labeled MRI data from our previous clinical study to train a convolutional neural network (CNN) model based on 3D U-Net. 

The specific challenge in this effort was that the label data for those structures were not widely available and were created only from MRI data obtained with a single imaging protocol at a single site. As network models trained on data from a single source suffer from quality loss due to the domain shift, we propose a semi-supervised domain adaptation (DA) method to refine the model's performance in the target domain. Our DA method combines transfer learning and uncertainty-guided self-learning based on deep ensembles. Experiments on the segmentation of the prostate, NVB, and EUS, show significant performance gains with the combination of those techniques compared to pure TL and the combination of TL with simple self-learning.

![Segmentation workflow](/images/projects/prostate-segmentation-workflow.jpg)

Results on a different task and data demonstrate our method's generic application capabilities. Our method has the advantage that it does not require any further data from the source domain, unlike the majority of recent domain adaptation strategies. This makes our method suitable for clinical applications where the sharing of patient data is restricted.

### Related Papers

{% bibliography --file tokuda_ref --query @*[pmid=34075061] %}

### Acknowledgements

The study was funded in part by the U.S. National Institutes of Health (R01EB020667, R01CA235134, P41EB015898, P41EB028741), and the EU and the federal state of Saxony-Anhalt, Germany (ZS/2016/08/80388). 


## Data-driven adaptive needle insertion assist for transperineal prostate interventions

In this project, we investigated a data-driven model predictive control (MPC) for robot-assisted precision needle placement. 

Clinical outcomes of percutaneous prostate interventions, such as biopsy, thermal ablations, and brachytherapy, depend on accurate needle placement. However, placing a long needle, typically 150-200 mm in length, is challenging due to needle deviation induced by needle-tissue interaction. While several approaches for needle trajectory correction have been studied, many of them do not translate well to practical applications due to the use of specialized needles not yet approved for clinical use, or to relying on needle-tissue models that need to be tailored to individual patients.Approach.In this paper, we present a robot-assisted collaborative needle insertion method that only requires an actuated passive needle guide and a conventional needle. The method is designed to assist a physician inserting a needle manually through a needle guide. If the needle is deviated from the intended path, actuators shifts the needle radially in order to steer the needle trajectory and compensate for needle deviation adaptively. The needle guide is controlled by a new data-driven algorithm which does not requirea prioriinformation about needle or tissue properties. The method was evaluated in experiments with bothin vitroandex vivophantoms.Main results.The experiments inex vivotissue reported a mean final placement error of 0.36 mm with a reduction of 96.25% of placement error when compared to insertions without the use of assistive correction.Significance.Presented results show that the proposed closed-loop formulation can be successfully used to correct needle deflection during collaborative manual insertion with potential to be easily translated into clinical application.


## AI-Based Isotherm Prediction for Focal Cryoablation of Prostate Cancer

