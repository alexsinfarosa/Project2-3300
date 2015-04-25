#CS 3300 - Project 2

###Part A

The data describes the European soccer season 2013-14 in Italy, Germany, France, Spain and England of their respective teams. Each team in a season plays twice against every other team participating the league, the first time in their hometown and the second in their opponent’s town.  The dataset provides the dates of the games for the 2013/14 season, the first half and final score of the games.  The number of soccer teams participating the soccer tournament in each of those european countries are 20. The data was obtained from Github: https://github.com/footballcsv. The variables are: Date, Team 1, Team 2, FT, HT, which represent  respectively the date of the game, the name of the home team, the name of the guest team, the score of the first half, and the score of the final game. 

The website provides datasets for various European countries, we decided to work with 5 countries. The data on the site are in CSV format and did not need any reformatting nor filtering. At first we were intentioned to convert those files to JSON and combine them together into a unique file. However, later on we opted to keep each country separated and to use CSV format instead. 

The graph provides information on soccer tournaments for the 2013/14 season in selected European countries. The user actively engages with the graph to obtain the desired information. For instance, if the user would like to know the results of any particular team he/she would just need first to click on one of the country buttons on the left of the graph and then select the desired team (Team 1). The collapsible tree diagram would expand showing all the soccer teams (Team 2), in chronological order, Team 1 has played against. More information are displayed once hovering on any of the Team 2. Such information contains the date, first half and final score.  

###Part B

We mapped the data using a tree layout in the following manner:
- The nodes represented the corresponding teams and countries. Note that each node was depicted as an svg circle in our project. The root of each tree would be the node that represents the country that the user selects. This node then has a path that leads to all the nodes that represent the teams that played in the selected country. Each of these nodes then has a path to another node for each team that they played against. Note that the first team selected denotes the home team and their child represents the away team.
- The children nodes of any node in our tree layout is only displayed when the parent node has been clicked on. If the parent node is clicked, the children nodes start from the parent node position and expand from radius of 1e^-6 to a radius of 4.5 pixels and extend to the right. Note that we also set a fixed-depth for each node by setting their y positions to their depth times 180.

###Part C
