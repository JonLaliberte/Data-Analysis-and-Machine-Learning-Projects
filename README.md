

## Original README:
# Randy Olson's data analysis and machine learning projects

This is a repository of code and data for my data analysis and machine learning projects.

Each repository will (usually) correspond to one of the blog posts on my web site, http://www.randalolson.com/blog/

Be sure to check the documentation (usually in IPython Notebook format) in the directory you're interested in for the notes on the analysis, code license, data usage terms, etc.

If you don't have the necessary software installed to run IPython Notebook, don't fret. You can use [nbviewer](http://nbviewer.ipython.org/) to view a notebook on the web.

For example, if you want to view the notebook in the `wheres-waldo-path-optimization` directory, copy the [full link](https://github.com/rhiever/Data-Analysis-and-Machine-Learning-Projects/blob/master/wheres-waldo-path-optimization/Where's%20Waldo%20path%20optimization.ipynb) to the notebook then copy it into [nbviewer](http://nbviewer.ipython.org/github/rhiever/Data-Analysis-and-Machine-Learning-Projects/blob/master/wheres-waldo-path-optimization/Where%27s%20Waldo%20path%20optimization.ipynb).

# My Changes
My only changes are to the optimal-road-trip python script (and my first real use of python, so excuse any faux pas).
I didn't really care so much about how well I did this, I just wanted to be able to test additional waypoints faster, so here we go...
Changes:
	Use the tsv file as a cache, so you can now add a location to the waypoint set and it will only have to hit gmaps for n-1 calculations instead of n^2. If you're planning a roadtrip this saves you a ton of time when checking if a new location will add significantly to your trip. Previously if you added a new waypoint you'd lose all the already calculated paths.
	Changed files to be saved using miles in the file name instead of meters, because that makes more sense to me when planning a trip.
	Display miles(again, instead of meters) when printing at each milestone iteration of the genetic algorithm
