# Final Project ID Bootcamp

The goal of this project is to create a prediction model for cancer detection.
As cancer is a very complicated condition due to its variability depending on the area affected, I decided to focus on a specific area of the body.
I focused on lung cancer. For this I gathered data from National Lung Screening Test(NSLT), a test conducted on patients that had to be smokers in the previous 15 years.

## Information 
  The data was divided in multiple sections:
### Data sets
  There are 5 different data sets:  
    ```The first gives the personal information and summarize data of each patient;  
    ```The second has the information about the type of screening the patient received;  
    ```The third shows the results found from the screening type;  
    ```The fourth compares the results found in the previous data set to see abnormal growths;  
    ```The final data set has all the information about the cancer that the patient has.  

There are multiple columns that are shared between each data sets and that is what I used to merge them. 
### Merging data sets
Merging the data caused some complications.
As the data sets were merge by using a specific column and I wanted to retain the information from both datasets, it created some duplication of the patients.
This is due to the columns used went from one to many. There were several uses of the ID column in all the data sets except the first one where it gave the information of the patients. 
This was a problem that I later realised was not so consequential, as one of the columns (size of the mass detected) was set to 0 for the patients with out cancer. 
When doing the confussion matrix, the column for the size of mass detected was not a 1:1 indicator of cancer as some patients had masses that were not cancer. It was an indicator of no cancer if 0 was the value.
This allowed me to train the model on only the patients with a mass detected which in turn made the model more accurate to determine which stage of cancer each patient was on. 

### Images
  The NLST also has some images of the screenings that show the cancers and other growths.
  The idea is to implement a neural network to process the images and gather the information directly from the images instead of the datasets.

"# Final-Project-ID-Bootcamp" 
