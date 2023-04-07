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
  
  
  As seen from the plot, the failure rate and mean time to failure (MTTF) for the original failure data and the predictions at the last interval (17) are:
  | Dataset        | Failure Rate (F/Interval) | MTTF (intervals) |
|----------------|---------------------------|------------------|
| Raw Data       | 17/54 = 0.315             | 1/0.315 = 3.174  |
| DW3 Prediction | 17/54 = 0.315             | 1/0.315 = 3.174  |
| GM Prediction  | 17/54 = 0.315             | 1/0.315 = 3.174  |

 From the table we can see that with the models the failure rate is 0.315. so for a business if the acceptable range of failure is is above this value it means  it is acceptable else it is not.
  

  

# Assessment Using Reliability Demonstration Chart 
  The following table details the parameters used in the RDC-11 Excel sheet used to graph and assess Failure Report 8.
| Parameter      | Parameter Value |
|----------------|-----------------|
| Discrimination Ratio (γ) | 2.000|          
| Developer's Risk (α) | 0.100|            
| User's Risk (β) | 0.100|           

  Below is a table of Cumulative Failure Count, Cumulative Execution Time, Time Between Failures.
| Cumulative Failure Count | Cumulative Execution Time (hours) | Time Between Failures (hours) |
|--------------------------|-----------------------------------|-------------------------------|
| 1  | 2.0 | 2.0   |
| 2  | 5.0 | 3.0   |
| 3  | 10.0 | 5.0  |
| 4  | 11.0 | 1.0  | 
| 5  | 12.3 | 1.3  |
| 6  | 13.5 | 2.2  |
| 7  | 16.6 | 3.1  |
| 8  | 21.0 | 4.4  |
| 9  | 25.8 | 4.8  |
| 10  | 31.4 | 5.6 |
| 11  | 37.6 | 6.2 |
| 12  | 45.3 | 7.7 |
| 13  | 53.3 | 8.0 |
| 14  | 61.6 | 8.3 |
| 15  | 70.5 | 8.9 |
| 16  | 79.6 | 9.1 |
  
 RDC plots:
  
 1. The first plot consists of FIO = 16 failures/79.6 intervals = 0.201, taking the inverse to get a MTTF value of = 1/0.201 = 4.975.
  ![image](https://user-images.githubusercontent.com/104797814/230473183-fdd71270-38fd-48ae-91a4-3d4e929522d6.png)
  
  2. The second plot consists of FIO = 19 failures/79.6 intervals = 0.238, taking the inverse to get a MTTF value of 1/0.238 = 4.189.
  ![image](https://user-images.githubusercontent.com/104797814/230474252-3741a663-25e0-4a55-a62a-2579e692573c.png)

  3. The third plot consists of doubling the minimum MTTF, which will be equal to 4.189 * 2 = 8.378.
  ![image](https://user-images.githubusercontent.com/104797814/230474901-f0819cad-38b5-4f59-9e86-899bab210862.png)

  4. The fourth plot consists of halving the minimum MTTF, which will be equal to 4.189 / 2 = 2.0945.
  ![image](https://user-images.githubusercontent.com/104797814/230475275-0399726d-30d4-4d84-84e0-d88d2253a82a.png)
 
  The minimum MTTF value was determined by trying to find a failure count across the total number of intervals which we found to be 19 failures over 79.6 intervals. By taking the inverse of this value we determined the minimum MTTF to be 4.189. We changed the FIO value until this minimum was determined, it is where the SUT is in the `Continue Test` region, not yet entering the `Accept` region.
# 

# Advantages and disadvantages of RDC

Advantages of RDC:

1. RDC is convenient for participants, who can complete surveys or provide data from their own homes, saving time and effort.

2. RDC is often cheaper than in-person data collection because it eliminates the need for a physical location and equipment.

3. RDC can increase the sample size as it enables researchers to reach more people via online platforms.

Disadvantages of RDC:

1. Researchers have limited control over the environment in which participants provide data, which can affect the accuracy and quality of the data.

2. RDC is not accessible to all populations, particularly those without internet access or who are not comfortable using technology.

3. Technical problems, such as poor internet connectivity or equipment failure, can lead to incomplete or inaccurate data.
  

# Comparison of Results
  For the Reliability Growth Testing, a MTTF value of 3.174 was obtained. For the Reliability Demonstration Chart we obtained a minimum MTTF value of 4.189. Due to the similarity of these values across the same failure set, therefore we can consider them to be valid. 
  

# Discussion on Similarity and Differences of the Two Techniques
  - Reliability Growth Testing mainly focusses on trying to improve reliability of a product or system, on the otherhand, Reliability Demonstration Chart focusses on demonstrating a product's required reliability expectations. This makes RDC especially useful for conveying information to investors or stakeholders.
  - Reliability Growth Testing is done iteratively, whereas Reliability Demonstration Chart is performed through taking a small sample of product to test and verify its reliability.
  - Both similiar in that they both rely on statistical analysis to analyze a product, system or service's reliability
  - Both are used to improve and assess quality and reliability
  

# How the team work/effort was divided and managed
  Temmy and Vishal focussed mainly on Part 1. of the assignment, which involves Reliability Growth Testing.
  Brandon and Aaryan focussed mainly on Part 2. of the assignment, which involves using the Reliability Demonstration Chart Excel spreadsheet.

# 

# Difficulties encountered, challenges overcome, and lessons learned
  - One of the difficulties faced was the overall confusion regarding the dataset and which one's to use. it would have been better if a proper dataset has been given in the proper format(excel or txt) which could have saved a lot of time.
  - more details and instruction on how to operate on C-SFRAT could have been useful.
  - One of the difficulties encountered was when testing using RDC, the spreadsheet needed to be set to unprotected in order to use it

# Comments/feedback on the lab itself
  - Compared to other assignments more details instructions could have been given in this lab. The lab is small compared to other but the confusion regarding dataset and operating tools made this assignment a bit hard.
  - The assignment was an interesting experience to get to test reliability tools, both are extremely useful and emphasize different aspects of testing quality and reliability
