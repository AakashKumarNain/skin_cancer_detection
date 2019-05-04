# TF Lite Android Skin Cancer detection App

A simple Android example that demonstrates skin cancer classification using `tflite` and `gpu-delegates`

## Building in Android Studio with TensorFlow Lite AAR from JCenter.
The build.gradle is configured to use TensorFlow Lite's nightly build.


## Build procedure
Here we are using the `gpu-delegates 0.0.0`, which was first experimental version. There is a newer version as well but with huge changes. As of now, we will work with the older version. You need to do follow these steps:
     
* Step 1. Clone the TensorFlow source code and open it in Android Studio

        git clone https://github.com/tensorflow/tensorflow

 * Step 2. Edit app/build.gradle to use the nightly GPU AAR. Add the tensorflow-lite-gpu package alongside the existing tensorflow-lite package in the existing dependencies block. Please make sure you have correct version of `Android SDK`

            dependencies {
                ...
                implementation 'org.tensorflow:tensorflow-lite:0.0.0-nightly'
                implementation 'org.tensorflow:tensorflow-lite-gpu:0.0.0-nightly'
            }

* Step 3. Build and run
Run → Run ‘app’. When you run the application you will see a button for enabling the GPU. You can toggle between `CPU` and `GPU`. You will see the performance difference between both.
