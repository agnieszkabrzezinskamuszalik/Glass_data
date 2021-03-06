# Glass_data - unbalanced group problem 
The most important part of any machine learning project is the proper preparation of data. In my project I focused on the problem of unbalanced data on a small packet of data with many classes.Some classes had very few observations, and the other part quite a lot.

Using literature (literature at the end of the jupyter notebook) I decided to write two methods looking for outliers based on IQR and Z-score and look first for outliers of the entire data set, and then outliers of individual classes.

Getting rid of cases that could disturb learning, I tried to equalize the number of groups, because the ratio of the most numerous to the least numerous was 70: 9 using the technique of reducing to the least numerous group would reduce the data packet to too little. At the same time, the high ratio did not allow artificial generation of such a large amount of data.

Three methods were written at the same time reducing the most numerous groups and increasing the least numerous groups to a certain number.
In the first case, data was generated by copying already existing observations.
In the second case, the attributes from the existing ones in the given group were drawn, thus creating new observations with similar properties.
In the third method, the mean and standard deviation for each attribute were determined and a floating-point number from the mean-std to mean+std range was drawn.
For comparison, three ready-made methods of data balancing were also used.

Random forest was used as the most suitable machine learning model for unbalanced data, and f1 was used for assessment.
