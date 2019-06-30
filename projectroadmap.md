1. DONE Get Professor Thomas approval of the Benchmarking project	so I can get started 
2. DONE Read the  Benchmark article and analyze these two links to get an understanding of machine learning, benchmarking and the intent of the Cornell Researchers' project 
[GitHub] https://github.com/YerevaNN/mimic3-benchmarks/commit/e70a7554bb5a39fb8483f1108936fb3df0a4930e  	
[GitHub] https://github.com/YerevaNN/mimic3-benchmarks/commit/59b5559141eb3f9cf468e416d7ac760a45e64d7e	
DONE Assess completion of Project Week 1 Tasks so the project is on time and move to Test 1 

- [ ] task 1
Evaluate these two links: 
https://github.com/YerevaNN/mimic3-benchmarks/commit/e70a7554bb5a39fb8483f1108936fb3df0a4930e  
https://github.com/YerevaNN/mimic3-benchmarks/commit/59b5559141eb3f9cf468e416d7ac760a45e64d7e
Here are the required steps to build the benchmark. It assumes that you already have MIMIC-III dataset (lots of CSV files) on the disk.

Clone the repo.

git clone https://github.com/YerevaNN/mimic3-benchmarks/
cd mimic3-benchmarks/
The following command takes MIMIC-III CSVs, generates one directory per SUBJECT_ID and writes ICU stay information to data/{SUBJECT_ID}/stays.csv, diagnoses to data/{SUBJECT_ID}/diagnoses.csv, and events to data/{SUBJECT_ID}/events.csv. This step might take around an hour.

python -m mimic3benchmark.scripts.extract_subjects {PATH TO MIMIC-III CSVs} data/root/
The following command attempts to fix some issues (ICU stay ID is missing) and removes the events that have missing information. About 80% of events remain after removing all suspicious rows (more information can be found in mimic3benchmark/scripts/more_on_validating_events.md).

python -m mimic3benchmark.scripts.validate_events data/root/
The next command breaks up per-subject data into separate episodes (pertaining to ICU stays). Time series of events are stored in {SUBJECT_ID}/episode{#}_timeseries.csv (where # counts distinct episodes) while episode-level information (patient age, gender, ethnicity, height, weight) and outcomes (mortality, length of stay, diagnoses) are stores in {SUBJECT_ID}/episode{#}.csv. This script requires two files, one that maps event ITEMIDs to clinical variables and another that defines valid ranges for clinical variables (for detecting outliers, etc.). Outlier detection is disabled in the current version.

python -m mimic3benchmark.scripts.extract_episodes_from_subjects data/root/
The next command splits the whole dataset into training and testing sets. Note that the train/test split is the same of all tasks.

python -m mimic3benchmark.scripts.split_train_and_test data/root/
The following commands will generate task-specific datasets, which can later be used in models. These commands are independent, if you are going to work only on one benchmark task, you can run only the corresponding command.

python -m mimic3benchmark.scripts.create_in_hospital_mortality data/root/ data/in-hospital-mortality/
python -m mimic3benchmark.scripts.create_decompensation data/root/ data/decompensation/
python -m mimic3benchmark.scripts.create_length_of_stay data/root/ data/length-of-stay/
python -m mimic3benchmark.scripts.create_phenotyping data/root/ data/phenotyping/
python -m mimic3benchmark.scripts.create_multitask data/root/ data/multitask/
powerpoint (remember) 
