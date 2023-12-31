1.After I split the datasets into train dataset and test dataset,  in ../data/train_data/sitting/dataset8.csv, we can see that it's jumping from 13250 to 13750, missing one input 13500. I have manually added the 13500 input with the average of both 13250 and 13750 to fill in the missing data. Because I manually changed it, if it does not work, please replace the dataset8 in the folder 'extra' to replace it with the dataset8 under sitting directory inside the train_data folder. Then proceed.

2. After I defined the function summary_table(path) don't run the next couple of lines replace ../data/train_data\bending2\dataset4.csv this dataset with dataset4.csv 
in the extra folder then run. Because For some weird reason, the time for bending2_dataset4 kept being added to another column if I merge them together, so I manually make it back to the correct position, and now we have the finished version of train and test datasets. 

This is a continuation on Project 3 