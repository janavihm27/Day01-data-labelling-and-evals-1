1. What is a manifest?

A manifest is a file that stores all the important information about each row in a dataset. It tells us the information such as source, what label it has and whether it can be used for training. It helps us keep the dataset organized and understand which data is correct and which data should not be used for training.

2. Why do rejected rows stay in the file?

Rejected rows stay in the file because they help us understand why some data was not selected for training. Instead of deleting them, we keep them to check what went wrong and identify mistakes. This helps us maintain the data properly and makes it easier to check the results later.

3. Why does the second run get a new folder?

The second run gets a new folder because we should not overwrite the results of the previous run. Every run is saved in a separate folder so that the old files remain safe. This helps us compare the results of different runs and check whether any changes have happened. It also makes it easier to track our work.

4. Which two statuses are trainable, and why is unmatched not one of them?

The two trainable statuses are matched and no_positive. 
    * In matched the generated label correctly matches an existing box so the data is properly labelled. 
    * In no_positive there is no object to mark, and this is also a correct result. Both can be used for training because they represent correct information.
    * Unmatched is not trainable because the generated label did not match any existing box. If we use it for training, the model may learn incorrect information.