Air pressure system failure classification at Scania Trucks

Problem description-

Scania makes around 90,000 trucks per each year. Failure of the air pressure system in truck manufacture is one of the most common things. If we can classify which truck air pressure system can get failed based on multiple factors before a customer can buy it, Scania can save a lot of revenue by not selling bad products to customers.

Relevant Information:
   -- Introduction
     The dataset consists of data collected from heavy Scania trucks in everyday usage. The system in focus is the 
     Air Pressure system (APS) which generates pressurized air that is utilized in various functions in a truck, 
     such as braking and gear changes. The datasets' 
     the positive class consists of component failures for a specific component of the APS system. 
     The negative class consists of trucks with failures for components not related to the APS. The data consists of a subset of all available data, selected by experts. 

   -- Challenge metric  

     Cost-metric of miss-classification:

     Predicted class |      True class       |
                     |    pos    |    neg    |
     -----------------------------------------
      pos            |     -     |  Cost_1   |
     -----------------------------------------
      neg            |  Cost_2   |     -     |
     -----------------------------------------
     Cost_1 = 10 and cost_2 = 500

     The total cost of a prediction model the sum of "Cost_1" 
     multiplied by the number of Instances with type 1 failure 
     and "Cost_2" with the number of instances with type 2 failure, 
     resulting in a "Total_cost".

     In this case, Cost_1 refers to the cost that an unnecessary 
     checks need to be done by a mechanic at a workshop, while 
     Cost_2 refer to the cost of missing a faulty truck, 
     which may cause a breakdown.

     Total_cost = Cost_1*No_Instances + Cost_2*No_Instances.

5. Number of Instances: 
     The training set contains 60000 examples in total in which 
     59000 belong to the negative class and 1000 positive classes. 
     The test set contains 16000 examples. 

6. Number of Attributes: 171 

7. Attribute Information:
   The attribute names of the data have been anonymized for 
   proprietary reasons. It consists of both single numerical 
   counters and histograms consisting of bins with different 
   conditions. Typically the histograms have open-ended 
   conditions at each end. For example, if we measuring 
   the ambient temperature "T" then the histogram could 
   be defined with 4 bins where: 

   bin 1 collect values for temperature T < -20
   bin 2 collect values for temperature T >= -20 and T < 0     
   bin 3 collect values for temperature T >= 0 and T < 20  
   bin 4 collect values for temperature T > 20 

   |  b1  |  b2  |  b3  |  b4  |   
   ----------------------------- 
         -20     0      20

  The attributes are as follows: class, then anonymized operational data. The operational data have an identifier and a bin id, like "Identifier_Bin".
  In total there are 171 attributes, of which 7 are histogram variables. Missing values are denoted by "na".
  
  OUTPUT:
  
  The accuracy is 0.9943125, and the f1 score is 0.8671532846715329.
              precision-recall  f1-score   support

           0       1.00      1.00      1.00     15625
           1       0.96      0.79      0.87       375

    accuracy                           0.99     16000
   macro avg       0.98      0.90      0.93     16000
weighted avg       0.99      0.99      0.99     16000


confusion_matrix

[[15612    13]
 [   78   297]]
 
 Total cost=
 


