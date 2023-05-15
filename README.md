## deep_learning_challenge


##Description
In this project, I took a csv file containing more than 34,000 organizations that have received funding for their organization ran multiple deep learning models. The purpose of this project is to create a model that can predict whether applicants will be successful if funding is received. The goal for the model is to predict with an accuracy of 75% or higher. 

#Neural Network Model Report
1.	Overview: The purpose of this project is to create a model that predicts with an accuracy of at least 75%, whether an application will be successful if funding is given. To achieve this goal, multiple models were created and tested in order to find a model with the desired accuracy as the outcome. The final file for this project is the “Starter_Code_kb_fina_jupyter_notebook”. 
2.	Results:
a.	Preprocessing:
    •	Each of the models used the column “IS_SUCCESSFUL” as the target.
    •	For the models, the features of each module are all columns from the dataset, except for the following columns:
     1.	“EIN”
     2.	“NAME”
     3.	“IS_SUCCESSFUL”
    •	“EIN” and “NAME” were dropped from the features because these columns are identifiers and do not impact the success of an application.  The “IS_SUCCESSFUL” was not included in features since this column is the target and as such should not be a feature. 
b.	Compiling, Training, and Evaluating the Model
    •	Each of the models are different to attempt to achieve the goal accuracy for the model of 75%. The models used different numbers of neurons, activation functions, epochs, and even different numbers of layers. The different activation functions help fit models to different shapes of data and since I do not know the shape of the data, different activation functions where to used to see which one fit the model the best.  Since it is possible to overfit a model, resulting in decreased accuracy, different numbers of neurons, layers, and epochs were used to find how many are necessary to fit the model while not over fitting. 
        1.	Model 1 (coded as nn) used 2 layers, 50 neurons in the first layer, 10 neurons in the second layer, "tanh" as the activation function for first layer, "relu" as the activation function for the second layer, “sigmoid” for the output layer, and 100 epochs. 
        2.	Model 2 (coded as nn2) used 2 layers, 25 neurons in the first layer, 2 neurons in the second layer, " relu" as the activation function for first layer, "relu" as the activation function for the second layer, “sigmoid” for the output layer, and 100 epochs. 
        3.	Model 3 (coded as nn3) used 2 layers, 15 neurons in the first layer, 3 neurons in the second layer, " relu" as the activation function for first layer, "relu" as the activation function for the second layer, “sigmoid” for the output layer, and 200 epochs. 
        4.	Model 4 (coded as nn_jp) used 3 layers, 25 neurons in the first layer, 10 neurons in the second layer,  2 neurons in the third layer “relu" as the activation function for first layer, "relu" as the activation function for the second layer, "relu" as the activation function for the third layer, “sigmoid” for the output layer, and 100 epochs. 
    •	I was not able to achieve the target model performance of 75% in the multiple model attempts that were made. 
    •	In my attempts to increase model performance I changed multiple variables including number of neurons per layer, number of layers, the activation function, and the number of epochs. 
c.	Summary:
    •	Each of the four models presented failed to achieve the target performance of 75%. The outcomes for each of the models are listed below:
    •	Model 1 (nn)
![image](https://github.com/kbrantner/deep_learning_challenge/assets/117327499/a897c6e3-df83-4722-850a-5a194da15429)

 
    •	Model 2 (nn2)
![image](https://github.com/kbrantner/deep_learning_challenge/assets/117327499/84a2a5ae-4caf-4534-a502-b843efcd7d8d)

 
    •	Model 3 (nn3)
![image](https://github.com/kbrantner/deep_learning_challenge/assets/117327499/9c24ab48-de42-434f-9ab0-2a7d8844ef5f)

 
    •	Model 4 (nn_jp)
![image](https://github.com/kbrantner/deep_learning_challenge/assets/117327499/b2a966c4-ea33-496a-adeb-24132297a2ca)

 
    •	Another model that could be used is the Random Forest model. This model could be appropriate since the data outcomes are known, it can perform both classification and regression tasks, and is appropriate to use with large data sets. However, when I used the Random Forest model the accuracy of the model was at its lowest, so the random forest code is committed out since it does not actually help improve accuracy. At this point I recommend continuing with the deep learning model. 
 
##Installation
For this project you will need to install the following dependencies when working in either google colab or in jupyter notebook:
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
import pandas as pd
import tensorflow as tf
import pandas as pd 
application_df = pd.read_csv("https://static.bc-edx.com/data/dl-1-2/m21/lms/starter/charity_data.csv")
Authors and acknowledgment
This project was completed by Kelsey Brantner. Bethany Lindberg helped me understand how export the module to an HDF5 file. She also helped me consider looking at the data using a Random Forest model as a comparison to see that the deep learning model is a better fit for this data.  

##Reference
IRS. Tax Exempt Organization Search Bulk Data Downloads. https://www.irs.gov/

##Project status
While this project is considered complete for the moment since multiple models were run, the project still has room for improvement and changes since the model never reached the desired accuracy. 


