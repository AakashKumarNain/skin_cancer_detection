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
images has been generated. I have created this folder separately instead of directly saving the augmented images in the `train` directory so that you can see whether there is no problem with the augmented images. **Debugging augmentation is one of the hardest part. It is always better to look for the data you are augmenting**. Once you have verified the images, copy the augmented images from the `final_aug` to `data/train` folder. Make sure that you copy images folder wise carefully.

4) Once you are done with the above step, make a `tar` file like this:
    `tar -zcvf data.tar.gz data`
5) Upload this file to your drive and then you can proceed to `skin_cancer_model.ipynb` and `model_convert.ipynb` in the respective order.

**Why not scripts? Why notebooks?**
I take reproducibility of ML models very serioulsy. The whole purpose of notebooks in the first place is to make this interactive so that you can see the diferences in the result on the fly. This helps you debug things in a more flexible way. **Once everything is verified, you can turn your notebook into script, refactor it and run it accordingly.** I didn't do it because I don't like to do to much of refactoring until unless I am running things on production. Also, as I have been putting models into production for a long time, I am used to look for every minute detail in the scripts which is time consuming. Hence, I took the notebooks path.
