1. DONE Get Professor Thomas approval of the Benchmarking project	so I can get started (I, Patricia, completed all tasks so I'm not adding my name to the rest of these tasks)
2. DONE Read the  Benchmark article and analyze these two links to get an understanding of machine learning, benchmarking and the intent of the Cornell Researchers' project https://github.com/YerevaNN/mimic3-benchmarks/commit/e70a7554bb5a39fb8483f1108936fb3df0a4930e  and	
https://github.com/YerevaNN/mimic3-benchmarks/commit/59b5559141eb3f9cf468e416d7ac760a45e64d7e	
3. DONE Assess completion of Project Week 1 Tasks so the project is on time and move to Test 1 
4. DONE Examine the mimic3-benchmarks helper tools 	to understand what helper tools generally do, how they impact the scope of this class project, and how they impacted the original Benchmark project	Done
5. DONE Explore the types and numbers of subfolders under the  mimic3-benchmarks/mimic3models/ file to assess the project scope
6. DONE Analyze line-by-line the preprocessing.py file under mimic3-benchmarks/mimic3models/ file	to help determine if the scope of the project is manageable
7. DONE Assess completion of Project Week 2 Tasks in order to stay on task and so I can take Test 2
8. DONE Create projectroadmap.md to stay in compliance with Project Week 2 tasks
9. Apply features from the Mastering Markdown cheatsheet 	in order to stay in compliance with Project Week tasks 
10. DONE Ask Professor Thomas for a change in scope	in order to produce an attainable project with time and resources avaialble. 
11.Review time, computing, and technical know-how requirements  for running benchmark and making a powerpoint to create a plan for 3 July completion. 
12. DONE Download MIMIC-III .csv files	so Steps 1-6 benchmarking steps can be done
13. DONE Step 1: Clone the repo by following these step:
    13. a. git clone https://github.com/YerevaNN/mimic3-benchmarks/
    13. b. cd mimic3-benchmarks/
14. Step 2: The following command takes MIMIC-III CSVs, generates one directory per SUBJECT_ID and writes ICU stay information to data/{SUBJECT_ID}/stays.csv, diagnoses to data/{SUBJECT_ID}/diagnoses.csv, and events to data/{SUBJECT_ID}/events.csv. This step might take around an hour. (python -m mimic3benchmark.scripts.extract_subjects {PATH TO MIMIC-III CSVs} data/root/)
15. The following command attempts to fix some issues (ICU stay ID is missing) and removes the events that have missing information. About 80% of events remain after removing all suspicious rows (more information can be found in https://github.com/YerevaNN/mimic3-benchmarks/blob/master/mimic3benchmark/scripts/more_on_validating_events.md. (python -m mimic3benchmark.scripts.validate_events data/root/)
15. Step 3: The next command breaks up per-subject data into separate episodes (pertaining to ICU stays). Time series of events are stored in {SUBJECT_ID}/episode{#}_timeseries.csv (where # counts distinct episodes) while episode-level information (patient age, gender, ethnicity, height, weight) and outcomes (mortality, length of stay, diagnoses) are stores in {SUBJECT_ID}/episode{#}.csv. This script requires two files, one that maps event ITEMIDs to clinical variables and another that defines valid ranges for clinical variables (for detecting outliers, etc.). Outlier detection is disabled in the current version. (python -m mimic3benchmark.scripts.validate_events data/root/)
16. Step 4: The next command splits the whole dataset into training and testing sets. Note that the train/test split is the same of all tasks. (ython -m mimic3benchmark.scripts.split_train_and_test data/root/)
17. Step 5: The following commands will generate task-specific datasets, which can later be used in models. These commands are independent, if you are going to work only on one benchmark task, you can run only the corresponding command.

python -m mimic3benchmark.scripts.create_in_hospital_mortality data/root/ data/in-hospital-mortality/
python -m mimic3benchmark.scripts.create_decompensation data/root/ data/decompensation/
python -m mimic3benchmark.scripts.create_length_of_stay data/root/ data/length-of-stay/
python -m mimic3benchmark.scripts.create_phenotyping data/root/ data/phenotyping/
python -m mimic3benchmark.scripts.create_multitask data/root/ data/multitask/
18. Complete Project Week 3 Tasks 
19. DONE Clarify the format of my final presentation in Teams or emails to Prof Thomas
20. Complete presentation with Voiceover
21. Upload presentation
