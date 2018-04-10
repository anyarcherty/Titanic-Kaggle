# Titanic-Kaggle

#### Purpose:

This project is a practical project to predict if a passenger survived from the sinking of the Titanic or not. 

#### 1.1 Data Extraction
    
   * The Titanic: Machine Learning from Disaster is from kaggle:
   
        https://www.kaggle.com/c/titanic/data
        
   * Dataset Features:
   
        Survival: Passenger Survival Status
        
         0 = No (the passenger is not survival) , 1 = Yes (the passenger is survival)
        
        Pclass: Passenger Socioeconomic Status
        
         1st = Upper Level, 2nd = Middle Level, 3rd = Lower Level
        
        Sex: Passenger Gender
        
         male, female
        
        Age: Passenger Age
        
         Age is fractional if less than 1. If the age is estimated, is it in the form of xx.5
         
        Sibsp: number of Sibling and Spouse
        
         Sibling = brother, sister, stepbrother, stepsister
        
         Spouse = husband, wife

        Parch: number of Parent and Children
        
         Parent = mother, father
        
         Child = daughter, son, stepdaughter, stepson
         
         Some children travelled only with a nanny, therefore parch=0 for them
        
        Ticket: Passenger Ticket Number
        
        Fare: Passenger Fare
        
        Cabin: Cabin Number
        
        Embarked: Port of Embarkation
        
         C = Cherbourg, Q = Queenstown, S = Southampton
        
        
#### 1.2 Data Preprocess

   * Imputate Missing Value:
        
        * Drop Cabin Feature, which contains more than 77% missing value in both train and test dataset
        
        * Imputate Test Fare Feature with train fare feature mean
        
        * Imputate Train Embarked Feature with train embarked feature mode
        
        * Imputate Age Feature by Feature Correlation
        
              Age Feature is most relevent with Fare feature 
            
              From the fare feature description, divided fare into 4 group:

              Group 1: fare: <=10
            
              Group 2: fare: 10-15
            
              Group 3: fare: 15-30
            
              Group 4: fare: >30
              
              Imputate the Age Feature by different Fare group
   
   * Transforming Feature
   
        * Modify Age feature:
            
            Label Encode
   
        * Modify Ticket feature:
   
            Tokenized the Ticket feature with numerical number
    
        * One Hot Encode Embark Feature
        
        * Obtain the Title via Name Feature
        
   * Add more Feature
        
        * Add FamilySize Feature
        
        * Add IsAlone Feature
  
#### 1.3 Model Selection

   * Xgboost
   
        * Validation Accurary is 0.85
        
        * Update Parameter
        
            Grid Search with Cross Validation
            
            After parameter update, Validation Accurary is 0.85 
    
   * Lgboost
   
        * Validation Accurary is 0.83
        
        * Update Parameter
        
            Grid Search with Cross Validation
            
            After parameter update, Validation Accurary is 0.8328
   
   * Random Forest
   
        * Validation Accurary is 0.83
        
        * Update Parameter
        
            Grid Search with Cross Validation
            
            After parameter update, Validation Accurary is 0.832
   
   * Support Vector Machine
        
        * Validation Accurary is 0.83
        
        * Update Parameter
        
            Grid Search with Cross Validation
            
            After parameter update, Validation Accurary is 0.832
        
   * Logistic Regression
   
        * Validation Accurary is 0.83
       
        * Update Parameter
        
            Grid Search with Cross Validation
            
            After parameter update, Validation Accurary is 0.832
   
   * KNN
        
        * Validation Accurary is 0.82
        
        * Update Parameter
        
            Grid Search with Cross Validation
            
            After parameter update, Validation Accurary is 0.804
   
   
#### 1.4 Stacking / Ensemble methods
   
   * Use Xgboost, Lgboost, Random Forest and KNN to build ensemble model.
   
   * Predict the testset result
   
#### 1.5 Output Result

   * The predict accuracy is 0.781, top 15% in the leadboard
