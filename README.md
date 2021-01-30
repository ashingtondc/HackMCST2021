# HackMCST2021
Image Recognition Workshop for Hack MCST 2021

Instructions
1. Create [Clarifai](https://www.clarifai.com/) account.
1. Download this repository to your desktop.
1. In Clarifai, create a new application. Name it whatever. Use the **General** preset.
1. Click **Explorer** on the left sidebar.
1. Click **Add Inputs** at the top right.
1. Upload the images in the _training_ folder of the downloaded data.
1. Go back to the **Explorer**.
1. In the left pane, click **Add Concept to Model**.
1. Add the following concepts:
    1. us-dollar
    1. mexican-peso
    1. canadian-dollar
    1. euro
    1. british-pound
1. In the left pane, click **Create New Model**.
    1. Choose _Context-based Classifier_
    1. Set the _Model ID_ as **currency-classifier**.
    1. Click _Select all concepts_
    1. Set _OUTPUT_INFO.OUTPUT_CONFIG.CONCEPTS_MUTUALLY_EXCLUSIVE_ to **YES**.
    1. Set _OUTPUT_INFO.OUTPUT_CONFIG.EMBED_MODEL_VERSION_ID_ to the first option in the dropdown.
    1. Click **CREATE MODEL**.
1. Go back to the **Explorer**.
1. Start going through the images and label them.
    1. If the current image is a US Dollar for example, click the **check** next to _us-dollar_ and the **X** next to the rest of the labels.
1. After all of the images are labeled, click **Train**.
1. Just like in Step 5, now upload the images in the _test_ folder of the downloaded data.
1. Go back to the **Explorer**.
1. Do not label these images. Instead, simply click through them. Since your model has been trained, it will now perform predictions on the new images it has not seen before (unlabeled images). 
1. Your model is exposed via an API to be used in your applications. I have created a Google Colaboratory [notebook](https://colab.research.google.com/drive/1b0ZPXQQff1dAOoq-jFVX8ARn6pvpFfzZ?usp=sharing) containing example code to show how this might be done in Python. 
    1. This is a Jupyter Notebook - a very useful and prominent tool in Data Science. 
    1. Create a copy of the notebook in order to edit and save. 
    1. The notebook is pre-filled with my working model's API key and a test [image](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT6qk7wJjNtRGDPhVqf83SzXFpzMdBH30E2WA&usqp=CAU).
    1. Substitute *my_api_key* with your model's API key (found in left side pane -> Application Details -> API Keys).
    1. Substitute *image_url* with the URL to any image you want to predict using the model.
    1. To run the cells, press Shift+Enter or click the play buttons next to each cell. Cells run code in the order in which you click them. You can re-run cells.

* If you want to implement image recognition in your application, this tutorial can serve as a way to get prototyping quickly. For more advanced applications, it would be better to try solutions from any of the leading cloud providers. 
* Hope you enjoyed this hands-on introduction to image recognition!
  
  
