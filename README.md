# FinalGEOG464 Analyzing and Mapping Census Data

Before You Begin:
<br>Before beginning to use the functions certain extensions need to be installed and imported.
The first block of code has all the installation that is required for the functions. It includes an extension for those who are using Google Colab. 
The second block of code has all the imports and their required names for the proceeding functions. 

Once that is complete, you will have a function that allows you to import any csv data that is needed. After this the 10 functions are next. 
These functions include a reading function for geodata frames that asks for a type of output so you can check the data as it is imported. A function to see all the information about your dataset with a choice of which information to see or be calculated. A function with a for loop allows you to display all the geodata frames at once, a few analyzing functions, a graphing function, and a final mapping function. 

Function 1: 
<br> Imports geodata frames from a json or geojson file with a choice of displaying the information as a plot or dataframe. The function requires two arguments, path which is where the data is coming from and dataview=0 which allows you to select the display of data after it has been imported and converted to a dataframe. 

Function 2: 
<br> To see all or chosen information about the dataframe selected. There are 4 selections, 1, returns all information such as column names, projection information, calculations based on column values. 2, returns the mean, maximum, minimum, mean absolute deviation, and the standard deviation. 3, returns number of columns, column labels, each column's datatype, amount of memory the dataframe takes, range index, and the number of cells that have non-null values for each column. 4, returns a select portion of the dataframe, the range must be selected for this function, range should look like example: [dataframe['column'] == value]. put 0 if there is no range required.

Function 3:
<br>Plot geodata frames from a list on one figure. First a list must be created. To create a list declare a variable as follows: new_list =[a,b,c,...]. Pass the list as the argument to the function. The function will iterate through the list and return a mapped plot of all the layers in the list. Choose a path to save the image for the variable path. Works best with vector data for large scale maps.

Function 4: 
<br> Clean Up Dataframes. There is a choice of different techniques to clean up the data. Rename will rename the column titles with the input that you give through a dictionary, variable is columnsDict. Convert will convert a column to a different datatype, i.e. convert from float to integer user is prompted with a choice to convert a column after inspecting the column. Fillna will fill in a value given to it by x for the chosen column, column and values have to be given by a list, list should have column names as: 'Column' in the list. Drop will drop a row based on the index number given to it by x

Function 5: 
<br> Analyze Data. In this function we will take census data with numerical values. Data can be analyzed in different manners such as change, will calculate the change from one year to another based on column values; aggregate, will aggregate the data based on the column, Column, and aggregate function, method, methods to choose are sum, first, last, min, max, mean, median; aggregate2, will aggregate the data based on a column, i.e. it can aggregate small dissemenation areas into larger census areas.

Function 6: 
<br> Calculations. This function will calculate three different arithmetic based scenarios. Percent will calculate the percentage of the dividend between two columns given to it by the arguments Column1 and Column2; average, will calculate the average of the column and create a new column with the average on each row; subtract will find the difference between the two column values based on their index. Each if will return the dataframe with the new column.

Function 7: 
<br>  Reclassification of dataframes based on column values. This is a two part function. The first part, Reclassification, reclassifies the rows based on a desired value. For this you will enter the name of the dataframe for the variable dataframe, enter the column to be analyzed for the variable column, enter the desired value for the variable desiredValue, this can appear as ex. 'none', or 1, enter the name for the column you wish to create in order to not forgot what the desirability value is for. Reclassification function will give either a 1 or 0 value based on the value found in the row of the column. It will return a dataframe with a new column function will have to be rerun for all columns desired to be reclassified.
For the second function sumReclassification this will sum the total columns that have a desirability value into a new column. This new column can be used to map the dataframe based on desirability. Rows that have a higher number will have a higher desirability. A list of columns to be summed must be given to this function as the variable ColumnList. This function also requires a dataframe input. It will return the dataframe with the new column of desirabilitysum. 

Function 8: 
<br> Check and Change CRS. The variable List should have the list of geodata frames to check and make sure that they are all the same. The user will be prompted to select if want to reproject or not, input shoud be either 'yes' or 'no'. If 'yes' is selected, then will be prompted to select the projection frame that is desired. Input of this should be 'EPSG:2950' as an example where 2950 is the projection value desired. Dataframes that need to be checked or reprojected must be given in a list through the variable List

Function 9: 
<br> Create a Scaled Map. Input the final dataframe that you wish to map with the column to be mapped. Arguments are dataframe which is the dataframe you wish to you, Column name as 'Column', max is the maximum limit of scale bar, min is the minimum limit of the scale bar, max and min need to be integer values, and path is the location for the function to save the image of the map that you will create. Included in the map are the axes limits on the figure, and a north arrow that is in a fixed location in the top left corner. 
















