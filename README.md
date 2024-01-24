UTA Data Bootcamp Module 5
==========================

Riley Taylor  
2024-Jan-23

**Setup and Related Info**

The python notebook of choice is located in the Pymaceuticals directory in this repo. Please note that at one point I imported numpy to handle the check for outliers in the final tumor volume for various drugs. It could have easily been done without it, but I noticed that the series had a .to_numpy() method that was slightly more convenient to me than checking to see how to cast the data to a list some other way.

Let me know if you have any questions.


-----------------------------------------




# Report:

The bulk of the analysis we did applied to only a portion of the data set. However, the summary statistics we found showed us that the Capomulin drug regimen seemed to yield lower measures of central tendency regarding tumor volume in the mice it studied. It also had one of the lowest standard error/deviations of the study. It had more observed mice timepoints, and it was the natural choice for a more in depth explortation. Ramicane also had arguably better results in general, but they were so close their differences could possibly be explained by mice weight averages being different in their lab mice populations (when you notice the correlation between mice weight and tumor volume, it shows there is room to control the study more), for example. 

The line plot of one particular mouse showed how the tumor volumes receeded over the course of the administration of the drug. It should be noted that the drug did not seem to strictly decrease the tumor volume in the mouse l509 - there were some instances where tumor volume still increased. As with most data analysis, the answer always seems to lie behind even more analysis. Ultimately, these questions have so much complexity at their heart that it can be hard to isolate explicit causes without more rigorous controls, null hypothesis testing, etc. 

We noticed a pretty high correlation between weight and tumor volume as well. That makes sense, considering there are more cells in larger organisms. Cancer incidence in humans for example is higher in larger humans, although the parallel is not the same and there are several other factors behind that as well. But it's not surprising. 

One final note - the question to produce a scatter plot of mouse weight vs. the average observed tumor volume for the entire Capomulin regimen was needlessly vague, and I believe the starter code solution assumed (or perhaps knew, because I think this is constructed data) that the weight of the mice stayed the same across the study. While that produced a cleaner scatterplot, because you don't end up overlaying points on top of each other, it seems a very naive and frankly illogical approach. I would always expect weight fluctuation in virtually any series of tests over a 45 day period. I advocate that the question ought to be requesting that we graph the weight of the mice under the drug of choice at each timepoint vs the average tumor volume for those mice, as opposed to a single weight measurement for said mice vs the average tumor volume. 

Also, there are several other possible derived statistics to calculate. Percentage change in tumor size over dosage period, for example. Measurements like these could reflect better on the quality of the drug regimen. 


## 



------------------------

# Sources


### For Data Cleaning

pandas.DataFrame.merge — pandas 2.2.0 documentation
https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.merge.html

pandas.DataFrame.duplicated — pandas 2.2.0 documentation
https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.duplicated.html

How do I get a list of all the duplicate items using pandas in python? - Stack Overflow
https://stackoverflow.com/questions/14657241/how-do-i-get-a-list-of-all-the-duplicate-items-using-pandas-in-python


python - Is there a short contains function for lists? - Stack Overflow
https://stackoverflow.com/questions/12934190/is-there-a-short-contains-function-for-lists

python - How do I select rows from a DataFrame based on column values? - Stack Overflow
https://stackoverflow.com/questions/17071871/how-do-i-select-rows-from-a-dataframe-based-on-column-values

python - Deleting DataFrame row in Pandas based on column value - Stack Overflow
https://stackoverflow.com/questions/18172851/deleting-dataframe-row-in-pandas-based-on-column-value

pandas.DataFrame.copy — pandas 2.2.0 documentation
https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.copy.html

python - How do I get the row count of a Pandas DataFrame? - Stack Overflow
https://stackoverflow.com/questions/15943769/how-do-i-get-the-row-count-of-a-pandas-dataframe



### For Summary Statistics

How to add table title in python preferably with pandas - Stack Overflow
https://stackoverflow.com/questions/57958432/how-to-add-table-title-in-python-preferably-with-pandas

