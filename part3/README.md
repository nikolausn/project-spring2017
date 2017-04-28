# All Purpose Visualization Library
## Group Totoro

# All Purpose Library

For this task, we build a class library AllPurpose that can be found in AllPurpose.py that can be imported into your visualization. The class needs a Panda Dataframe object as an initialization parameter according to the column naming rules that has given below:
- Name: names
- Date: dates
- Latitude: latitude
- Longitude: longitude
- 1 Categorical label: categorical
- 3 Quantitive columns: quant1, quant2, quant3

The class instantiation can be called using

AllPurpose(data,column_name={},datestr = '%d/%m/%y')
- data: a panda dataframe
- column_name: the column name can be changed as long as you provide correct key for the columns. The default column names are follow
                  {'names': 'names',
                   'dates':'dates',
                   'latitude':'latitude',
                   'longitude':'longitude',
                   'categorical': 'categorical',
                   'quant1': 'quant1',
                   'quant2': 'quant2',
                   'quant3': 'quant3'                  
                  }
- datestr: how you want to display your date string. Some date, by default it will display day/month/year format.

We build three functions that will generate three visualizations described below

----------------------------------------------------------------------------------------------
## AllPurpose.plotGeneralStat()

We firstly visualized the general statistics for the dataset, focusing on the categorical data and three quantitative data. The visualization contains four graphs. Because the graphs are interrelated with each other, we combined them into one static visualization. 

When people are looking at the dataset, they might want to know how many categories are there and how many data falls in each category. So we used a bar chart to show the category frequencies. We can get a general idea about how the categories are distributed from this chart. To improve this graph, we can add the exact number of the frequencies to it.

We then plotted three graphs for the three quant data visualizing how are they distributed among the categories. We chose histogram as our visualization tool in these graphs because we could compare the percentages of quantities in each category intuitively. Since some of the data for quant2 are negative numbers, the quantity sum percentages of the data in this column also appear negative numbers. This may lead to some confusion, so it will be better if we convert all the percentages into positive numbers.

Aesthetic:
- For the Category Frequency Plot, we choose to plot it using Pie chart because this frequency is depicting the percentage of such category over all the data in the dataset.
- For the sum/total quantity for each category, we choose bar plot because it will represent the average value that lies in the particular category. In addition, because the quantity can contain minus value, we can't use the pie chart for this
- For the color, we choose Pastel because its linear color can separate the category the most and it also nice to be seen.

----------------------------------------------------------------------------------------------
## AllPurpose.plotDetailStat()

Our second visualization is an interactive plot, which shows the statistical details of the quantity data, is interactive. We binned the data in order to visualize the trends and changes of the statistics through different times. Users can choose the categories, quantity columns, statistics, and even binning numbers and colors as they want. It makes analyzing and comparing the statistics clear and easy. We haven't found any significant weakness of this visualization, but we are open to suggestions. 

Aesthetic:
- For this detail stat, we decide to build a toolbox that can work for any kind of data as long as the data follow a particular format. This toolbox will produce a visualization of quantity columns and their statistics over time using binning operation.
- We make this toolbox as customizable as possible to support users to get insight about the data. 
- The user can choose which categories they want to visualize by selecting categories in the multi-select box. 
- Quantity columns that one to be displayed can be chosen using the drop down box. 
-  The user also can choose which statistics (mean, min, max,1-SD, or sum) values that they want to display. We choose a straight line (-),  to represent the mean, dashed line (--) to represent 1-SD over the mean, dash-dot line (-.) to represent Min and Max values.
- A number of bins that want to be produced can be chosen using slider box, the default value is 12 bins
- Besides that, the user also can choose the Names that they want to display based on the values in the Names column. By default, All Names will be displayed in this statistics.
- Finally, the user can also choose any supported color that they want to see. By default, the color is Viridis. This will give the user a freedom to choose their own color

----------------------------------------------------------------------------------------------
## AllPurpose.plotSpatialStat()

The last function is also an interactive plot to visualize spatial data. The visualization is plotted on a static google map because it would be too abstract without one. We also made it interactive by adding drop down widgets, so that people can choose to look at specific categories or quantities with different binning scales. A circle represents the binned quantity mean in one spatial area and there are five intervals for the size of circles. People could get intuitive impressions on the spatial distributions of the quantitative data from this visualization. However, since the map is static, we can not see the detailed distribution from a narrower view. We could make the map dynamic so that people can zoom in and out to be able to focus on only one country or an even smaller area. 

Aesthetic:
- This toolbox will provide categories that have maximum average values over spatial space using spatial binning. 
- Firstly, the users can choose which categories they want to display in the visualization. User can choose more than one categories to provide comparison within categories in the spatial space
- Next, users also can choose which quantity column they want to compare
- How much the number of bin that user want to produce is also can be selected using binning slider box
- Finally, users can choose which color they want to represent in their visualization
- Within all the categories displayed in the spatial dimension, this visualization also will give the amount representation using the radius of the circle visualized. Therefore, a legend to provide circle scale is provided on the right top of the visualization.

----------------------------------------------------------------------------------------------
Nikolaus and Yiting worked and finished this part together. Nikolaus was in charge of coding and Yiting was responsible for writeup. We used Salem and Motionless libraries in this part. 