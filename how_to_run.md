# Detailed steps to make sure that results are **reproducible**
All the work done for this project is divided into three notebooks:
* **EDA**: An explorartory analysis of data and some preprocessing
* **skin_cancer_model:** A detailed notebook for building and training model
* **model_convert:** Notebook for converting keras model to tflite model

All notebooks were made in **Google Colab**, hence you can directly open the notebooks in **Colab playground**.

## Dataset Preparation
1) Download the dataset from [Kaggle]() and unzip it
2) Run the notebook **EDA.ipynb** to segregate data into `train` and `validation` sets. Each set contains images from
different categories in different subfolders. Your data should be arranged like this now:
```
   data
     |__train
        |_akiec
        |_bkl
        |_bcc
        |_df
        |_mel
        |_nv
        |_vasc
        
     |__valid
        |_akiec
        |_bkl
        |_bcc
        |_df
        |_mel
        |_nv
        |_vasc
```
3) There will be another folder created for augmentation names as `final_aug`. This is the directory where the augmentation
images has been generated. I have created this folder separately instead of directly saving the augmented images in the train
