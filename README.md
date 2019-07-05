# Demonstrating How MIMIC-III Benchmarks Run in Python
The Medical Information Mart for Intensive Care III (MIMIC-III) is one of the largest and most publically accessible critical care unit databases in the world. It contains scrubbed health-related data of ~ 60,000 pediatric and adult patients who stayed in critical/intensive care units (CCUs or ICUs) at the Beth Israel Deaconess Medical Center between 2001 and 2012. The MIMIC-III database is created from information such as “demographics, vital sign measurements taken at bedside, laboratory test results, procedures, medications, caregiver notes, imaging reports, and mortality (both in and out of hospital).” (https://mimic.physionet.org/about/mimic/) Its data are housed in 26 tables with additional derived tables.  MIMIC-III represents the third collection of ICU data organized and maintained by the Laboratory of Computational Physiology at MIT, in conjunction with Philips Medical Systems, and Beth Israel Deaconess Medical Center (BIDMC) (https://link.springer.com/chapter/10.1007/978-3-319-43742-2_5).  

## What Makes this a Worthwhile Final Project
MIMIC-III is a database in which I have been certified to work since August, 2018. For reasons outside the scope of the HMI 7540 course, my exposure to MIMIC-III has heretofore been limited. Additionally, one of the goals of my graduate research professor is that we apply Python Code to the research we are planning in the MIMIC-III data for Fall, 2019. So, the timing of this class project presented  a timely opportunity.

A GitHub search for potential topics uncovered this title and associated repository "Python suite to construct benchmark machine learning datasets from the MIMIC-III clinical database" (https://github.com/YerevaNN/mimic3-benchmarks). The research from this article, "Multitask Learning and Benchmarking with Clinical Time Series Data" (https://arxiv.org/abs/1703.07771), aligned with some of our graduate research (GRA) work. In the Introduction section of the article, the authors encouraged others to go to the repository above, use their code to duplicate the benchmarks while noting that no "extensive knowledge of medicine or clinical data" was required. The only cavaet was that everyone had to download the MIMIC-III files, which I had the access to do. 

Selecting this for the class project also allowed me to introduce MIMIIC-III to fellow student researchers and this was important for two reasons:
 1. MIMIC-III contains high-temporal resolution data including lab results, electronic documentation, bedside monitor trends and waveforms, which makes it one of the most thorough databases of healthcare information related to ICU patient hospital stays. Given the difficulty of finding and gaining permission to do research on actual patient data, access to MIMIC-III gives students exposure to healthcare information that might otherwise be nearly impossible to get.
 1. To gain access to MIMIC-III, students needed to complete a series of courses written by MIT dealing with laws and ethics of human research and the MIMIC-III database. These are housed on the CITI Program website and Kennesaw State University (KSU) provides free access to CITI-based courses for KSU-related projects so students can take the MIT courses, too, and gain access to MIMIC-III. (https://about.citiprogram.org/en/homepage/)

## Code Examined
AS stated, the Python code used by Cornell University researchers Hrayr Harutyunyan, Hrant Khachatrian, David C. Kale, Greg Ver Steeg, and Aram Galstyan was located in this repository https://github.com/YerevaNN/mimic3-benchmarks. The amount of code used in their project was massive and a colleague, who is a consultant providing code review and trouble-shooting, explained it would take him three months just to review the code. For example, the mimic3models file (https://github.com/YerevaNN/mimic3-benchmarks/tree/master/mimic3models) contained ~20 subfolders. Working it together, it took 90-minutes to "walk-through" or dissect the first 50 lines of the Python code of one of those subfolders, "preprocessing.py" (https://github.com/YerevaNN/mimic3-benchmarks/blob/master/mimic3models/preprocessing.py).it would take him 3-montwith expertise in C and C# and with a career as a code reviewer and trouble-shooter reviewed code as a consultant, it would taken him 3-months to have reviewed each folder andAfter cloning the repository and downloading it to my Their Python scripts were used to build machine learning (ML) datasets from the MIMIC-III database so healthcare researchers using data analytics based on ML would have a standard against which to test their own and newer methods. Prior to their efforts, there were no benchmark sets based on publicly available healthcare data and the absence of such cases hampered discoveries waiting in the vast amounts of patient data rapidly accumulating and otherwise available to data miners. 

An article derived from their research is published here: (https://arxiv.org/abs/1703.07771) and their code repository is found here:  

## Process Used
After reviewing Harutyunyan, et al's article, examination of the MIMIC-III-benchmarks began and took multiple hours. 

To demonstrate how the Python code worked, this project followed the instructions in the original repository where, unfortunately, mistakes and a few hiccups occurred. 

## Mistakes and "Regrets, I've Had a Few..." 
### (from Frank Sinatra's, "My Way")
1. Downloading the entire MIMIC III database was a pain because of the file type
 1. The original file type from the 
1. The requirements on how to run the scripts really do require NumPY and Pandas.





 



