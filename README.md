# A Visualization of Student Debt
### Summary
After a lot of contemplation I finally decided on visualizing student debt. Using data I found on the website http://college-insight.org/, I created a map of the US states, with each state colored in a different shade of red to show average debt and a "bubble" to indicate the percentage of students in debt. The main point I am trying to convey with my visualization is that student debt has worsened over the years.

### Design
#### Revision 1( http://bl.ocks.org/spgitmonish/raw/a63036ef024e1b27c8d3/ )
When I decided on visualizing student data across the US, I wanted to convey my message on a map of the US. It was pretty easy to get the information I needed to display the US states(for more information look at the Resources section). Once I created the map, I had to go through my .csv file which had the debt data to understand which fields to use for visually conveying the information.

The two pieces of information I decided to convey were: _Average Debt in a State & Percentage of Students in Debt_.

I definitely had to think about what visual cues/encodings I wanted to use for my visualization. I was pretty conviced that a color encoding would be one of the most effective cues to use for conveying my message. I wasn't surely initially whether I wanted to use the color encoding for Average Student Debt or for Percentage of Students in Debt. After using color encoding for both, I decided that it would be best to use color coding for Average Student debt because based on the data, the student debt increased but the percentage of students in debt didn't necessarily increase year by year. Once that decision was made, I decided Percentage of Students in Debt would be an additional piece of information I wanted to display and after looking at a few options(like an option on the map to toggle for the two types of data) decided that a "bubble" would be a nice addition to overlay on the map. Since percentage has only a limited range, the "bubbles" would be limited in size and wouldn't add too much clutter on the map(this is also the reason why a squareroot scale in the code didn't make sense to me when using it for the radius of the bubble because the range is so limited). 

With my encodings decisions finalized, I did a little bit of online research and found a pre-defined color scale d3.scale.category10() to use for the different ranges of the average debt($0 - $54,999). I decided to use unique colors for easy correlation(also added a legend to help the user correlate). On the same map I used a custom scale to convert percentage of students in debt to varying sized circles. These circles are displayed on top of each state, approximately centered at the center of each state.

The data I have varies based on the academic year(for example "2003-04") and also based on the type of school("Private" or "Public"). For better user interaction, I went for a slider for the user to change the year and radio buttons to change the school type.

#### Revision 2( http://bl.ocks.org/spgitmonish/raw/efbe68d690f006e3f2b0/ )
After going through all the feedback from my friends, I decided to make significant changes in my visualization. One of the main takeaways for me was to change the color scheme from random colors to a gradient, that way as the user goes from year to year, the increase in debt is more evident i.e. a heat map!.

From the feedback it was pretty obvious that users had a tough time understanding the size of the circle and correlating it to the percentage. So to make this more obvious for the users, I added a tooltip and a legend. The tooltip displays more detailed information when the user hovers using the mouse over the circles because Percentage of Students is only an additional piece of information to go along with Average Debt of Students. 

Other modifications I made was to add a legend entry to help the user correlate for when the data was not available for the selected year and school type(this was again in response to the universal feedback). Since a couple of users were curious as to where I got my data, I also added my source at the bottom of the map.

Finally decided to display "National" data in a little box as I liked the suggestion from User 1.

### Feedback
#### User 1  
*What do you notice in the visualization?*  
Map of the United States with each state color coded based on the student debt situation.
The Colors change as the years are changed. The visualization also shows a circle
for each state indicating % in debt. The visualization can toggle between data
for private and public schools.

*What questions do you have about the data?*       
Where was this data taken from?
Do the total number of students per state increase/decrease over time as the avg
debt increases? What is the percent in debt in numbers? - Not able figure out the
percent in debt from the size of the circle

*What does white color mean?*  
There is no avg debt number associated with white.

*What relationships do you notice?*  
Every color has an avg debt number associated with it.
The circle size determines the % of students in debt.
As you change the year the colors change for the dates based on updated data.
The data differs as you toggle between private and public schools.

