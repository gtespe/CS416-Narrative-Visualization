# Messaging
My narrative visualization tackles the topic of climate change. I wanted to show a relationship between carbon emissions and oil drilling, and contrast this with the net-zero emissions goals many countries have set. I want to convey the message that we have not been doing enough to reduce our emissions, and need to make changes to reach our climate goals. My data comes from three publicly available sources, a UNFCCC overview on climate change, an OECD report on crude oil production, and Our World In Data for the net zero targets. The datasets can be found here:

https://www.kaggle.com/datasets/ulrikthygepedersen/co2-emissions-by-country

https://www.kaggle.com/datasets/caesarmario/oecd-data-crude-oil-production

https://ourworldindata.org/grapher/net-zero-target-set

# Narrative Structure
I used an interactive slideshow structure for my narrative visualization. It is made up of three slides, and the user can choose to move forward or backwards through the story. Additionally, each of the three visualizations is interactive in that the user can drill down into the data and receive "details on demand" by mousing over points on any of the three slides.

# Visual Structure
The structure of my slides is simple yet clean and clear. I have titles in a large bold font, axes titles in a smaller bold font, color coded graphs and clearly marked axes. The graphs take center stage, with labeled navigation buttons at the bottom of the page. I used the same categorical color scheme from the d3 library, called "Tableau10". These colors are clearly distinct from one another, helping the user differentiate the nominal data.
 I standardized the location of the navigation button in order to maintain consistency across the slides. They are placed at the bottom of the slide, after the graph, to not distract from the visualization. Only after looking at the graph should the reader's eyes wander to the buttons, because we read top to bottom, left to right. The buttons are labeled clearly with both a name and a direction, to help the user navigate between the scenes more easily.

# Scenes
The first scene in my visualization shows how CO2 emissions have risen across the globe, using a stacked bar chart that is separated into regions. I chose to use regions for this first slide rather than countries, because I wanted to start with a broad overview, before getting into specific statistics about countries. Next, I present a line chart depicting Crude oil production for five different countries over time. The purpose of this chart is to incept the idea that countries' reliance on fossil fuels are the cause of the emissions, as well as the idea that countries are continuing to drill despite the damage they are causing to the planet. Finally, I contrast these two more complex graphs with a simple bar chart that shows when countries aim to reach net-zero emissions. I wanted the audience to question the countries' commitments to achieving these goals, as well as question the feasibility given the previous two graphs. 


# Annotations
My annotations across the slides are in a sans-serif font. The annotations will change when the reader mouses over a new data point, displaying a new tooltip. My tooltips all have the same opacity level and color, slightly offset from the cursor in order to not obscure the visualization. Rather than using 100% opacity, I used 85% so that the next datapoints will still be somewhat visible behind the tooltip. The charts are labeled with titles, axes titles, axis labels in the same location and format across the slides. Additionally, I provided a short description for the main purpose of the chart, below each of them. This annotation helps the user orient themselves, and understand the message I am trying to convey.


# Parameters
Because I used an interactive slideshow, the individual scenes are the primary selectable parameter for the user. Each of the navigation buttons is labeled with a succinct description of what the newly selected scene will display. When a user navigates to a new slide, the title of the scene is presented at the top in a large bold font, defining the state to the user. The labels on the navigation button will then change to reflect the new parameters available to be selected by the user.

# Triggers
The three triggers I implemented were "mouseover", "mouseout", and "mouseclick". When the user mouses over a datapoint, a tooltip will display details about that datapoint. When the user moves away from the same datapoint, that tooltip will be hidden. The user navigates between the slides by clicking their mouse on the navigation buttons at the bottom of the page.
One important affordance I have on my slides is the border on the navigation buttons. If you look closely, you will see that the top of the border is a lighter color, whereas the bottom of the border is a darker color. Because humans are used to seeing light illuminate objects from above, this evokes the perception that the button is raised on the page. This is a common technique to show that the button can be pressed. 
On the second slide, for crude oil production, I implemented an affordance by adding SVG circles over each of the backend data points on the line chart. This is to show the user which parts of the line chart are interactable.
