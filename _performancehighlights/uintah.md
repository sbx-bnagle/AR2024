---
layout: highlight

theme: dark
permalink: 'features/aurora-performance-highlights/uintah'

title: 'Reverse Monte-Carlo Radiative Ray Tracing Calculations at Scale: Uintah'
pi: 'Martin Berzins, The University of Utah'
award: 'Aurora Early Science Program'
systems: '-'

image: 'Uintah_Architecture.png' 

---

{% include txt-intro.html 
    blurb = "The Uintah Computational Framework, an open-source asynchronous many-task (AMT) runtime system, has been modified to be performance and large-scale portable across exascale DOE supercomputing systems, including Aurora. This work is the culmination of Uintah’s decade-long, University of Utah-led preparation for DOE exascale systems through highly collaborative multidisciplinary efforts pursued in conjunction with Argonne, Oak Ridge National Laboratory, and Intel as a part of the Predictive Science Academic Alliance Program II and the Aurora Early Science Program. Notable updates to Uintah’s support for Kokkos were required to make this extension possible through Uintah’s adoption of a portable MPI+X hybrid parallelism approach using the Kokkos performance portability library (that is, MPI and Kokkos)."
%}



## Challenge

To scale application codes to hundreds and thousands of Aurora processes via the AMT framework, the development team focused on a Reverse Monte-Carlo Ray Tracing radiation benchmark calculation, central to the University of Utah’s predictive boiler simulations. This benchmark involves potentially global all-to-all communication and uses adaptive mesh refinement and ray tracing to achieve scalability. This benchmark has been used as part of previous scalability studies on a number of pre-exascale systems and the DOE-operated exascale Frontier system while harnessing 98 percent of the machine.



## Performance Results
Working on Aurora, the team was able prepare for a run that would scale from 1280 nodes up to 10,240 nodes successfully for the Burns and Christon benchmark problem on a 2-level structured adaptive mesh refinement grid with more than 129 billion cells, demonstrating that good strong-scaling efficiency is achievable.

These large-scale studies explored the impact of a larger refinement ratio to determine if aggressive mesh refinement will make full-system runs possible. The Uintah runtime systems have proved exceptionally capable in enabling the application to run efficiently at scale on Aurora.


{% include media-img.html
   source= "AR2024_Berzins-chart.png"
   caption= "Strong-scaling results for the Burns and Christon benchmark problem on a 2-level structured adaptive mesh refinement grid with more than 129 billion cells and with 100 rays per cell. Simulations were run on Aurora, from 1,280 nodes up to 10,240 nodes."
%}

## Impact
The scalability results obtained are a promising start and help show the capabilities of Uintah as an exascale AMT runtime system and pave the way for scientific simulations, such as fluid-structure interaction problems or simulations of turbulent reacting flows at unprecedented sizes on exascale machines. Additional work is underway to improve performance, and to better understand how to balance the tradeoffs between computation loads and communications costs when running at the largest scales.
