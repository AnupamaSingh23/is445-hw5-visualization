# Facebook Ego Network Visualization

## Plot 1: Histogram of Node Degrees

The first plot displays a histogram showing the distribution of Facebook users based on their number of friends (node degree). The X-axis represents friend counts, and the Y-axis shows how many users fall into each range. I used binning with a max of 30 bins for readability. This plot helps understand how friend count is distributed across the network. The data was transformed using NetworkX to compute degree for each node.

<iframe src="assets/histogram.html" width="100%" height="500px" frameborder="0"></iframe>

## Plot 2: Scatterplot of Degree vs Centrality

The second plot compares each user's number of friends with their betweenness centrality. Each point represents a user, and the color intensity reflects the centrality value using the 'plasma' scheme. I computed centrality using NetworkX and mapped the values to their node IDs. This visualization helps identify key influencers in the network.

<iframe src="assets/scatterplot.html" width="100%" height="500px" frameborder="0"></iframe>

## Interactivity Feature

I added a slider to filter users by maximum degree. This lets users explore how centrality varies among users with different friend counts. The slider was implemented using Altair’s `param` and `transform_filter`, which is more interactive than Altair’s default `.interactive()`.

<iframe src="assets/interactive_plot.html" width="100%" height="600px" frameborder="0"></iframe>

---

### The Data  
[facebook_combined.txt.gz](https://snap.stanford.edu/data/facebook_combined.txt.gz)

### The Analysis  
[Notebook on GitHub](https://github.com/AnupamaSingh23/is445-hw5-visualization/blob/cfeac33efd5e13e08a31a38080b75c732c1317fd/Workbook.ipynb)
