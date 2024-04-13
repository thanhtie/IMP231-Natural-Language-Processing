
teacher forcing: x feed to next recurrent is ground truth -> using in the training phase.

none teacher forcing: x feed to next recurrent is predicted value of lást recurrent -> using in the inferent phase.

What is the result for teacher forcing and none teacher forcing?

Must wait the previous recurrent complete to perform next recurrent. take longer time for training due to cannot parallel processing

disadvantages: 
+ Lack of information to predict due to 1 way encoding
