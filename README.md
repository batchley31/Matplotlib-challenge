  # Matplotlib-challenge

#Prepare the Data
  To prepare my data I created variable paths for the CSV and then read those paths as panadas. To merge them into a single DataFrame I created a new variabel and merged each path usign the common variabel "Mouse ID".  To find the number of mice I jsut looked within my new merged DataFrame and did a unique number search by the Mouse ID's which gave me the total amount of mice in the study.  Using groupby I looked for Mouse ID and Timepoint so I could see each mouse and how many times its was registered.  Just for an example I garabbed one Mouse ID and looked at all the Timepoints for that mouse by using .loc to locate only that Mouse ID.

#Generate Summary Statistics
  To calculate the mean, median, variance, standard deviation, and SEM I created a variable for each to repersent them, and then used my cleaned dataframe to look in the "Tumor Volume column and claculated the mean by grouping them all up within each drug regimen so when I put the function at the end it would calculate that function for all the Tumor Volumes of each drug that was used.  I then cretaed and statitstics table by listing out each variable and a corresponding name for it.  So when my columns in the DataFrame would populate it will also put all the calculations for each drug.  In the next cell below I did the same exact thign esstionally but used the aggregation funciton and listed out each variable I wanted to pull through. 

#Create Bar Charts and Pie Charts
To start I created the variable I wanted to chart but getting the value count of of all the tests performed in the "Drug Regimen" column.  On the next line I ploted all the drugs by bar to show all the individual counts for each drug and labeled my title and x and y axis accordingly.  Using a different method to create the bar chart I created two variables looking at jsut the drug names and the number of mice observed for each drug.  I then labeled the names of the drugs for my x axis and the count of how many times the mice were studied on the y axis, changed the color of the bars, and aligned them all to center with thier x variable.  Then created my x, y, and table lables to represent each axis and then rotated the x ticks to be verticle for less mashed up x varaibles 
#Calculate Quartiles, Find Outliers, and Create a Box Plot

#Create a Line Plot and a Scatter Plot

#Calculate Correlation and Regression
