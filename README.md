# Project-3-SQLite-Visualization

In this project, we decided to analyze the movie/TV show streaming platform of Netflix, a multi-billion dollar company that offers its users
access to some of the top rated shows and movies in the nation. Using a dataset of Netflix's top 246 rated shows, we did an in-depth analysis
to see what exactly holds the key to Netflix's continued and prolonged success as the world's go-to streaming platform. 
There were no ethical data restrictions as this Netflix dataset is publicly available information with no API requirements.

Please interact with the script's in this order:

"Jade_Interactive.ipynb", 
"show_demo_info_script.ipynb", 
"Top 10 Shows by Country.ipynb", 
"Top 20 Shows by Genre.ipynb"

*You may ignore the file: Michael_interactive_script.ipynb*

Summary of each Script's Purpose/Function and References:

"Jade_Interactive.ipynb" : My main objective was creating an interactive bar chart that a user can customize to their liking. I chose not to make every variable available to the user for readability purposes. For example, if I allowed a user to choose Title, which represents the title of the Netflix series, there would be over 200 unique values on the bar chart making it hard to read. Micheal will demonstrate how a user can look up and view the stats of their favorite shows. For the sake of my interactivity however, I needed to be able to convey as much information as possible without affecting the ability to read and interpret the data. Because we were using the Seaborn library, I researched possible ways to use Seaborn to create interactive data within Jupyter Notebook. I found a blog titled “Interactive Visualizations with Pandas, Seaborn, and IpyWidgets” that inspired my dynamic charts. This is where I learned how to use the dropdown function from widgets. I then experimented with a pie chart and learned a lot about widgets and implementing Seaborn into visualizations.

References for "Jade_Interactive.ipynb" : https://plainenglish.io/blog/interactive-visualizations-with-pandas-seaborn-and-ipywidgets-173e5d7d6a5e 

"show_demo_info_script.ipynb" : The Purpose of this script is to depict, analyze, and compare the averaged total vote count for each genre of Netflix's top 246 shows.
Within this script, you will see a non-interactive bar-graph that shows each genre and it's respective averaged vote count total and then below it you should be able 
to see the top 10 ranked shows within the dataset. Below that cell, there exists an interactive cell that, when inputted with a Netflix title, will output the respective
title's information and the aggregated total vote count that respective show recieved; then the user can compare that to the bar-graph above. 

References for "show_demo_info_script.ipynb" : I used ChatGPT Version 3.5 to help me generate an initial and bare-bones ipywidget function with the necessary interactions. I did this by asking ChatGPT to create a widget that will take in an inputted movie title 
and return information about that chosen title. I also used ChatGPT to get an understanding of the syntax regarding Seaborn, ie. how to create barplots
with the Seaborn library and incorporate that into my widget. Link to website: *https://chat.openai.com/*

"Top 10 Shows By Country.ipynb" : In order to analyze the data in a practical and efficient manner, I chose to provide the top 10 shows by country as my first visualization. There were a total of 18 countries in the dataset (top 246 Netflix shows) so this should provide a good mix of shows per country. I began by creating a dictionary that contained all the countries. I then stored the actual names of the countries instead of the ISO 3166 codes that were provided on the dataset. This will make it much easier for the user to be able to input specific countries.
  I then created a plot function to display the information via visualization in the form of a bar plot. This was rather straightforward, but I also included a print statement for errors ("Unfortunately, that country isn't available! Please try again...").
  The next part proved to be the most difficult, as I had to use widgets in order to provide the text box. This was because our group decided to use Seaborn as our additional library and widgets are needed for some interactive visualizations within Seaborn. For the text widget, I simply provided the input, output, and then the widget instructions. This is all labeled with my comments.

"Top 20 Shows by Genre.ipynb" : The next interactive visualization I chose to display was the top 20 shows per genre. I thought this would be one of the most practical and useful things to use since people generally know their favorite genres. I also extended the list from 10 (which I used for Countries) to 20 because I wanted to mix the code up for the project. Within this code, I first created the function to visualize the data. I opted for another bar plot, as it certainly represents this data best. In that plot, I will show the top 20 shows per genre and create a nice spread of numbers on the x and y axis to ensure an easy-to-read graph.
  I then created the button function, ensured that the output is cleared every time, then called the “topshows” function. Then I created a list of button objects, and finally made sure to display the buttons vertically so it would look clean and clear. Finally, we output the widget to complete the code.


References for "Top 10 Shows by Country.ipynb" and "Top 20 Shows by Genre.ipynb" :
•	Class Codes
•	Personal Codes (converting CSV to SQLite)
•	General Seaborn Info: https://seaborn.pydata.org/generated/seaborn.barplot.html
•	Barplot format and labels: https://stackoverflow.com/questions/44861539/barplot-label-individual-bars-with-their-height-matplotlib-python
•	Annotate barplots: https://stackoverflow.com/questions/57203871/put-significance-asterisks-in-the-horizontal-middle-of-each-bar-in-a-barplot
•	Annotate barplots: https://www.geeksforgeeks.org/how-to-annotate-bars-in-barplot-with-matplotlib-in-python/
•	Seaborn interactivity: https://www.tutorialspoint.com/how-can-we-use-seaborn-for-interactive-visualization
•	General seaborn visualization info: https://medium.com/geekculture/python-seaborn-statistical-data-visualization-in-plot-graph-f149f7a27c6e
•	Widgets: https://ipywidgets.readthedocs.io/en/stable/examples/Widget%20Events.html
•	Widgets: https://ipywidgets.readthedocs.io/en/latest/examples/Widget%20List.html
•	Python coding examples: https://www.analyticsvidhya.com/blog/2021/10/interactive-plots-in-python-with-plotly-a-complete-guide/
•	Widgets: https://anywidget.dev/en/jupyter-widgets-the-good-parts/

Data-Set Reference/Link for download : *https://www.kaggle.com/datasets/thedevastator/netflix-top-rated-movies-and-tv-shows-2020-2022?select=Best+Shows+Netflix.csv*  
(specifically "Best Shows Netflix.csv")
