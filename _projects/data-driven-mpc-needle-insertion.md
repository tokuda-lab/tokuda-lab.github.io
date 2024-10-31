---
title: "Data-Driven Adaptive Needle Insertion Assist for Transperineal Prostate Interventions"
date: 2024-04-02T12:00:00+5:00
weight: 3
---

A data-driven appraoch to improving the precision of needle placement.

In this project, we investigated a data-driven model predictive control (MPC) for robot-assisted precision needle placement. 

Clinical outcomes of percutaneous prostate interventions, such as biopsy, thermal ablations, and brachytherapy, depend on accurate needle placement. However, placing a long needle (typically 150-200 mm in length) is challenging due to needle deviation induced by needle-tissue interaction. While robotic assistance can potentially address this challenge by compensating for needle deviation based on model-based prediction and/or real-time feedback, several technical hurdles exist, including 1) difficulty in modeling individual patients with accurate geometry and material properties and 2)  complexity of hardware (e.g., a steerable needle, a high-dexterity robot) to achieve accurate needle steering in the soft tissue. 

To overcome those hurdles, we investigated a robot-assisted collaborative needle insertion method that only requires a minimum of 2 degree-of-freedom (2 DOF) passive needle guide and a conventional needle. The method is designed to assist a physician in inserting a needle manually through a needle guide. If the needle deviates from the intended path, actuators shift the needle radially to steer the needle trajectory and compensate for needle deviation adaptively. 


![Radial needle shift - overview](/images/projects/radial-needle-shift-1.png)
![Radial needle shift - algorithm](/images/projects/radial-needle-shift-2.png)

The key technical challenge here is determining the amount of needle-guide shift required to induce needle steering to compensate for the deviation without modeling the patient. We developed a new data-driven MPC algorithm that figured out the needed shift adaptively based on feedback from the previous insertion steps. The method, therefore, does not require a priori information about the needle or tissue properties. 

The method was evaluated in experiments with both in vitro and ex vivo phantoms. The experiments in ex vivo tissue reported a mean final placement error of 0.36 mm with a reduction of 96.25% of placement error when compared to insertions without compensation. The results presented show that the proposed data-driven MPC can be successfully used to correct needle deflection during collaborative manual insertion, and it has the potential to be easily translated into clinical application.

## References

{% bibliography --file tokuda_ref --query @*[pmid=37080237||pmid=33651407] %}

## Acknowledgements

The study was funded in part by the National Institutes of Health (R01CA235134, R01EB020667, and P41EB028741). The content of the material is solely the responsibility of the authors and does not necessarily represent the official views of these agencies.




