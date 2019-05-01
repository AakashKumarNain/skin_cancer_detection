There are three notebooks which are required to run the project from end-to-end. The order should be the same
as described here. 

* `EDA.ipynb:` This notebook gives you an overview of the data. The preprocessing required before modelling is also
described in this notebook with detailed explanation in the notebook itself. 

* `skin_cancer_model.ipynb:` This notebook contains all the code required for building and training the model after the data
has been preprocessed. One of the best things about this notebook and the next one is that you can directly run these on `Google Colab` without changing anything. Just make sure that the data is on your drive.

* `model_conversion.ipynb:` This is the final notebook. Once you have saved your `tf.keras` model to your drive, you can then load the model in this notebook and directly convert it to `tflite` format. I made this as a separate notebook becuase some functionalities of `tflite converter` aren't available in tf-2.0 alpha, hence I had to use a `tf-2.0 nighly` version.  
