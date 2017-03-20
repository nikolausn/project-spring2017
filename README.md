# TOTORO
# Final Project: LIS590DV - Spring 2017
Data Visualization (LIS590DV) Final Project, by Totoro group

Your final project is composed of four parts.  You will work in groups of three
or four people; each person will be expected to participate in the project.

Note that in some cases, the descriptions of *what* you are to visualize are
somewhat vague.  This is in keeping with our discussion of carefully choosing
the story you want to tell.  You're going to be called upon in this assignment
to examine the data, and then within the rough outlines of the discussion,
construct a visualization that "answers" the posed question.

There are a few important notes:

 * All of the source code must be provided.
 * Use GitHub to version your code and your writeup.  This will also be used to
   verify individual contributions.
 * The writeup will be evaluated.
 * A "visualization" does not mean a single plot; it is broadly defined to
   include linked visualizations, collections of plots, etc.

## Component 1: Procedural, Bespoke Visualization

**Concept**: Tell us about the routes in the Champaign-Urbana Metro Transit
District.

Your first dataset will be based on the [CUMTD](http://cutmd.com/) data.  There
are several feeds available.  A copy of an example feed will be provided in
this repository; you should also feel free to scrape at regular intervals.
Data sources can be found at http://developer.cumtd.com/ .  In particular,
check the [GTFS](https://developers.google.com/transit/gtfs/reference/) data
feed, which is provided in zipfile form (and updated with regularity.)

Your visualization should be constructed in a procedural way, and should be
suitable for static viewing.  (i.e., it should be non-interactive.)

A few of the possible concepts to explore are listed below; please note that
these should be considered starter points, and you should explore beyond them.

 * How quickly do buses go?  How does this vary based on time of day, region,
   route, etc?
 * How many stops are there?  What is their density?
 * How many buses are there on each route?  Does this correlate with stop
   density?

Generate from this a single PDF or PNG.

## Component 2: Interactive, Bespoke Visualization

**Concept**: What is the distribution of [IMLS](http://imls.gov/) grants, and
what do these grants do?

Your second dataset will be the [IMLS](http://imls.gov/) discretionary grants
database.  These grants include information about the topic of the grant, the
institution that received it, its duration, and a few other pieces of data.
You may also find useful and interesting data (especially related to zip codes
and economic factors) at [FRED](http://fred.stlouisfed.org).

Your visualization should be interactive. There are several frameworks you can
use to do this.  The three that we have discussed in detail in class have been
using the [IPython widgets](http://ipywidgets.readthedocs.io) interface to
build small, exploratory visualizations, the [Bokeh
framework](http://bokeh.pydata.org) and [Plotly](http://plot.ly/).
You may not use Tableau to build this visualization.  If there is another
framework you would like to use, please ask.

A few of the concepts that you may explore:

 * What types of grants are supported by IMLS?
 * How are these grants distributed across the United States?  Are they
   particularly clustered in certain states?
 * Is there a relationship between the economic factors in a zip code and the
   grants from IMLS?

Generate from this data either a notebook that can be executed, a python script
that can be executed, or a plotly dashboard that can be accessed.  If you
utilize plotly, at lease some of the plotly setup must be in a python script.

## Component 3: System for Receiving New Data

**Concept**: Given limited information about a dataset, what types of
all-purpose visualizations can you construct to provide an overview of the
data?

You will build a function which will either produce a visualization (either
static or interactive) that provides an overview of the data.  This may mean
applying heuristics to the data to guess at different possible interesting
characteristics.  This function should accept a pandas dataframe.

The data will have **at least** eight columns:

 * Name
 * Date
 * Latitude, longitude
 * At least 1 Categorical label
 * At least 3 Quantitive columns

There will be three sample datasets provided.

## Component 4: Narrative Report Around a Dataset

This is forthcoming; it will be built on the CUMTD dataset.

## Final Writeup

You will be tasked with providing a writeup of your visualizations as well.
Each should be in markdown form and in the directory with your visualizations.
These should describe in some detail:

 * Why you took the approach you did
 * Strengths of your approach
 * Weaknesses of your approach
 * What you wished you had been able to do (if anything)
 * Who in the group contributed each part of the visualization (from code, data
   management, data cleaning, writeup, and so on.)
