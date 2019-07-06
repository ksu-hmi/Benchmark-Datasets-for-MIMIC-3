# Demonstrating How MIMIC-III Benchmarks Run in Python
The Medical Information Mart for Intensive Care III (MIMIC-III) is one of the largest and most publically accessible critical care unit databases in the world, containing scrubbed health-related data of ~ 60,000 pediatric and adult patients who stayed in critical/intensive care units at the Beth Israel Deaconess Medical Center between 2001 and 2012. The MIMIC-III database is described in detail here: (https://mimic.physionet.org/about/mimic/)  MIMIC-III is the third collection of ICU data organized and maintained by the Laboratory of Computational Physiology at MIT, in conjunction with Philips Medical Systems, and Beth Israel Deaconess Medical Center (BIDMC) (https://link.springer.com/chapter/10.1007/978-3-319-43742-2_5).  

## What Makes this a Worthwhile Final Project
MIMIC-III is a database in which I have been certified to work since August, 2018. For reasons outside the scope of the HMI 7540 course, my exposure to MIMIC-III has  been limited. However, one of the goals of my graduate research professor for FAll, 2019 is that we apply Python Code and machine learning technologies to the research we are planning in the MIMIC-III database. The timing of this class project presented  a opportunity that combined all three of these elements.

A GitHub search for potential topics uncovered a project using Python Code, machine learning, and the MIMIC-III database by four Cornell University researchers: Hrayr Harutyunyan, Hrant Khachatrian, David C. Kale, Greg Ver Steeg, and Aram Galstyan. Their work was located in this repository https://github.com/YerevaNN/mimic3-benchmarks called "Python suite to construct benchmark machine learning datasets from the MIMIC-III clinical database." Their research was published in the article, "Multitask Learning and Benchmarking with Clinical Time Series Data" (https://arxiv.org/abs/1703.07771). The authors encouraged others to reproduce their benchmarks using their code in the master branch and stated in their paper that no "extensive knowledge of medicine or clinical data" was needed. Their only cavaet was each researcher needed to download the MIMIC-III files on their own.  

Also, selecting this for the class project introduced fellow students to MIMIIC-III and this was benefical for two reasons:
 1. MIMIC-III contains high-temporal resolution data from actual patients and this is often difficult to gain access to  
 1. Secondly, students can gain access to MIMIC-III by completing a series of nine courses from MIT, which are housed on the CITI Program website (https://about.citiprogram.org/en/homepage/). Kennesaw State University (KSU) provides free access to CITI-based courses. 

## Summary of the Original Research Purpose
Harutyunyan and his colleagues used Python scripts to help "compile a subset of the MIMIC-III database with more than 31 million clinical events from 42,276 [intensive care unit] ICU stays of 33,798 unique patients." Using this subset, they defined "four clinical predication tasks"  previously identified as the premium areas in which data analytics could make a significant impact. These four areas include:
 1. in-hospital mortality prediction
 1. physiological decompensation prediction
 1. length-of-stay prediction
 1. phenotype classification
 
Theirs were the first publicly available clinical prediction data sets or benchmarks. Prior to this, there were no publicly available benchmarks. Their theory was that the absence of readily available benchmarks handicapped the development of machine learning models in healthcare research, which led to underexamined patient data that was accumulating due to the increasing adoption of electronic health records (EHRs). 
 
## Process Used and Code Examined 
My intention for this project was to  follow the authors' suggestion to duplicate the creation of the benchmarks. After a read-through of their article,  the next step was to examine the whole MIMIC-III-benchmarks repository.  (https://github.com/YerevaNN/mimic3-benchmarks) This required various types of study over the course of days. For instance, I started with READMe and then began looking at the .py code in the mimic3models file and subfolders. The code was detailed.  As an example, the mimic3models file (https://github.com/YerevaNN/mimic3-benchmarks/tree/master/mimic3models) contained ~20 subfolders. I opened all of them but examined the preprocessing.py file. (https://github.com/YerevaNN/mimic3-benchmarks/blob/master/mimic3models/preprocessing.py).  It took 90-minutes to "talk-through" or dissect the first 50 lines of the ~231 total lines in "preprocessing.py."   
 
I looked at the other content in the repository, including the Structure section https://github.com/YerevaNN/mimic3-benchmarks#structure and especially the Requirements https://github.com/YerevaNN/mimic3-benchmarks#requirements and Building A Benchmark portion.  https://github.com/YerevaNN/mimic3-benchmarks#building-a-benchmark. I missed an important step and that was clicking on the chat-gitter button. And, unfortunately, things did not go as planned.

## "Regrets, I've Had a Few..." 

1. Downloading the 26 tables of the MIMIC III database took time but ran smoothly. However, opening the files took time because they are stored as .tar.gz files. I used a free version WinZip to open one of the MIMIC tables for a project last fall, but WinZip had caused other issues on my desktop and I wanted to avoid it. I discovered that Windows 10 had a built-in Linux utility that could unpackage .gz files. I followed multiple steps to unpack them using Windows 10. This process took several hours and eventually, I downloaded 7-Zip and  used it to convert the .gz files to .csv files and stored them all on my laptop. 
1. Step 1: Cloning the repository and accessing the mimic3-benchmarks on my home system was easy.
1. Step 2: My project never made it past this point. Here's why:
   1. The Requirements state: "Specifically, download the CSVs. Otherwise, generally we make liberal use of the following packages:numpy and pandas." To me, that read: "You have to download the CSVs. Otherwise, even though we used numpy and pandas, athough we used numpy and pandas, and other statistical packages for other parts of our study, you don't need them if all you're going to do is build the benchmarks. So, download the CSVs and run the Python scripts in Steps 2-6 and you'll see how to build the benchmarks." 
   1. I should have just downloaded NumPY and Pandas from the start because when I ran the script found in Step 2: [python -m mimic3benchmark.scripts.extract_subjects {PATH TO MIMIC-III CSVs} data/root/], I got the error message that "numpy" could not be located. I used a "pip install" command on the CMD prompt and downloaded them both.
   1. With those packages installed, the same script was run again. This time, the  error message was that "YAML" could not be found.
   1. I researched YAML to find out what this package was and it seemed that it didn't even work with the version of Python that was located on my laptop. 
   1. To be sure it was used in the extract_subjects.py file, I used IDLE to open the extracts_subjects.py file to see if YAML was used in the code and it was. So YAML was installed via pip at the CMD prompt just like the previous two packages.
   1. The script in Step 2 was run again. This time, the script it appeared to run - appeared to run until another error message popped out. This one was: "extract_subjects.py: error: the following arguments are required: output_path". Switching to the Anaconda command prompt produced the same error. 
   1. I attempted to run the script from IDLE and that produced a syntax error, too. I was running out of time to figure it out.  
1. The Structure section did not provide me with the help I needed though those resources were reviewed. https://github.com/YerevaNN/mimic3-benchmarks#structure
 
 ## Conclusions
1. Tenacious effort was applied towards attempting to duplicate the benchmark building as outlined in Steps 1-2. Too late, I resourced the "chat on gitter", the public channel for the mimic3-benchmarks project (https://gitter.im/YerevaNN/mimic3-benchmarks?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge) and found that other people had the same experiences as I was having and that some errors had been added to the mimic3-benchmark file by the authors, themselves. I wish I'd been more careful in my examination of that repository - every part of it. 
1. I didn't understand how to interpret and fix some of the error messages (i.e., output_path) or to understand what error messages could have been fixed by adjusting the code that existed.
1. The authors needed to be more thorough with their requirements and their own commits, according to what I read on the chat gitter - though, again, my limited experience with Python got in the way. However, it would have helped to have clear requirements for all the packages that were needed, like YAML, which was not mentioned anywhere.
1. I did learn a lot through trial and error. It is disappointing that I could not get the steps completed by the project deadline and it seems after reviewing the chat gitter files that I needed more time and more help in figuring this out. I would like to run these benchmarks; some people in chat-gitter did get further ahead than I did. I hope that getting the  KSU certificate in Python, which I am now registered in, will give me more background. And, it would have been more fun to have worked with a team. 





 