pandas.Series.var — pandas 2.2.0 documentation
https://pandas.pydata.org/docs/reference/api/pandas.Series.var.html

pandas.Series.sem — pandas 2.2.0 documentation
https://pandas.pydata.org/docs/reference/api/pandas.Series.sem.html

standard error - Google Search
https://www.google.com/search?q=standard+error&rlz=1C1CHBF_enUS929US929&oq=standard+error&gs_lcrp=EgZjaHJvbWUqDggAEEUYJxg7GIAEGIoFMg4IABBFGCcYOxiABBiKBTIMCAEQABhDGIAEGIoFMgcIAhAAGIAEMgcIAxAAGIAEMgcIBBAAGIAEMgcIBRAAGIAEMgcIBhAAGIAEMgYIBxBFGDzSAQgxOTMxajBqN6gCALACAA&sourceid=chrome&ie=UTF-8

pandas.DataFrame.agg — pandas 2.2.0 documentation
https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.agg.html

How to Use Pandas Dataframe (agg) Method? - Scaler Topics
https://www.scaler.com/topics/pandas-agg/



### For Bar and Pie Charts


python - Get row-index values of Pandas DataFrame as list? - Stack Overflow
https://stackoverflow.com/questions/18358938/get-row-index-values-of-pandas-dataframe-as-list

Pandas groupby() and count() with Examples - Spark By {Examples}
https://sparkbyexamples.com/pandas/pandas-groupby-count-examples/#:~:text=Group%20the%20Rows%20by%20Column,floating%20type%20data%20as%20well.

python - Converting a Pandas GroupBy multiindex output from Series back to DataFrame - Stack Overflow
https://stackoverflow.com/questions/10373660/converting-a-pandas-groupby-multiindex-output-from-series-back-to-dataframe

python - Rotate axis tick labels - Stack Overflow
https://stackoverflow.com/questions/10998621/rotate-axis-tick-labels

Simple plot — Matplotlib 3.8.2 documentation
https://matplotlib.org/stable/gallery/pyplots/pyplot_simple.html#sphx-glr-gallery-pyplots-pyplot-simple-py

pandas.DataFrame.plot.bar — pandas 2.2.0 documentation
https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.bar.html

pandas.DataFrame.plot.pie — pandas 2.2.0 documentation
https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.plot.pie.html

python - How to customize pandas pie plot with labels and legend - Stack Overflow
https://stackoverflow.com/questions/68909283/how-to-customize-pandas-pie-plot-with-labels-and-legend

How to Create Pie Chart from Pandas DataFrame? - GeeksforGeeks
https://www.geeksforgeeks.org/how-to-create-pie-chart-from-pandas-dataframe/

Color Demo — Matplotlib 3.8.2 documentation
https://matplotlib.org/stable/gallery/color/color_demo.html



### For Remainder of Project:

python - Renaming column names in Pandas - Stack Overflow
https://stackoverflow.com/questions/11346283/renaming-column-names-in-pandas

python - How do I select rows from a DataFrame based on column values? - Stack Overflow
https://stackoverflow.com/questions/17071871/how-do-i-select-rows-from-a-dataframe-based-on-column-values

python - Selecting with complex criteria from pandas.DataFrame - Stack Overflow
https://stackoverflow.com/questions/15315452/selecting-with-complex-criteria-from-pandas-dataframe

pandas.Series.to_numpy — pandas 2.2.0 documentation
https://pandas.pydata.org/docs/reference/api/pandas.Series.to_numpy.html

matplotlib.pyplot.boxplot — Matplotlib 3.8.2 documentation
https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.boxplot.html

matplotlib.pyplot.plot — Matplotlib 3.8.2 documentation
https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.plot.html

Configuring the font family — Matplotlib 3.8.2 documentation
https://matplotlib.org/stable/gallery/text_labels_and_annotations/font_family_rc.html

Indexing and selecting data — pandas 2.2.0 documentation
https://pandas.pydata.org/docs/user_guide/indexing.html

