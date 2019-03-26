---
layout: post
title:      "Chapter 2 - Right, Wrong, & Better!"
date:       2019-03-25 10:52:15 -0400
permalink:  chapter_2_-_right_wrong_and_better
---

There is a right way, a wrong way, and an even better way when it comes to using pie charts. 

### Before diving into our pie charts’ “report card,” why do we use any types of charts in the first place?

* Charts allow us to take information from sets of data and make it more understandable, and importantly for data scientists, more presentable. 

* In general, having charts make it easier to compare your different sets of data and the more information you can convey in your charts without making them more complex, the better. When your boss can get their answers quickly without having to decipher through your work, that is always a good sign.

### Why pie charts? A "pros" reasoning.

* Pie charts are one of the most common charts that many people know how to read the basics of.

* These circular-shaped types of charts (including donut charts too) are typically used to tell a story about the parts-to-whole aspect of a set of data. As a one-dimensional display, if you like looking at relativity in pictures, you can straightforwardly see if a subset is more in quantity than another. 

### Why not pie charts? A "cons" list.

Again reiterated: as a one-dimensional display of relativity, pie charts plainly show you proportions. 

**Note: All of the following examples are all made up data sets.*

<ol><li value="1">
Having more than five, “lengthy-descripted” categories that are mutually exclusive (i.e., the data does not overlap) will make the information appear more crowded, and less reader-friendly; remember, we want to convey more information without making it more complex. If the subsets are not mutually exclusive, a workaround is to add another category, but that just calls for a positive-feedback to add more categories. 
</li></ol>

<center>
<b>► ► ► Example 1a. ◄ ◄ ◄<br>
What are the statuses of shipments in each territory?</b>

<br>
<table>
  <caption><b>Data Set of Shipment Statuses:</b></caption>
  <tr>
    <td></td>
    <th scope="col">North</th>
    <th scope="col">East</th>
    <th scope="col">South</th>
    <th scope="col">West</th>
  </tr>
  <tr>
    <th scope="row">Active & Open</th>
    <td>31</td>
    <td>44</td>
    <td>13</td>
    <td>12</td>
  </tr>
  <tr>
    <th scope="row">In Transit</th>
    <td>25</td>
    <td>32</td>
    <td>19</td>
    <td>14</td>
  </tr>
	 <tr>
    <th scope="row">Complelted</th>
    <td>35</td>
    <td>10</td>
    <td>22</td>
    <td>26</td>
  </tr>
</table>

