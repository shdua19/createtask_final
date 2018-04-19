import numpy as np
import matplotlib.pyplot as plt


# Global lists for the user-inputted data set values of x and y.
dataSetX = []
dataSetY = []

# Lets user choose graph type then creates figure.
def graphType():
    graph_type = raw_input("What kind of graph would you like to make? ")
    if "scatter" in graph_type:
        plt.figure()
        plt.scatter(dataSetX, dataSetY)
        labelValues()
    elif "line" in graph_type:
        plt.figure()
        plt.plot(dataSetX, dataSetY)
        labelValues()
    elif "bar" in graph_type:
        plt.figure()
        plt.bar(dataSetX, dataSetY)
        labelValues()

# Lets user title graph and create axis labels, then asks if user wants additional calculations. Produces graph in separate window.
def labelValues():
    x_label = raw_input("What do you want to label the X axis? ")
    y_label = raw_input("What do you want to label the Y axis? ")
    graph_label = raw_input("What is the title of your graph or chart? ")
    font_size = raw_input("What do you want the font size to be? ")
    plt.xlabel(x_label)
    plt.ylabel(y_label)
    plt.title(graph_label, fontsize=(font_size))
    calculate = raw_input("Calculate average, median and mode? ")
    if "yes" in calculate:
        calculateValues()
    else:
        print "You can save your graph by clicking the save icon on the far right of the tool bar."
        plt.show()
#Asks for users to input Y values into a list to set the global list
def yValues():
    while True:
        data_entry = raw_input("Enter a y value (press enter when complete): ")
        if data_entry == "":
            break
        else:
            dataSetY.append(data_entry)
            print(dataSetY)
    graphType()

#Asks for users to input X values into a list to set the global list
def xValues():
    while True:
        data_entry = raw_input("Enter an x value (press enter when complete): ")
        if data_entry == "":
            break
        else:
            dataSetX.append(data_entry)
            print(dataSetX)
    yValues()


#Calculates the average of the X values for the dataset
def calculateValues():
    average = (sum(dataSetX)) / (len(dataSetX))
    print "Average: " + str(average)
    plt.show()
    
#Calls xValues to start the loop    
def createGraph():
    xValues()

#This shows the comparisons between min and max values in the datasets
def comparison():
     mn_idy = min( (dataSetY[i],i) for i in xrange(len(dataSetY)))
     mn_idx = min( (dataSetX[i],i) for i in xrange(len(dataSetX)))
     mx_idy = max( (dataSetY[i],i) for i in xrange(len(dataSetY)))
     mx_idx = max( (dataSetX[i],i) for i in xrange(len(dataSetX)))
     if mn_idy > mn_idx: 
        print "Your dataset indicates the minimum Y value is larger than the minimum X value"
     elif mn_idy < mn_idx: 
        print "Your dataset indicates the minimum X value is larger than the minimum Y value"
     if mx_idy > mx_idx:
        print "Your dataset indicates the maximum Y value is larger than the maximum X value"
     elif mn_idy < mn_idx:
        print "Your dataset indicates the maximum X value is larger than the maximum Y value"
     
createGraph()
comparison()
