### Build an American Sign Language alphabet classifier using pytorch and GPU environments on WatsonX 


# Overview

we will use PyTorch to build and train a deep learning model to classify images to 29 classes (26 ASL alphabet, space, Del, and nothing) which can be used later to help Deaf peope communicate with other and maybe with computers as well. We will use a pre-trained mobile network and we will define our classifier and connect it to network, then train this classifier along with some of the last blocks of the network on our dataset.

In this notebook we will:

1- Obtain dataset from Kaggle.  
2- explore data and define transformers to preprocess images before training.  
3- define our classifier to have an output layer of 29 outputs.  
4- train the last blocks of the network along with the classifier we defined.  
5- test the model we trained.  

This notebook uses python 3.6 + GPU environment which allow us to do the whole process and train complex model in the same place which is a notebook in WatsonX.
Learn more about available environments <a href="https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/gpu-environments.html"> WatsonX environments.</a>




# Instructions


1. [Sign up for WatsonX](#1-sign-up-for-watson-studio)
2. [Create a new project](#2-create-a-new-project)
3. [Create the notebook](#3-create-the-notebook)
4. [Run the notebook](#4-run-the-notebook)
5. [Test your model](#5-Test-the-model)

### 1. Sign up for WatsonX

We will use WatsonX to run this notebook, WatsonX is available through IBM cloud.

* To start you must have IBM cloud account, Get your for free <a href="https://cloud.ibm.com/registration">Here.</a>   
* From the catalog create a <a href="https://cloud.ibm.com/catalog/services/watsonx">WatsonX</a> with standard plan or more and make sure the region is dallas to enable GPU environment.  



https://github.com/ArvyKR/ASL-Pytorch/assets/95832640/4f13d6b7-59be-4202-b492-bf78f69f9c5a

pilih Get started pada pilihan watsonx.ai
![image](https://github.com/ArvyKR/ASL-Pytorch/assets/95832640/6366965c-aeec-451e-9c4d-3fea78f59ffd)

Selanjutnya pilih Dallas (us-south) sebagai region default yang akan digunakan dan Create an IBM Cloud account.
![image](https://github.com/ArvyKR/ASL-Pytorch/assets/95832640/10e5eece-fedf-44e9-93b9-cb589f7f53fe)

Lengkapi seluruh account information yang dibutuhkan, gunakan email student (email IL).
![image](https://github.com/ArvyKR/ASL-Pytorch/assets/95832640/a21072bd-18d0-42ca-85fa-42138d6830cf)

Cek inbox Webmail email student (email IL) untuk mendapatkan kode verifikasi dari IBM.
![image](https://github.com/ArvyKR/ASL-Pytorch/assets/95832640/ece369bf-d493-4ed7-9bb9-91b0266671ef)

Untuk Personal information bisa diisi dengan nama kampus masing-masing student.
![image](https://github.com/ArvyKR/ASL-Pytorch/assets/95832640/f765723e-cf12-4724-8ac1-fd26349f2bc1)

Setelah seluruh informasi telah diisi, click Continue dan ceklis box yang ada seperti di gambar dan click Continue sekali lagi.
![image](https://github.com/ArvyKR/ASL-Pytorch/assets/95832640/4e68b50a-56e2-4733-8dc2-202389456e1c)
![image](https://github.com/ArvyKR/ASL-Pytorch/assets/95832640/be22a165-71f4-474c-bac7-f3932699ba7e)



### 2. Create a service
Back to IBM Cloud home page create Cloud Object Storage service by searching `Object Storage`.

https://github.com/ArvyKR/ASL-Pytorch/assets/95832640/39486e6d-1d2e-4c0a-b315-b5b590f98dde


and then go to WatsonX home page, go to Menu -> Administration -> Services -> Service Catalog, create service `Watson Machine Learning` and `Watson Studio`.

![SERVICE](https://github.com/ArvyKR/ASL-Pytorch/assets/95832640/c45bc32d-9394-4ddf-be49-a92e63862457)
![image](https://github.com/ArvyKR/ASL-Pytorch/assets/95832640/7e3102b6-ea3a-4414-867d-8bc6039bfd5f)



### 3. Create the notebook 

* create a new notebook from WatsonX with GPU support.    
    * the notebook should have a GPU support <a href="https://www.youtube.com/watch?v=RNIWtpnNBoo">click here to learn how to create a notebook with GPU support.</a>
    * Use the From URL option and    
    use this URL for GPU supported notebook: https://github.com/IBM/ASL-Pytorch/blob/master/ASL-GPU.ipynb \
    or use this URL for CPU notebook(LITE) : https://github.com/IBM/ASL-Pytorch/blob/master/ASL-CPU.ipynb

![NOTEBOOK](https://github.com/ArvyKR/ASL-Pytorch/assets/95832640/ea55b61a-38a7-46f6-ab7f-6c78465cdd3e)


### 4. Run the notebook 

To view your notebooks, select `Notebooks` in the project `Assets` list. To run a notebook, simply click on the `edit` icon listed in the row associated with the notebook in the `Notebooks` list.

![ASL notebook](https://github.com/IBM/ASL-Pytorch/blob/master/images/note.png)

Follow notebook instructions to load data and train the model.  

Cells are how notebooks are structured and are the areas where you write your code. To run a piece of code, click on the cell to select it, then press `SHIFT+ENTER` or press the play button in the toolbar above. Additionally, the Cell dropdown menu has several options to run cells, including running one cell at a time or to run all cells at once.

### 4. Test the model

The last two cells in the notebook is where we test our trained model.
run the last model many times to check different samples.

![Result](https://github.com/IBM/ASL-Pytorch/blob/master/images/result.png)