![<blockquote class="imgur-embed-pub" lang="en" data-id="a/qzzP09Y"><a href="//imgur.com/qzzP09Y"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>](https://www.imgur.com/2BJ0dvm.png) 
</center>

<br><ol><li value="2">
Assuming they tell you the percentage for each part “slice” would be useful. But sometimes they do not and that can be a lot of guesswork into measuring the angle, especially if they are seemingly similar. Furthermore, after given actual/approximation of the angle percentage, more operative calculation may need to be done to get the specific dataset info in the set and/or subset. That extra work on your part can easily be avoided.
</li></ol>

<center>
<b>► ► ► Example 2a. ◄ ◄ ◄<br>
We own an exotic animal sanctuary that can occupy up to 300 animals<br>of eight different species. Given that we are at full capacity and if we<br>have to bulk buy food for 100 animals at a time based on their diet,<br>how many different combinations can we group together?</b>

<br>
<table>
  <caption><b>Data Set of Exotic Animals:</b></caption>
	<tr>
		<th>Animal</th>
		<th>Tally</th>
		<th>Diet</th>
	</tr>
	<tr>
		<td>Wolf</td>
		<td>44</td>
		<td>Carnivore</td>
	</tr>
	<tr>
		<td>Falcon</td>
		<td>35</td>
		<td>Carnivore</td>
	</tr>
	<tr>
		<td>Moose</td>
		<td>44</td>
		<td>Herbivore</td>
	</tr>
	<tr>
		<td>Elephant</td>
		<td>39</td>
		<td>Herbivore</td>
	</tr>
	<tr>
		<td>Red Fox</td>
		<td>48</td>
		<td>Carnivore</td>
	</tr>
	<tr>
		<td>Tiger</td>
		<td>21</td>
		<td>Carnivore</td>
	</tr>
	<tr>
		<td>Snapping Turtle</td>
		<td>27</td>
		<td>Herbivore</td>
	</tr>
	<tr>
		<td>Panda</td>
		<td>42</td>
		<td>Herbivore</td>
	</tr>
</table>

![<blockquote class="imgur-embed-pub" lang="en" data-id="a/qzzP09Y"><a href="//imgur.com/qzzP09Y"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>](https://www.imgur.com/DlAg4Uw.png)
</center>

<br><ol><li value="3">
In many real-world circumstances, data is presented as incomplete, more frequently so the larger the set. Well, if the parts do not sum up to the meaningful whole, a pie chart cannot represent the data, period. The total of a subsample and the comparison of each element value to the artificial whole are not meaningful in the least.
</li></ol>

<center>
<b>► ► ► Example 3a. ◄ ◄ ◄<br>
We just finished November’s sales data. Which quarter was our best<br>performing? How many orders were fulfilled this past year?</b>

<br>
<table>
  <caption><b>Data Set of Quarter Performances:</b></caption>
  <col>
  <col>
	<col>
  <thead>
    <tr>
      <th scope="col">Quarter</th>
      <th scope="col">Month</th>
			<th scope="col">Product's Market Value</th>
      <th colspan="2" scope="colgroup">Orders (M→Q cumulative)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="3" scope="rowgroup">Q1</th>
      <th scope="row">January</th>
      <td>30</td>
			<td>52</td>
			<td>52</td>
    </tr>
    <tr>
      <th scope="row">February</th>
			<td>33</td>
      <td>49</td>
      <td>101</td>			
    </tr>
    <tr>
      <th scope="row">March</th>
			<td>32</td>
      <td>51</td>
			<td>152</td>
    </tr>
  </tbody>
  <tbody>
    <tr>
      <th rowspan="3" scope="rowgroup">Q2</th>
      <th scope="row">April</th>
			<td>28</td>
      <td>68</td>
			<td>68</td>
    </tr>
    <tr>
      <th scope="row">May</th>
			<td>25</td>
      <td>78</td>
      <td>140</td>
			</tr>
    <tr>
      <th scope="row">June</th>
			<td>26</td>
      <td>71</td>
			<td>211</td>
    </tr>
  </tbody>
  <tbody>
    <tr>
      <th rowspan="3" scope="rowgroup">Q3</th>
      <th scope="row">July</th>
			<td>29</td>
      <td>63</td>
			<td>63</td>
    </tr>
    <tr>
      <th scope="row">August</th>
			<td>31</td>
      <td>51</td>
      <td>114</td>
			</tr>
    <tr>
      <th scope="row">September</th>
			<td>27</td>
      <td>72</td>
			<td>186</td>
    </tr>
  </tbody>
  <tbody>
    <tr>
      <th rowspan="3" scope="rowgroup">Q4</th>
      <th scope="row">October</th>
			<td>34</td>
      <td>47</td> 
			<td>47</td>
    </tr>
    <tr>
      <th scope="row">November</th>
			<td>28</td>
      <td>55</td>
      <td>102</td>
			</tr>
    <tr>
      <th scope="row">December</th>
			<td>21</td>
      <td></td>
      <td>102</td>
		</tr>
  </tbody>
</table>

![<blockquote class="imgur-embed-pub" lang="en" data-id="a/qzzP09Y"><a href="//imgur.com/qzzP09Y"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>](https://www.imgur.com/ACG1h2S.png)
</center>

<br><ol><li value="4">
Furthermore, people want to seem smarter and fancier, so they try to make a 3-dimensioinal pie chart version with differing shades/opacity/design fill. Aesthetically, there is no logical sense nor linear gradient scale to do these, and only adds to the distraction and enhances the complexity of its clutter. This happened in our 2nd example above when we did not take into account color blindness. Also to consider, if you have to print your chart(s), you will not always have access to a color printer and the grayscale may not be easily distinguishable.
</li></ol>

<center>
<b>► ► ► Example 4a. ◄ ◄ ◄<br>
What is the typical time spent walking your dog every day for 10 weeks?</b>

<br>
<table>
  <caption><b>Data Set of Dog Walks:</b></caption>
  <tr>
    <td></td>
    <th scope="col">Sunday</th>
    <th scope="col">Monday</th>
    <th scope="col">Tuesday</th>
    <th scope="col">Wednesday</th>
		<th scope="col">Thursday</th>
		<th scope="col">Friday</th>
		<th scope="col">Saturday</th>
  </tr>
  <tr>
    <th scope="row">Week 1</th>
    <td>22</td>
    <td>24</td>					
    <td>28</td>
    <td>24</td>
		<td>25</td>
		<td>26</td>
		<td>26</td>
  </tr>
  <tr>
    <th scope="row">Week 2</th>
    <td>24</td>
    <td>31</td>
    <td>26</td>
    <td>15</td>
		<td>0</td>
		<td>28</td>
		<td>22</td>
  </tr>
  <tr>
    <th scope="row">Week 3</th>
    <td>14</td>
    <td>22</td>
    <td>12</td>
    <td>16</td>
		<td>17</td>
		<td>19</td>
		<td>12</td>
  </tr>
  <tr>
    <th scope="row">Week 4</th>
    <td>25</td>
    <td>0</td>
    <td>14</td>
    <td>23</td>
		<td>14</td>
		<td>13</td>
		<td>15</td>
  </tr>
	  <tr>
    <th scope="row">Week 5</th>
    <td>12</td>
    <td>30</td>
    <td>15</td>
    <td>15</td>
		<td>17</td>
		<td>19</td>
		<td>30</td>
  </tr>
	  <tr>
    <th scope="row">Week 6</th>
    <td>14</td>
    <td>33</td>
    <td>22</td>
    <td>0</td>
		<td>13</td>
		<td>18</td>
		<td>26</td>
  </tr>
	  <tr>
    <th scope="row">Week 7</th>
    <td>29</td>
    <td>25</td>
    <td>26</td>
    <td>15</td>
		<td>18</td>
		<td>24</td>
		<td>18</td>
  </tr>
	  <tr>
    <th scope="row">Week 8</th>
    <td>25</td>
    <td>30</td>
    <td>13</td>
    <td>21</td>
		<td>15</td>
		<td>0</td>
		<td>16</td>
  </tr>
	  <tr>
    <th scope="row">Week 9</th>
    <td>15</td>
    <td>11</td>
    <td>22</td>
    <td>14</td>
		<td>22</td>
		<td>19</td>
		<td>25</td>
  </tr>
	  <tr>
    <th scope="row">Week 10</th>
    <td>11</td>
    <td>22</td>
    <td>10</td>
    <td>31</td>
		<td>29</td>
		<td>16</td>
		<td>16</td>
  </tr>
</table>

![<blockquote class="imgur-embed-pub" lang="en" data-id="a/qzzP09Y"><a href="//imgur.com/qzzP09Y"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>](https://www.imgur.com/ozJc643.png)
</center>

<br><b>Ultimately, pie charts are rarely a good fit for the problem they are intended to solve because they are poor at communicating the desired observations in the data. </b>

### So then, what is an even better way than the pie chart?

Arguably, there is almost always an alternative visualization choice that displays the data more clearly and effectively than a pie chart. So, I recommend to always opt for that alternative. The more efficient charts do not require data labeling nor multiple colors (unless there are different series); you should not need to have any extraneous numbers in your chart to make your point.

<ol><li value="1">
But if you are adamant in showing your figure in relations to a whole, and your category descriptions are on the lengthier side, try instead squaring the pie/a waffle chart/a tree map. A 10x10 cell square makes it possible to read values precisely to a (rounded) single percent. You can either separate the subsets or combine it into one large square. However, in some programs, it is possible that your chart will default into a rectangle shape, in which it again can make it obscure to compare all the categories, but at least it is more accurate than a pie chart.
</li></ol>

<center>
<b>► ► ► Example 1b. ◄ ◄ ◄<br>
What are the statuses of shipments in each territory?</b>

<br>
<table>
  <caption><b>Data Set of Shipment Statuses:</b></caption>
  <tr>
    <td></td>
    <th scope="col">North</th>
    <th scope="col">East</th>
    <th scope="col">South</th>
    <th scope="col">West</th>
  </tr>
  <tr>
    <th scope="row">Active & Open</th>
    <td>31</td>
    <td>44</td>
    <td>13</td>
    <td>12</td>
  </tr>
  <tr>
    <th scope="row">In Transit</th>
    <td>25</td>
    <td>32</td>
    <td>19</td>
    <td>14</td>
  </tr>
	 <tr>
    <th scope="row">Complelted</th>
    <td>35</td>
    <td>10</td>
    <td>22</td>
    <td>26</td>
  </tr>
</table>

![<blockquote class="imgur-embed-pub" lang="en" data-id="a/qzzP09Y"><a href="//imgur.com/qzzP09Y"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>](https://www.imgur.com/NbSLBNx.png)
</center>

<br><ol><li value="2">
Bar charts are cleaner than waffle charts because you can compare each category to every other category efficiently with raw values rather than percentages. The exact numbers give us the ability to be, in general, more credible for anyone to look at the report and have confidence that the source is reliable. If you have a sample population of 100 vs 100,000, which data set would you more likely want sourced?
</li></ol>

<center>
<b>► ► ► Example 2b. ◄ ◄ ◄<br>
We own an exotic animal sanctuary that can occupy up to 300 animals<br>of eight different species. Given that we are at full capacity and if we<br>have to bulk buy food for 100 animals at a time based on their diet,<br>how many different combinations can we group together?</b>

<br>
<table>
  <caption><b>Data Set of Exotic Animals:</b></caption>
	<tr>
		<th>Animal</th>
		<th>Tally</th>
		<th>Diet</th>
	</tr>
	<tr>
		<td>Wolf</td>
		<td>44</td>
		<td>Carnivore</td>
	</tr>
	<tr>
		<td>Falcon</td>
		<td>35</td>
		<td>Carnivore</td>
	</tr>
	<tr>
		<td>Moose</td>
		<td>44</td>
		<td>Herbivore</td>
	</tr>
	<tr>
		<td>Elephant</td>
		<td>39</td>
		<td>Herbivore</td>
	</tr>
	<tr>
		<td>Red Fox</td>
		<td>48</td>
		<td>Carnivore</td>
	</tr>
	<tr>
		<td>Tiger</td>
		<td>21</td>
		<td>Carnivore</td>
	</tr>
	<tr>
		<td>Snapping Turtle</td>
		<td>27</td>
		<td>Herbivore</td>
	</tr>
	<tr>
		<td>Panda</td>
		<td>42</td>
		<td>Herbivore</td>
	</tr>
</table>

![<blockquote class="imgur-embed-pub" lang="en" data-id="a/qzzP09Y"><a href="//imgur.com/qzzP09Y"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>](https://www.imgur.com/faf5MMH.png)
</center>
 
<br><ol><li value="3">
Line charts are great for visualizing change over time. Because the data is connected by a continuous “slope” line, we can see how a value develops. The relationship of time between each category should be consistently periodical and not random. Bonus points if you can ratio multiple y-axes to further analyze why these values may be trending the way they are.
</li></ol>

<center>
<b>► ► ► Example 3b. ◄ ◄ ◄<br>
We just finished November’s sales data. Which quarter was our best<br>performing? How many orders were fulfilled this past year?</b>

<br>
<table>
  <caption><b>Data Set of Quarter Performances:</b></caption>
  <col>
  <col>
	<col>
  <thead>
    <tr>
      <th scope="col">Quarter</th>
      <th scope="col">Month</th>
			<th scope="col">Product's Market Value</th>
      <th colspan="2" scope="colgroup">Orders (M→Q cumulative)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="3" scope="rowgroup">Q1</th>
      <th scope="row">January</th>
      <td>30</td>
			<td>52</td>
			<td>52</td>
    </tr>
    <tr>
      <th scope="row">February</th>
			<td>33</td>
      <td>49</td>
      <td>101</td>			
    </tr>
    <tr>
      <th scope="row">March</th>
			<td>32</td>
      <td>51</td>
			<td>152</td>
    </tr>
  </tbody>
  <tbody>
    <tr>
      <th rowspan="3" scope="rowgroup">Q2</th>
      <th scope="row">April</th>
			<td>28</td>
      <td>68</td>
			<td>68</td>
    </tr>
    <tr>
      <th scope="row">May</th>
			<td>25</td>
      <td>78</td>
      <td>140</td>
			</tr>
    <tr>
      <th scope="row">June</th>
			<td>26</td>
      <td>71</td>
			<td>211</td>
    </tr>
  </tbody>
  <tbody>
    <tr>
      <th rowspan="3" scope="rowgroup">Q3</th>
      <th scope="row">July</th>
			<td>29</td>
      <td>63</td>
			<td>63</td>
    </tr>
    <tr>
      <th scope="row">August</th>
			<td>31</td>
      <td>51</td>
      <td>114</td>
			</tr>
    <tr>
      <th scope="row">September</th>
			<td>27</td>
      <td>72</td>
			<td>186</td>
    </tr>
  </tbody>
  <tbody>
    <tr>
      <th rowspan="3" scope="rowgroup">Q4</th>
      <th scope="row">October</th>
			<td>34</td>
      <td>47</td> 
			<td>47</td>
    </tr>
    <tr>
      <th scope="row">November</th>
			<td>28</td>
      <td>55</td>
      <td>102</td>
			</tr>
    <tr>
      <th scope="row">December</th>
			<td>21</td>
      <td></td>
      <td>102</td>
		</tr>
  </tbody>
</table>

![<blockquote class="imgur-embed-pub" lang="en" data-id="a/qzzP09Y"><a href="//imgur.com/qzzP09Y"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>](https://www.imgur.com/oZp5fir.png)
</center>
 
<br><ol><li value="4">
Box (and whisker) plots go little further in showing us the descriptive statistics of the data by grouping the ordered numerical data through their quartiles. We can distinguish the degree of dispersion (i.e., the spread distribution). In addition to the points themselves, the range is made known (via the top/maximum and bottom/minimum horizontal line joined by the vertical “whiskers”), often excluding any outliers that can ultimately skew our data. The interquartile range is the middle 50% of our data (via the boxes to show the 1st (and 2nd) and 3rd quartiles). The 2nd quartile (i.e., the median) is useful for data sets where you want to get a sense of a "representative" measure of centrality since the mean would be skewed by outliers.
</li></ol>

<center>
<b>► ► ► Example 4b. ◄ ◄ ◄<br>
What is the typical time spent walking your dog every day for 10 weeks?</b>

<br>
<table>
  <caption><b>Data Set of Dog Walks:</b></caption>
  <tr>
    <td></td>
    <th scope="col">Sunday</th>
    <th scope="col">Monday</th>
    <th scope="col">Tuesday</th>
    <th scope="col">Wednesday</th>
		<th scope="col">Thursday</th>
		<th scope="col">Friday</th>
		<th scope="col">Saturday</th>
  </tr>
  <tr>
    <th scope="row">Week 1</th>
    <td>22</td>
    <td>24</td>					
    <td>28</td>
    <td>24</td>
		<td>25</td>
		<td>26</td>
		<td>26</td>
  </tr>
  <tr>
    <th scope="row">Week 2</th>
    <td>24</td>
    <td>31</td>
    <td>26</td>
    <td>15</td>
		<td>0</td>
		<td>28</td>
		<td>22</td>
  </tr>
  <tr>
    <th scope="row">Week 3</th>
    <td>14</td>
    <td>22</td>
    <td>12</td>
    <td>16</td>
		<td>17</td>
		<td>19</td>
		<td>12</td>
  </tr>
  <tr>
    <th scope="row">Week 4</th>
    <td>25</td>
    <td>0</td>
    <td>14</td>
    <td>23</td>
		<td>14</td>
		<td>13</td>
		<td>15</td>
  </tr>
	  <tr>
    <th scope="row">Week 5</th>
    <td>12</td>
    <td>30</td>
    <td>15</td>
    <td>15</td>
		<td>17</td>
		<td>19</td>
		<td>30</td>
  </tr>
	  <tr>
    <th scope="row">Week 6</th>
    <td>14</td>
    <td>33</td>
    <td>22</td>
    <td>0</td>
		<td>13</td>
		<td>18</td>
		<td>26</td>
  </tr>
	  <tr>
    <th scope="row">Week 7</th>
    <td>29</td>
    <td>25</td>
    <td>26</td>
    <td>15</td>
		<td>18</td>
		<td>24</td>
		<td>18</td>
  </tr>
	  <tr>
    <th scope="row">Week 8</th>
    <td>25</td>
    <td>30</td>
    <td>13</td>
    <td>21</td>
		<td>15</td>
		<td>0</td>
		<td>16</td>
  </tr>
	  <tr>
    <th scope="row">Week 9</th>
    <td>15</td>
    <td>11</td>
    <td>22</td>
    <td>14</td>
		<td>22</td>
		<td>19</td>
		<td>25</td>
  </tr>
	  <tr>
    <th scope="row">Week 10</th>
    <td>11</td>
    <td>22</td>
    <td>10</td>
    <td>31</td>
		<td>29</td>
		<td>16</td>
		<td>16</td>
  </tr>
</table>

![<blockquote class="imgur-embed-pub" lang="en" data-id="a/qzzP09Y"><a href="//imgur.com/qzzP09Y"></a></blockquote><script async src="//s.imgur.com/min/embed.js" charset="utf-8"></script>](https://www.imgur.com/b3vKyKu.png)
</center>
</ol>
