  # Matplotlib-challenge

#Prepare the Data
  
  To prepare my data I created variable paths for the CSV and then read those paths as panadas. To merge them into a single DataFrame I created a new variabel and merged each path usign the common variabel "Mouse ID".  To find the number of mice I jsut looked within my new merged DataFrame and did a unique number search by the Mouse ID's which gave me the total amount of mice in the study.  Using groupby I looked for Mouse ID and Timepoint so I could see each mouse and how many times its was registered.  Just for an example I garabbed one Mouse ID and looked at all the Timepoints for that mouse by using .loc to locate only that Mouse ID.

#Generate Summary Statistics
  
  To calculate the mean, median, variance, standard deviation, and SEM I created a variable for each to repersent them, and then used my cleaned dataframe to look in the "Tumor Volume column and claculated the mean by grouping them all up within each drug regimen so when I put the function at the end it would calculate that function for all the Tumor Volumes of each drug that was used.  I then cretaed and statitstics table by listing out each variable and a corresponding name for it.  So when my columns in the DataFrame would populate it will also put all the calculations for each drug.  In the next cell below I did the same exact thign esstionally but used the aggregation funciton and listed out each variable I wanted to pull through. 

#Create Bar Charts and Pie Charts
  
  To start I created the variable I wanted to chart but getting the value count of of all the tests performed in the "Drug Regimen" column.  On the next line I ploted all the drugs by bar to show all the individual counts for each drug and labeled my title and x and y axis accordingly.  Using a different method to create the bar chart I created two variables looking at jsut the drug names and the number of mice observed for each drug.  I then labeled the names of the drugs for my x axis and the count of how many times the mice were studied on the y axis, changed the color of the bars, and aligned them all to center with their x variable.  Then created my x, y, and table lables to represent each axis and then rotated the x ticks to be verticle for less mashed up x varaibles.  For the two pie charts I used the same format at the bar charts but used the pie function instead.  The only extra thing I added was the percetnage of male vs female inside the pie chart by using the autopct= at the end of the plot variable.

#Calculate Quartiles, Find Outliers, and Create a Box Plot

  To calculate I started by creating a DataFrame for each Drug Regimen but locating by the Drug Name in the Drug Regimen column of my mouse data DataFrame. I then created headers for each drug regimen seperately by doing a groupby function using the mouse ID and timepoint columns. I then used the total of each drug regimen and merged the total mouse ID's and timepoints of the full data frame with the timepoints of each drugs data frame.  From there to calculate the quartiles I used the merged dataframe for each drug regimen and looked through the total volume column.  I calculated the quartiles ny using the .quartile function and labeling it by the first quater the halfway point and the third quater of the tumor volumes to get the lower and upper for each drug. I then used my lower and upper quartiles to calculate if there could be any possible outliers and created seperate variables for those on each drug regimen.
  I used all of the calcualtions to create a boxplot graph so that I could see all the lower and upper bounds for each and their quartiles.  I also labeled any outlier dots as red so they would pop out and be easy to see.

#Create a Line Plot and a Scatter Plot

  To create the line plot I used the same concept as the box plot but used Timepoint as my x axis and Tumor Volume as my y axis so there is a measure of how big the tumor is over time as the mouse was introduced to the drug.
  for the scatter plot I did the same thing as the line but put my mouse weight on the x axis and tumor volume on the y axis so you could see if there was a correlation to how much to mosue weight for how big the tumor volume was.
  
#Calculate Correlation and Regression

  To start I imported scipy.stats as a lineregress so the code would be able to compute the equations I then labeled my line regression with all the values of slope, intercept, rvalue, pvalue, stderr.  To calculate each value I toko the mean of the weight and tumor volume searching by Mouse ID by using the .mean on the end of each groupby for the Capmulin data frame.  I then created the regression values by using the y=mx + b formula and used the slope for x and the intercept for b.  I then used a scatter plot so the line would go through a set of data to see how far away the points were from the line.  Lastly I used the plt.annotate to put the regression quatation on the graph for easy viewing.
