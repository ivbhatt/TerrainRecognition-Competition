# DLNN-ProjC1
Project made as part of ECE542: Deep Learning &amp; Neural Networks; TerrainRecognition

Please refer instructions.txt for running instructions:

instructions:
Link to Dataset (NCSU access) (ECE542_sp2021_Project_TerrainRecognition):
https://drive.google.com/drive/folders/15qAg_VhIEGRIBGc6Uwr-dQssTLlpRNoO?usp=sharing 

=== 1 sync_data.ipynb [compuslory] ===

This notebook synchronizes the x_attributes and y_labels. Details about data-synchronization is presented in report.

Cell 3:
* set INPUT_DIR path to "ECE542_sp2021_Project_TerrainRecognition" provided by teaching staff
* set OUTPUT_DIR_TRAIN to a place where you want to save the synchronized training data-files.
* set OUTPUT_DIR_TEST to a place where you want to save the synchronized testing data-files.

=============================
=== 2 eda.ipynb [optional]===

This notebook has some code that performs exploratory data analysis on the training data provided by teaching staff.

Cell 3:
* set INPUT_DIR path to OUTPUT_DIR_TRAIN produced by sync_data.ipynb

=============================
=== 3 data_augmentation [compulsory for re-train/ optional for generate_preds].ipynb ===

This notebook augments the training data. Details about data-augmentation is presented in report.

Cell 4:
* set INPUT_DIR_TRAIN path to OUTPUT_DIR_TRAIN produced by sync_data.ipynb
* set OUTPUT_DIR_TRAIN to a place where you want to save the augmented training data-files.


=============================
=== 4 data_sampling.ipynb [compulsory for re-train/ optional for generate_preds] ===

This notebook samples the training data to address the imbalanced-classes in the training data. Details about data-sampling is presented in report.

Cell 4:
* set INPUT_DIR path to OUTPUT_DIR_TRAIN produced by data_augmentation.ipynb
* set OUTPUT_DIR to a place where you want to save the balanced training data-files + normalization-information.


=============================
=== 5 train.ipynb [compulsory for re-train/ optional for generate_preds] ===

This notebook trains all our ensemble models. Details about model-training is presented in report.

Cell 3:
* set INPUT_DIR path to OUTPUT_DIR produced by data_sampling.ipynb
* set OUTPUT_DIR to a place where you want to save all the models.


=============================
=== 6 generate_preds.ipynb [compuslory] ===

This notebook samples the training data to address the imbalanced-classes in the training data. Details about data-sampling is presented in report.

Cell 3:
* set MODEL_DIR path to OUTPUT_DIR produced by train.ipynb - where all the models are stored
* set INPUT_DIR path to OUTPUT_DIR_TEST produced by data_sync.ipynb - where all the synchronized test-data is produced
		= you can set this to other data also provided it is first run through data_sync.ipynb & synchronized
* set OUTPUT_DIR to a place where you want to save all the predictions.
* set NORMALIZE_DIR to OUTPUT_DIR produced by data_sampling.ipynb - where normalization data is stored
=============================
