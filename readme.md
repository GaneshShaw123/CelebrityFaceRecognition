# CelebrityFaceRecognition
we are beginning end to end machine learning project or data science project for sports celebrity image classification.We will try to classify an image of my favourite 5 sports people.

There are 4 different ways of collecting data for our project,
(1) Manually download images from google images
(2) Use python and web scrapping to automate downloading images from google.
(3) Use a chrome extention called fatkun.
(4) Buy these images from third party vendor who is selling images database. Sometimes if a company is in sports or news domain they might have internal database of these images. You can work with engineering team that owns that database and get an access of those images.

In the next step, we are going to clean images that we downloaded from google in a way that it is suitable to train our classifier. We mostly identify a person in a photo with a face. Hence we will use opencv and a technique called haar cascades to detect if a face and two eyes are clearly visible or not. If they are than we keep the image otherwise we discard the image. Majority of the data cleaning work will be done using python code but there will be some cleaning work that we will have to do manually. 
Now, we will use cropped images and apply wavelet transform to extract meaning features that can help with image identification. we need to understand many important concepts such as time vs frequency domain, fourier transform, representing images as frequency etc. USing wavelet transform and a raw pixel image we will create our X and use class labels as y. These X and y will be used for model training. Feature engineering techniques in this tutorial will enhance your understanding on how they can be used to create powerful prediction function.

Once we have X and y after applying feature engineering techniques, we can now create simple SVM model to get a feel of how it is going to perform on image classification. We will then use GridSearchCV and try different models with different hyper parameters to come up with a best model that can give us maximum accuracy. We will use sklearn classification_report to check the performance. Once we select best model based on GridSearchCV we can evaluate it on X_test and y_test to get a feel of how it is going to perform in production. Confusion matrix is used with seaborn visualization to get an understanding of classification errors for each of the classes. In the end we export the model to a file using joblib.

Python flask is a light weight web server. In the next step, we will write a flask server that will use the trained model and perform image classification. UI will talk to this backend server and perform image classification task for our sports person identification project. At the end of this we will have fully functioning python flask server or backend ready that UI can talk to. 

Now, we will build a website for our project. This website have an area where someone can drag and drop an image of a person and it will identify that person. The image classification is restricted to only 5 classes or 5 sports people. We will use HTML/CSS/Javascript for this project. JQuery is used to make http calls to python flask backend. 

Now at the end we can deploy this project on Amazon EC2, Google cloud or Heroku.
