---
title: "Needle Guiding Devices for Prostate Interventions"
date: 2023-05-15T12:00:00+5:00
weight: 3
---

Needle guidance for precision needle placement in the prostate.


Magnetic resonance imaging (MRI) has become essential in the care of prostate cancer. Multiparametric MRI, which combines various MRI contrasts such as T2-weighted, diffusion-weighted, and dynamic contrast-enhanced images, has significantly enhanced the ability to detect, evaluate, and report potential diseases. These images are interpreted and reported using the standardized PI-RADS reporting system.

The rapid advancements in prostate MRI are revolutionizing the diagnosis and treatment of prostate cancer. Multiparametric MRI allows clinicians to target tissue samples from suspected lesions for pathological analysis, a departure from the traditional systematic sampling approach that samples tissues from 6-12 regions regardless of potential lesion locations. The accurate disease mapping provided by multiparametric MRI also makes "focal treatment" more viable. Focal treatment aims to locally destroy the disease while leaving the rest of the prostate gland intact, potentially preserving functions essential for postoperative recovery compared to conventional whole gland treatments, such as prostatectomy and radiation.

To fully leverage MRI in prostate cancer care, it is crucial to guide interventions (e.g., biopsy and focal treatment) with MRI. Our department has been at the forefront of using intraoperative MRI to guide prostate interventions since the 1990s. Our colleagues, Drs. Clare Tempany and Nobuhiko Hata have led this effort and established a successful research program. As part of this program, our team has been developing new technologies to make intraoperative MRI safer, more accurate, and more accessible.

The primary engineering challenge is to accurately deliver a needle into the lesion using MRI guidance. Precise needle placement is essential for MRI-guided prostate interventions to avoid false-negative biopsies and ensure optimal dose distribution for brachytherapy or optimal ablation zone for thermal ablations. To address this challenge, we have developed and evaluated several hardware systems. Those systems are outlined below roughly in chronological order.

## Transperineal Template System for in-bore MRI guidance

While our research program used a specially designed 0.5 Tesla open-configuration MRI system in the early days, it became evident that a specialized system was not viable for widespread adoption due to its limited availability and imaging quality. Since 2009, we transitioned to a more conventional, closed-bore 3T MRI scanner for interventional guidance.

![Manual Template 1](/images/projects/prostate-bx-template-1.jpg){: width="180px" } 
![Manual Template 2](/images/projects/prostate-bx-template-2.jpg){: width="200px" } 
![Manual Template 3](/images/projects/prostate-bx-template-3.jpg){: width="180px" } 

MRI-guided prostate biopsy in conventional closed-bore scanners has its own challenges due to the limited access to the patient in the imaging position in the MRI gantry. To address this issue, we developed a custom-made in-bore setup and software to support MRI-guided transperineal prostate biopsy in the closed-bore MRI scanner {% cite Tokuda2012-ej --file tokuda_ref %}. The setup consists of a specially designed tabletop and a needle-guiding gird template that gives a physician access to the perineum of the patient at the imaging position and allows the physician to perform MRI-guided transperineal biopsy without moving the patient out of the scanner. We also developed custom planning and guidance software based on 3D Slicer.

The hardware and software setup underwent several iterations of improvements and is still used to date at the Brigham. It has been a critical clinical research platform and allowed us to evaluate the efficacy of MRI-guided prostate biopsies. It has also been extended for other procedures, including MRI-guided focal ablation.


## Motorized Template (“Smart Template”)

With Drs. Hata and Sang-Eun Song, we developed our first robotic biopsy guidance system, named Smart Template {% cite Song2013-za --file tokuda_ref %}. The goal is to overcome the problems of limited needle insertion accuracy and human error in the use of a conventional needle guide template.

The Smart Template resembles a transrectal ultrasound-guided prostate template. Unlike the grid template used in the conventional setup, its needle guide is mounted on an X-Y stage, allowing continuous rather than discrete positioning of a needle. The device is made of non-ferromagnetic materials, and fully operational inside the 3-Tesla MRI gantry.

![Smart Template 1](/images/projects/smart-template-clinical-0.png){: width="200px" } 
![Smart Template 2](/images/projects/smart-template-clinical-1.jpg){: width="200px" } 
![Smart Template 3](/images/projects/smart-template-clinical-2.jpg){: width="200px" } 

