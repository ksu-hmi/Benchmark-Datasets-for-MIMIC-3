# Demonstrating How MIMIC-III Benchmarks Run in Python
The Medical Information Mart for Intensive Care III (MIMIC-III) is one of the largest and most publically accessible critical care unit databases in the world. It contains scrubbed health-related data of ~ 60,000 pediatric and adult patients who stayed in critical/intensive care units (CCUs or ICUs) at the Beth Israel Deaconess Medical Center between 2001 and 2012. The MIMIC-III database is created from information such as “demographics, vital sign measurements taken at bedside, laboratory test results, procedures, medications, caregiver notes, imaging reports, and mortality (both in and out of hospital).” (https://mimic.physionet.org/about/mimic/) Its data is housed in 26 tables and derived tables.  It is the third collection of ICU data organized and maintained by the Laboratory of Computational Physiology at MIT in conjunction with Philips Medical Systems, and Beth Israel Deaconess Medical Center (BIDMC) (https://link.springer.com/chapter/10.1007/978-3-319-43742-2_5).  

MIMIC III is unique for multiple reasons including two that are important for this project:  
 1. •	the database is freely available to researchers worldwide once they complete the CITI “Data or Specimens Only Research” course  (https://about.citiprogram.org/en/homepage/).  
 1. •	MIMIC-III contains high temporal resolution data including lab results, electronic documentation, and bedside monitor trends and waveforms, which makes it one of the most thorough databases of healthcare information from patient hospital stays. 

For these two reasons and others, the MIMIC-III database is an excellent database for student researchers to be made aware of. 

To help introduce MIMIC-III to Cohort #2 and to illustrate the use of Python code  in conjunction with this database, this project examined the work of Cornell University researchers Hrayr Harutyunyan, Hrant Khachatrian, David C. Kale, Greg Ver Steeg, and Aram Galstyan. They used Python code to build machine learning datasets from the MIMIC-III database. An article derived from their research is published here: (https://arxiv.org/abs/1703.07771) and their repository can be found here: (https://github.com/YerevaNN/mimic3-benchmarks). Their benchmarks provided "train and test cases"  to help foster machine learning applications in healthcare research. Historically, there were no benchmark sets based on publicly available healthcare data and the absence of such cases hampered discoveries waiting in the vast amounts of patient data rapidly accumulating and otherwise available to data miners. (https://arxiv.org/abs/1703.07771)

After reviewing Harutyunyan, et al's article, examination of the mimic3-benchmarks began and took several hours. For example, the mimic3models file (https://github.com/YerevaNN/mimic3-benchmarks/tree/master/mimic3models) contained ~20 subfolders. It took 90-minutes to understand the first 50 lines of the Python code of one  subfolder, "preprocessing.py" when it was opened and examined line-by-line (https://github.com/YerevaNN/mimic3-benchmarks/blob/master/mimic3models/preprocessing.py).

To show how benchmarks work using Python code, this project concluded by following the six steps Harutyunyan, et al, provided so others could duplicate their work. 




 