*What do you think is the main takeaway from this visualization?*  
Avg student increases every year from 2004 to 2013

*Is there something you don’t understand in the graphic?*  
The white color for a state and I’m not able to tell the % in debt from the size
of the circle

*Any other suggestions? Feedback? Improvements?*  
Maybe you can show actual % in debt numbers when I hover or click on a circle
It would also be interesting to have a comparison table where I can compare avg
debt for two different years - say I want to compare between year 2007 and year 2010
I want to know what the average debt for USA as a whole is for every year?

#### User 2
*What do you notice in the visualization?*  
I notice that is addresses student debt in two categories, public and private
schools and the percentage of students that come out of school in debt.

*What questions do you have about the data?*  
I was wondering what the source was on it. You might want to add that so people
know instantly where the numbers came from. This shows how the Denver Post sources look:
http://www.denverpost.com/portlet/article/html/imageDisplay.jsp?contentItemRelationshipId=7125117

*What relationships do you notice?*    
I noticed that the debt in the east coast seems to be higher than in other locations and that their seems to be a general correlation with region and costs.

*What do you think is the main takeaway from this visualization?*  
Student debt is increasing.

*Is there something you don’t understand in the graphic?*    
I find the impact of the information difficult to measure because the different colors are distracting. Instead of seeing a gradual change I just see lots of colors changing.

*Any other suggestions? Feedback? Improvements?*  
I would also like the option to click through the years rather than just scroll.
That way I could slowly go through each year and process the information more completely.
I like that the scroll option is there but I think also being able to click through
would be nice and have the years listed closer to the scroll/click area so people
are more aware of the year.


#### User 3
*What do you notice in the visualization?*  
Colors do not go in a gradient, making it hard to see trends
Circles have no sense of scale... I can't tell if that circle is 100% or 15%

*What questions do you have about the data?*  
Where did this data come from? No sources cited on the page.

*What relationships do you notice?*  
Debt is increasing over time, cannot tell if percentage of debt is increasing or
decreasing. Debt is relatively similar across the USA

*What do you think is the main takeaway from this visualization?*  
Total debt has increased over the past 10 years

*Is there something you don’t understand in the graphic?*  
What percentage is each circle size?
What does white mean? (I assume no data, but that isn't in the key)
Where did the data come from?

*Any other suggestions? Feedback? Improvements?*  
I like the slider and being able to switch via the bullets to go private/public
Change colors, use a gradient rather than random colors. Put a percentage number
in the bubble, or have a way to change between total debt and percentage in debt
(another toggle on the map). Good size of map.

### User 4
*What do you notice in the visualization?*  
I understood that you are trying to portray the average debt in every state for
different time periods. I like the different colors and could easily map the
amount to each color.

*What questions do you have about the data?*  
What is the %debt for each state ? I see the circle you put in each state but
did not really understand what the circle means.

*What relationships do you notice?*  
I picked Kansas to follow from year 1 to the end and noticed that the average
debt has only been increasing or remains at a stage and has definitely not
decreased (again not sure what white means).

*What do you think is the main takeaway from this visualization?*  
The average debt was very clear to understand with the colors.

*Is there something you don’t understand in the graphic?*  
I could not understand what the circle means clearly, and also what does the
color white mean ? Does it mean no debt?

*Any other suggestions? Feedback? Improvements?*  
The %debt based on circle size is not too clear, maybe mention that clearly,
I was trying to click the circles thinking it might pop up some info.
Also, if you can indicate what the white color means it would be good.

### Resources
The following links are the sources I used for finishing up my Project  
http://bost.ocks.org/mike/bubble-map/  
http://bl.ocks.org/mbostock/4342045  
http://bl.ocks.org/d3noob/10632804  
http://bl.ocks.org/biovisualize/1016860  
http://bl.ocks.org/rveciana/5181105  