A clinical study by Tilak et al. {% cite Tilak2015-iq --file tokuda_ref %} evaluated the utility of the Smart Template as compared to a manual template for in-bore 3T transperineal MRI-guided prostate biopsy. Fifty-six biopsy cases were assessed, including 43 cases performed using the Smart Template. It shows that the Smart Template outperforms the manual template in terms of the accuracy of the best needle placement attempts (2.39 mm vs. 3.71 mm, p<0.027), the procedure time (90.82 min vs. 100.63 min, p < 0.030), and the percentage of cancer volume in positive core samples (p < 0.001).

## 4-DoF Needle Guiding Manipulator

A multi-institutional team consisting of BWH, Johns Hopkins University (JHU) (PI: Iulian Iordachita), and Worcester Polytechnic Institute (WPI) (PI: Gregory Fischer) developed a 4-DoF parallel manipulator for needle guidance {% cite Patel2019-gk --file tokuda_ref %}. Unlike the Smart Template, which guides a needle through a small hole, this manipulator has a platform that is translated and rotated by four MRI-conditional ultrasonic motors. This platform serves as a passive needle guide for manual needle insertion. It is also large enough to be equipped with additional actuators to actively insert a needle for future studies. The hardware was primarily developed by WPI and JHU and tested at BWH.

![Prostate Robot 4DoF](/images/projects/prostate-robot-4dof.jpg){: width="300px" } 

Our laboratory led the effort to test the 4-DoF manipulator clinically in 27 patients {% cite Moreira2018-ba --file tokuda_ref %}. The median targeting error in 188 insertions was 6.3 mm. Interestingly, the in vivo accuracy achieved during the clinical trial was significantly lower than that of a phantom test. These results, along with comprehensive MRI data acquired during the study, gave us an insight into how the needle was deflected from the intended needle path. Particularly, we looked into the anatomical structures, such as skin and muscles, involved in the transperineal needle insertion to test if the involvement of any of those structures is correlated to a larger targeting error. The analysis indicated that insertions crossing the bulbospongiosus presented a targeting error lower than the average. The mixed-model analysis demonstrated that the distance between the needle guide and the patient skin, the deviation at the entry point, and the path length inside the pelvic diaphragm had a statistically significant contribution to the targeting error (p < 0.05). Our results indicate that the errors associated with the elastic contact between the needle and the skin were more prominent than the needle bending along the insertion. Our findings will help to improve the preoperative planning of transperineal prostate biopsies.

## 4-DoF Smart Template

With our industrial collaborator, Drs. Jesung Park and Nick Iftimia of Physical Sciences Inc. (PSI) (Andover, MA), we extended the original Smart Template to achieve 4-DoF needle placement {% cite Moreira2021-ey --file tokuda_ref %}. The added DoFs would allow choosing an alternative insertion path to mitigate the deviation induced by the interaction between the needle and specific anatomical structures found in the study outlined above. 

![Smart Template 4DoF](/images/projects/smart-template-4dof-clinical.jpg){: width="300px" }

The new Smart Template has a 4-DoF needle-guiding mechanism allowing a translational range of motion of 65 and 58 mm along the vertical and horizontal axes and a needle rotational motion l (± 30 degrees horizontally and [−30, +10] vertically). We defined a path planning strategy that chooses between straight and angulated insertion paths depending on the anatomical structures on the potential insertion path.

The device was tested in animal models (swine, n = 3) to determine whether the angulated insertion can improve targeting accuracy. It showed that the proposed strategy of selecting straight or angulated insertions based on the subject's anatomy outperformed the conventional approach of just straight insertions regarding targeting accuracy (2.4 mm vs 3.9 mm; p = 0.041 after the bias correction). The in vivo experiment successfully demonstrated that an angulated needle insertion path could improve needle placement accuracy with a path planning strategy that takes account of the subject-specific anatomical structures.
The device was further refined and is currently tested in a human subject study. 



## References

{% bibliography --cited_in_order --file tokuda_ref %}

## Acknowledgements

The study was funded in part by the National Institutes of Health (R01CA235134, R01EB020667, 1R01CA111288, R44CA224853, and P41EB028741). The content of the material is solely the responsibility of the authors and does not necessarily represent the official views of these agencies.











