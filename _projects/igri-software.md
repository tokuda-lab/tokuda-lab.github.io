---
title: "Software System for Image-Guided Robot-Assisted Interventions"
date: 2023-05-15T12:00:00+5:00
weight: 4
---

Seamless integration of medical image computing and medical robotics.

This project aims to support research on image-guided robot-assisted interventions (IGRI) by providing a common open-source software platform for efficient research, development, and resource sharing. IGRI combines image guidance and robotic assistance to enhance the physician’s ability to see and physically access the lesion with minimal invasion, resulting in a better clinical outcome. 

![Architecture](/images/projects/rosmed-architecture.jpg)

Open-source software is crucial for academic research in many fields, including medical imaging and robotics. It is not simply a cheap alternative to commercial software but has become part of an ecosystem where researchers and engineers share program codes to avoid “reinventing the wheel” and advance the entire field together. Historically, such codes are shared as libraries, which are designed to be incorporated into software applications to reduce the coding effort. However, as software applications become large and complex, it has become a common practice for application developers to deal with numerous libraries to build a software package. Simply sharing libraries is not enough to keep application development manageable. As a solution to this ever-growing software complexity, research communities have been committed to open-source integrated platforms to facilitate rapid and efficient development. Typically, those platforms provide mechanisms for common tasks, such as data I/O and management, as well as visualization. They also provide mechanisms to easily customize or extend with minimal coding efforts, such as plug-in and scripting language interfaces. The 3D Slicer and ROS are two notable examples of integrated platforms that evolved in medical imaging and robotics, respectively.

Integrating 3D Slicer and ROS for IGRI research is seemingly an obvious choice as they already provide many medical imaging and robotics algorithms used in IGRI systems. However, IGRI research has a unique engineering challenge. To build an IGRI system, medical imaging tools, and robotics software/hardware must work harmoniously to achieve the goal. For example, in typical IGRI systems, the robot’s motion is planned in the imaging space; hence, the image processing and the kinematics algorithms must share the same coordinate frame. However, building such a robust software system is difficult, particularly in a low-resource academic research setting. 


Therefore, the goal of this project is to enable seamless integration of 3D Slicer and ROS to establish an open-source software ecosystem for IGRI systems. We believe that the project will allow researchers to incorporate state-of-the-art algorithms and models into their systems for medical robotics with minimum engineering effort and ultimately facilitate rapid and seamless bench-to-bedside translation.


## Collaborators
- [Axel Krieger, Ph.D.](https://engineering.jhu.edu/faculty/axel-krieger/) (Johns Hopkins University)
- [Simon Leonard, Ph.D.](https://www.cs.jhu.edu/~sleonard/) (Johns Hopkins University)
- [Mark Fuge, Ph.D.](https://enme.umd.edu/clark/faculty/539/Mark-D-Fuge)_ (University of Marlyand)
- [Anton Deguet](https://malonecenter.jhu.edu/people/anton-deguet/) (Johns Hopkins University)

## Related Page
- [ROS for Medical Robotics](https://rosmed.github.io)
- [OpenIGTLink](http://openigtlink.org)

## References

{% bibliography --file tokuda_ref --query @*[pmid=35891016||pmid=28567563||pmid=2492347||pmid=22374845||pmid=20033506||pmid=19699057||pmid=19621334] %}

## Acknowledgements

This study was supported in part by the National Institutes of Health (R01EB020667).
