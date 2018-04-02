# Titanic-Kaggle

#### Purpose:

This project is to predict if a passenger survived the sinking of the Titanic or not. 

#### 1.1 Data Extraction
    
   * The Titanic: Machine Learning from Disaster is from kaggle:
   
        https://www.kaggle.com/c/titanic/data
        
   * Dataset Features:
   
        |   Feature          | Definition           |   Key                         |
        | ----------------   |-------------         |-------------                  | 
        |   survival         |  Survival            |0 = No, 1 = Yes                |
        |   pclass           |  Ticket class        |1 = 1st, 2 = 2nd, 3 = 3rd      |
        |   sex              |  Sex                 | female, male|
        |   age              |  Age                 |                               |
        |   sibsp            |  number of siblings / spouses aboard the Titanic| Sibling: brother, sister, stepbrother, stepsister  Spouse: husband, wife|
        |   parch            |  number of parents / children aboard the Titanic|    |
        |   ticket           |  Ticket number       |                               |
        |   fare             |  Passenger fare      |                               |
        |   cabin            |  Cabin number        |                               |
        |   embarked         |  Port of Embarkation | C = Cherbourg, Q = Queenstown, S = Southampton|
        
   * Variable Note
   
        pclass: A proxy for socio-economic status (SES)
        ```
        1st = Upper
        2nd = Middle
        3rd = Lower
        ```
        age: Age is fractional if less than 1. If the age is estimated, is it in the form of xx.5

        sibsp: The dataset defines family relations in this way...
        
        Sibling = brother, sister, stepbrother, stepsister
        
        Spouse = husband, wife (mistresses and fiancés were ignored)

        parch: The dataset defines family relations in this way...
        
        Parent = mother, father
        
        Child = daughter, son, stepdaughter, stepson
        
        Some children travelled only with a nanny, therefore parch=0 for them
        
   
