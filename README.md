# Demonstrating How MIMIC-III Benchmarks Run in Python
The Medical Information Mart for Intensive Care III (MIMIC-III) is one of the largest and most publically accessible critical care unit databases in the world. It contains scrubbed health-related data of ~ 60,000 pediatric and adult patients who stayed in critical/intensive care units (CCUs or ICUs) at the Beth Israel Deaconess Medical Center between 2001 and 2012. The MIMIC-III database is created from information such as “demographics, vital sign measurements taken at bedside, laboratory test results, procedures, medications, caregiver notes, imaging reports, and mortality (both in and out of hospital).” (https://mimic.physionet.org/about/mimic/) Its data are housed in 26 tables with additional derived tables.  MIMIC-III represents the third collection of ICU data organized and maintained by the Laboratory of Computational Physiology at MIT, in conjunction with Philips Medical Systems, and Beth Israel Deaconess Medical Center (BIDMC) (https://link.springer.com/chapter/10.1007/978-3-319-43742-2_5).  

## What Makes this a Worthwhile Final Project
MIMIC-III is a database in which I have been certified to work since August, 2018. For reasons outside the scope of the HMI 7540 course, my exposure to MIMIC-III has heretofore been limited. Additionally, one of the goals of my graduate research professor is that we apply Python Code to the research we are planning in the MIMIC-III data for Fall, 2019. So, the timing of this class project presented  a opportunity that combined both MIMIC-III and Python.

A GitHub search for potential topics uncovered a project using Python Code and the MIMIC-III database by four Cornell University researchers: Hrayr Harutyunyan, Hrant Khachatrian, David C. Kale, Greg Ver Steeg, and Aram Galstyan. Their work was located in this repository https://github.com/YerevaNN/mimic3-benchmarks and titled,  "Python suite to construct benchmark machine learning datasets from the MIMIC-III clinical database." Their research was published in the article, "Multitask Learning and Benchmarking with Clinical Time Series Data" (https://arxiv.org/abs/1703.07771), and it aligned with some of our targeted research around machine learning. Additionally, the authors encouraged others to reproduce their benchmarks using their code, noting that no "extensive knowledge of medicine or clinical data" was required. They provided the steps to follow, the Python scripts to use and the only cavaet was to download the MIMIC-III files, which they could not provide and that I already had access to them. 

Also, selecting this for the class project introduce fellow students to MIMIIC-III and this was benefical for two reasons:
 1. MIMIC-III contains high-temporal resolution data including lab results, electronic documentation, bedside monitor trends and waveforms, which makes it one of the most thorough databases of healthcare information related to ICU patient hospital stays. Given the difficulty of finding and gaining permission to do research on actual patient data, access to MIMIC-III might remove a right-to-access block from students who need real patient data for their research.  
 1. Secondly, it is a straight-forward though somewhat time-consuming process to gain access to MIMIC-III. Students just need to complete a series of nine courses from MIT, which are housed on the CITI Program website (https://about.citiprogram.org/en/homepage/). Kennesaw State University (KSU) provides free access to CITI-based courses and require students to take KSU-related courses on through the CITI platform for IRB requirements so, students can take the MIT courses, too.

## Summary of the Original Research Purpose
Harutyunyan's, et al's work used data from the MIMIC-III database to create four publicaly available clinical prediction benchmark data sets. Prior to their efforts, there were no benchmark sets based on publicly available healthcare data. The theory is that the absence of readily available benchmarks handicaps the progress of machine learning in healthcare research, specifically in discoveries that can't be identified in the reams of accumulating and underexamined patient data. This patient information continues to accumulate because it is generated through the increasing adoption of electronic health records (EHRs). 

Harutyunyan and his colleagues wrote and Python coded scripts to help "compile a subset of the MIMIC-III database with more than 31 million clinical event from 42,276 [intensive care unit] ICU stays of 33,798 unique patients." Using this subset, they defined "four clinical predication tasks"  previously identified as the premium areas in which data analytics could make a significant impact. These four areas include:
 1. in-hospital mortality prediction
 1. physiological decompensation prediction
 1. length-of-stay prediction
 1. phenotype classification
 
## Process Used and Code Examined 
After several read-throughs of the Harutyunyan, et al's article, and with the intention of following the author's suggestion to duplicate the creation of the benchmarks, the next step was to examine the whole MIMIC-III-benchmarks repository.  (https://github.com/YerevaNN/mimic3-benchmarks) This took days rather than hours and required various types of study. For instance, I started with READMe and then began looking at the .py code in the mimic3models file and subfolders. The code was detailed.  As an example, the mimic3models file (https://github.com/YerevaNN/mimic3-benchmarks/tree/master/mimic3models) contained ~20 subfolders. I opened all of them but examined the preprocessing.py file. (https://github.com/YerevaNN/mimic3-benchmarks/blob/master/mimic3models/preprocessing.py).  It took 90-minutes to "talk-through" or dissect the first 50 lines of the ~231 total lines in "preprocessing.py."   
 
I noted the other content in the repository, including the Structure section https://github.com/YerevaNN/mimic3-benchmarks#structure and especially the Requirements https://github.com/YerevaNN/mimic3-benchmarks#requirements and Building A Benchmark portion.  https://github.com/YerevaNN/mimic3-benchmarks#building-a-benchmark.

Unfortunately, things did not go as planned.

## Mistakes and "Regrets, I've Had a Few..." 
### (from Frank Sinatra's, "My Way")
1. Downloading the entire MIMIC III database was a pain because of the file type
 1. The original file type from the 
1. The requirements on how to run the scripts really do require NumPY and Pandas.





 



