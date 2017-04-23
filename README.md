## Make effective data visualization

To see the project: https://bl.ocks.org/dmavridis/d3_titanic

### Summary
The purpose of this project is to investigate the Titanic dataset, which contains demographics and passenger information from a subset of the 2224 passengers and crew on board the Titanic. Through visual representation of data, it will be shown that some particular categories of passengers stood more chance of surviving, especially females of first and second class and between ages 15-40.

### Design 
For the implementation of the project, I used dimple.js for the visualization part of the problem. Dimple is a bit more compact than d3 but still provides the entirety of its advantages for the particular task. I also tried to use the original dataset, without any processing directly with dimple, but I came across many problems which in my level I could not overcome. Therefore, I decided to use Excel and some post processing to extract the desired information. Excel is perfect for a small dataset but of course for larger ones, Python, Matlab or R are inevitable choices. 


Before creating the story, I made some quick plots and summaries in Excel, which is faster to get a feeling of the data. Then some design choices needed to be made, such as what kind of plot to use, the selection of the most important variables and what kind of representation (absolute or percent) the survived passengers would be. 
Since the independent variables are of categorical type, there was the option to use bar plot or a scatter plot one. I chose after my review comment to use a combination according to the particular graph. I also considered bubble charts but since the radius of the bubble is proportional to the data value, the area will have square dependence of the data and could lead to confusion regarding the data values.  I believe that count values are represented well side by side according to the Sex filter showing the difference of the values. Also for the percentages plots, the combination of scatter with line clearly delivers the message of survival probability. Also despite the variables being categorical, they are represented as linear range.  

The initial approach is implemented in `index_first.html`. It is a good starting point but needed much of work to reach its final form. Also it does not include any buttons or text, only the basic graph. 
Then, after requesting feedback from 3 colleagues, the final form was gradually reached. 
Throughout the work, I came to realize the following:

* For a relatively complicated set of data with several variables, it is challenging to fit everything in one graph. Even if this is achieved, the result will look complicated requiring increased effort from the reader to understand. Therefore it is efficient to use multiple graphs and let the reader explore. 
* As the graph creator, I got quite familiar with the data but when designing it is of greatest importance to think through the perspective of the reader, who can be someone totally ignorant of the data. Therefore, explanations and key information should be provided.
* The graph can be more easily understood through the use of colours and particularly some social norms for colours, such as blue for males and pink for females. 

The final design has the form that I wanted to demonstrate from the beginning. I have included explanations so that a reader can get the necessary background fast and then focus on the graph itself. Moreover, key conclusions have been also included. 

### Feedback
When I created a initial version of the graph, I asked in person two colleagues who are software engineers and another being a teacher which is more neutral, to provide some feedback on what they are understanding from the graph. 

The key points of their responses are as follows:

**Colleague 1, Software Engineer**

* Colours needed to be more representative for males (blue) and females(pink). The default colours were following a different order

	*Action:* Changed the order of default colours

* Need to provide more information of what is shown, using caption and simple text

	*Action:* Added some key information in the graphs

* In the age group data, it is better to avoid entries where there is not age information. 

	*Action:* Tried to apply that but searching extensively the web could not find a solid way to make it work. It is still in the graph but I believe it is not a negative point. 

**Colleague 2, Software Engineer**

* Make the initial slide a summary one using bar or line chart.
	
	*Action:* That was a good idea and an extra introductory slide was implemented showing general information. 

**Colleague 3, Teacher**

* Provided some feedback on the text structure, on the titles and labels. 
	
	*Action*: Added the age group information on the x-axis for the age.




### Resources

* dimplejs.org : Examples of using dimple.js

* https://www.kaggle.com/c/titanic: Titanic data

* Technical posts that helped overcome some issues: 
	* https://github.com/PMSI-AlignAlytics/dimple/wiki/dimple.axis#categoryFields
	* http://dimplejs.org/advanced_examples_viewer.html?id=advanced_interactive_legends

