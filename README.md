# Demonstrating How MIMIC-III Benchmarks Run in Python
The Medical Information Mart for Intensive Care III (MIMIC-III) is one of the largest and most publically accessible critical care unit databases in the world. It contains scrubbed health-related data of ~ 60,000 pediatric and adult patients who stayed in critical/intensive care units (CCUs or ICUs) at the Beth Israel Deaconess Medical Center between 2001 and 2012. The MIMIC-III database is created from information such as “demographics, vital sign measurements taken at bedside, laboratory test results, procedures, medications, caregiver notes, imaging reports, and mortality (both in and out of hospital).” (https://mimic.physionet.org/about/mimic/) Its data are housed in 26 tables with additional derived tables.  MIMIC-III represents the third collection of ICU data organized and maintained by the Laboratory of Computational Physiology at MIT, in conjunction with Philips Medical Systems, and Beth Israel Deaconess Medical Center (BIDMC) (https://link.springer.com/chapter/10.1007/978-3-319-43742-2_5).  

## What Makes this a Worthwhile Final Project
MIMIC-III is a database in which I have been certified to work since August, 2018. For reasons outside the scope of the HMI 7540 course, my exposure to MIMIC-III has heretofore been limited. However, the opportunity to work with it in this type of project environment comes at a good time because my graduate research professor wants us to use Python for studies within MIMIC-III beginning in the Fall 2019 semester.

Additionally, introducing MIMIIC-III to fellow student researchers is important for two reasons:
 1. Once a series of courses has been completed through the CITI Program, students have ready access to this database. (https://about.citiprogram.org/en/homepage/)
 1. MIMIC-III contains high-temporal resolution data including lab results, electronic documentation, bedside monitor trends and waveforms, which makes it one of the most thorough databases of healthcare information related to ICU patient hospital stays. Given the difficulty of finding and gaining permission to do research on actual patient data, access to MIMIC-III gives students exposure to healthcare information that might otherwise be nearly impossible to get.  

## Code Examined
To introduce MIMIC-III to my colleagues and to illustrate the use of Python code, this project examined and replicated the Python code used by Cornell University researchers Hrayr Harutyunyan, Hrant Khachatrian, David C. Kale, Greg Ver Steeg, and Aram Galstyan. Their Python scripts were used to build machine learning (ML) datasets from the MIMIC-III database so healthcare researchers using data analytics based on ML would have a standard against which to test their own and newer methods. Prior to their efforts, there were no benchmark sets based on publicly available healthcare data and the absence of such cases hampered discoveries waiting in the vast amounts of patient data rapidly accumulating and otherwise available to data miners. 

An article derived from their research is published here: (https://arxiv.org/abs/1703.07771) and their code repository is found here: (https://github.com/YerevaNN/mimic3-benchmarks). 

## Process Used
After reviewing Harutyunyan, et al's article, examination of the MIMIC-III-benchmarks began and took multiple hours. For example, the mimic3models file (https://github.com/YerevaNN/mimic3-benchmarks/tree/master/mimic3models) contained ~20 subfolders. It took 90-minutes to understand the first 50 lines of the Python code of one  subfolder, "preprocessing.py" when it was examined line-by-line (https://github.com/YerevaNN/mimic3-benchmarks/blob/master/mimic3models/preprocessing.py).

To demonstrate how the Python code worked, this project followed the instructions in the original repository where, unfortunately, mistakes and a few hiccups occurred. 

# Mistakes and "Regrets, I've Had a Few..." ###(from Frank Sinatra's, "My Way")
1. Downloading the entire MIMIC III database was a pain because of the file type
 1. The original file type from the 
1. The requirements on how to run the scripts really do require NumPY and Pandas.





 



