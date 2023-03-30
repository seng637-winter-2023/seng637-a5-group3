****SENG 637 - Dependability and Reliability of Software Systems****

**Lab. Report \#5 – Software Reliability Assessment**

| Group:  3    |
|-----------------|
| Student 1 name:    Temiloluwa Bakare            |   
| Student 2 name:    Brandon Phan          |   
| Student 3 name:    Aaryan Sharma           |   
| Student 4 name:    Vishal Ravindran            | 

# Introduction
Assignment 5 deals with the analysis of integration test data using Reliability assesment tools with two methods
1. Reliability Growth Testing(RGT)
2. Reliability assessment using Reliability Demonstration Chart (RDC)

we will experimenting with both methods in the lab.

# 

# Assessment Using Reliability Growth Testing 
For the RGT testing we used C-SFRAT tool on the ds1 dataset and measured the results.C-SFRAT had user friendly interfaceand was easy to work with. using the ds1 spreadsheet the tool was run for the all the models and the spreadsheet was exported. link to spreadsheet<insert link>
  ![image](https://user-images.githubusercontent.com/104803633/228938741-2bb4a199-6035-4508-b677-6f4f28a567c1.png)

  

 while analysing the chart based on the AIC and BIC values the best models were Negative Binomial (NB2) with covariate F, Followed by NB2 with Covariate E,F , the third best model was Discrete weibull Order 2 (DW2) with covariate F. The best models was decided by the lowest of AIC and BIC values.
The best model had am AIC value of 63.60 and BIC of 66.100.
 ![image](https://user-images.githubusercontent.com/104803633/228938027-58a58c69-66c8-49ed-89da-06af4c288d27.png)
  
 Time-Interval plot
  ![image](https://user-images.githubusercontent.com/104803633/228941895-1ad21e27-e98c-43cd-b136-bf1ae156aa89.png)
For as we experiment with different time intervals DW2(F) gets better as failure is decreasing the above figure represents the 3 best models with nuimber of intervals as 20.
  
  Intensity plot
  ![image](https://user-images.githubusercontent.com/104803633/228958170-beee9cf0-2e67-4776-8120-cd26f199b125.png)

  
  

  

# Assessment Using Reliability Demonstration Chart 

# 

# Comparison of Results

# Discussion on Similarity and Differences of the Two Techniques

# How the team work/effort was divided and managed

# 

# Difficulties encountered, challenges overcome, and lessons learned

# Comments/feedback on the lab itself
