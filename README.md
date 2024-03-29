# End to End Heart disease prediction

This notebook uses different ML and DS libraries to build ML model capable of predicting wheter someone has a heart disease or not.

**Approach:**
1. Problem definition
2. Data
3. Evaluation
4. Features
5. Modelling
6. Experimentation

## 1. Problem Definition
> Given clinical parameters about a patient, can we predict whether a patient has a heart disease or not.

## 2. Data

The original data came from the Cleavland data from UCI Machine Learning Repository: https://archive.ics.uci.edu/ml/datasets/heart+disease

There is also a version of it available on Kaggle: https://www.kaggle.com/datasets/volodymyrgavrysh/heart-disease

**Attribute Information:**

    1. Age: Age
    2. Sex: Sex (1 = male; 0 = female)
    3. ChestPain: Chest pain (typical, asymptotic, nonanginal, nontypical)
    4. RestBP: Resting blood pressure
    5. Chol: Serum cholestoral in mg/dl
    6. Fbs: Fasting blood sugar > 120 mg/dl (1 = true; 0 = false)
    7. RestECG: Resting electrocardiographic results
    8. MaxHR: Maximum heart rate achieved
    9. ExAng: Exercise induced angina (1 = yes; 0 = no)
    10. Oldpeak: ST depression induced by exercise relative to rest
    11. Slope: Slope of the peak exercise ST segment
    12. Ca: Number of major vessels colored by flourosopy (0 - 3)
    13. Thal: (3 = normal; 6 = fixed defect; 7 = reversable defect)
    14. target: AHD - Diagnosis of heart disease (1 = yes; 0 = no)

## 3. Evaluation

> If we can reach 95% accuracy at predicting wheter or not a patient has heart disease during the proof of concept, we'll pursue the project.

## 4. Features

Features are different parts of the data. During this step, you'll want to start finding out what you can about the data.

One of the most common ways to do this, is to create a **data dictionary**.

### Heart Disease Data Dictionary

A data dictionary describes the data you're dealing with. Not all datasets come with them so this is where you may have to do your research or ask a **subject matter expert** (someone who knows about the data) for more.

The following are the features we'll use to predict our target variable (heart disease or no heart disease).

1. age - age in years 
2. sex - (1 = male; 0 = female) 
3. cp - chest pain type 
    * 0: Typical angina: chest pain related decrease blood supply to the heart
    * 1: Atypical angina: chest pain not related to heart
    * 2: Non-anginal pain: typically esophageal spasms (non heart related)
    * 3: Asymptomatic: chest pain not showing signs of disease
4. trestbps - resting blood pressure (in mm Hg on admission to the hospital)
    * anything above 130-140 is typically cause for concern
5. chol - serum cholestoral in mg/dl 
    * serum = LDL + HDL + .2 * triglycerides
    * above 200 is cause for concern
6. fbs - (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false) 
    * '>126' mg/dL signals diabetes
7. restecg - resting electrocardiographic results
    * 0: Nothing to note
    * 1: ST-T Wave abnormality
        - can range from mild symptoms to severe problems
        - signals non-normal heart beat
    * 2: Possible or definite left ventricular hypertrophy
        - Enlarged heart's main pumping chamber
8. thalach - maximum heart rate achieved 
9. exang - exercise induced angina (1 = yes; 0 = no) 
10. oldpeak - ST depression induced by exercise relative to rest 
    * looks at stress of heart during excercise
    * unhealthy heart will stress more
11. slope - the slope of the peak exercise ST segment
    * 0: Upsloping: better heart rate with excercise (uncommon)
    * 1: Flatsloping: minimal change (typical healthy heart)
    * 2: Downslopins: signs of unhealthy heart
12. ca - number of major vessels (0-3) colored by flourosopy 
    * colored vessel means the doctor can see the blood passing through
    * the more blood movement the better (no clots)
13. thal - thalium stress result
    * 1,3: normal
    * 6: fixed defect: used to be defect but ok now
    * 7: reversable defect: no proper blood movement when excercising 
14. target - have disease or not (1=yes, 0=no) (= the predicted attribute)

**Note:** No personal identifiable information (PPI) can be found in the dataset.

It's a good idea to save these to a Python dictionary or in an external file, so we can look at them later without coming back here.


## Steps to run:
* Create a conda environment with scikit-learn, numpy, matplotlib, jupyter, pandas, seaborn
* Clone this repo
* Run the notebook


## License

This notebook is created by Abhishek Gautam and is licenced under MIT.
