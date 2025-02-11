# Final Project ID Bootcamp

The goal of this project is to create a prediction model for cancer detection.
As cancer is a very complicated condition due to its variability depending on the area affected, I decided to focus on a specific area of the body.
I focused on lung cancer. For this I gathered data from National Lung Screening Test(NSLT), a test conducted on patients that had to be smokers in the previous 15 years.

---

## 📝 Information 
The data was divided into multiple sections:

### 📊 Data sets
There are 5 different data sets:  
- **[Screening Type](./nlst_780_screen_idc_20210527.csv)** – Information on the screening process used for each patient  
- **[Screening Results](./nlst_780_ctab_idc_20210527.csv)** – What was found on the screenings carried on the patients  
- **[Abnormal Growths](./nlst_780_ctabc_idc_20210527.csv)** – The abnomalities found in the screenings/details about it    
- **[Personal Information](./nlst_780_prsn_idc_20210527.csv)** – Personal information of the patients   
- **[Cancer Diagnosis](./package-nlst-780.2021-05-28/nlst_780/nlst780.idc.delivery.052821/nlst_780_canc_idc_20210527.csv/nlst_780_canc_idc_20210527.csv)** – Details of the cancer types found in patients  

There are multiple columns that are shared between each dataset, which were used to merge them.

---

## 🔀 Merging Data Sets
Merging the data caused some complications.  
Since the datasets were merged using a specific column and I wanted to retain information from both datasets, it created some duplication of patients.  
However, one of the columns (`size of the mass detected`) was set to `0` for patients **without** cancer. This allowed to organize the patients who had a growth to be set apart and use the model only on them.
This gives a more precise model to detect the stage at which the patients´ cancer is at.  

---

## 📂 Jupyter Notebooks
The following notebooks contain different steps that I carried when making the process:

- **[Preprocessing](./PreProcess.ipynb)** – Data cleaning and merging
- **[Data Analysis](./Analisis.ipynb)** – Initial data exploration and visualization  
- **[First Model Try](./First%20try.ipynb)** – First attempt at building a model  
- **[Second Model Try](./Second%20try.ipynb)** – Improved version of the model  
- **[XGBoost Testing](./XGboost%20test.ipynb)** – Testing XGBoost for cancer classification, best results  

---

## 🚀 Future Steps
- Implement a **neural network** to analyze screening images.  
- Use **deep learning** to extract cancer information directly from scans.  
- Improve data preprocessing to handle missing values more efficiently. 

