# matplotlib
matplotlib has two methods for graphing data


- One uses MATLAB's plotting syntax
    MATLAB's plotting syntax is concise and the most useful when 
    creating simple plots that require little coding. This method 
    is most effective when graphing data directly from a DataFrame

- object-oriented interface
    better suited to more complicated graphs that require more 
    coding, such as those with multiple lines or bars, or multiple 
    plots in one graph.

must be imported as `import matplotlib.pyplot`

## function to generate a simple x and y axis line plot

    import matplotlib.pyplot

    X_axis=list_1

    Y_axis=list_2

    matplotlib.pyplot.xlabel("Label for Axis X")

    matplotlib.pyplot.ylabel("Label for Axis Y")

    matplotlib.pyplot.plot(X_axis,Y_axis)

    matplotlib.pyplot.show()

