# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Exploratory Data Analysis & Recommendation

### Overview

Our first section of DSI covers:
- basic statistics (distributions, confidence intervals, hypothesis testing)
- many Python programming concepts
- programmatically interacting with files and directories
- visualizations
- EDA
- working with Jupyter notebooks

You might wonder if you're ready to start doing data science. While your have lots to learn, there are many aspects of the data science process that you're ready to tackle. Project 1 aims to allow you to practice and demonstrate these skills.

For our first project, we're going to take a look at aggregate SAT and ACT scores and participation rates from each state in the United States. We'll seek to identify trends in the data and combine our data analysis with outside research to identify likely factors influencing participation rates and scores in various states.

You will be asked to come up with a data science problem. Here's a specific prompt that should help you craft this statement:
> The new format for the SAT was released in March 2016. As an employee of the College Board - the organization that administers the SAT - you are a part of a team that tracks statewide participation and recommends where money is best spent to improve SAT participation rates. 

>Your presentation and report should be geared toward **non-technical** executives with the College Board. You will use the provided data and outside research to make recommendations about how the College Board might work to increase the participation rate in a **state of your choice**.

---

### Datasets

#### Provided Data

For this project, you'll have six provided datasets:

- [2017 SAT Scores](./data/sat_2017.csv)
- [2017 ACT Scores](./data/act_2017.csv)
- [2018 SAT Scores](./data/sat_2018.csv)
- [2018 ACT Scores](./data/act_2018.csv)
- [2019 SAT Scores](./data/sat_2019.csv)
- [2019 ACT Scores](./data/act_2019.csv)

These data give average SAT and ACT scores by state, as well as participation rates for the classes of 2017, 2018, and 2019.

You can see the sources for the SAT data [here](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/) and [here](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent), and the sources for the ACT data [here](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows) and [here](https://www.act.org/content/act/en/research/reports/act-publications/condition-of-college-and-career-readiness-2017.html). **Make sure you cross-reference your data with your data sources to eliminate any data collection or data entry issues.**

#### Additional Data
(_This data is for your reference only. It is not needed to complete the project. You are required to include all of the above csv data._)

2018 and 2019 state-by-state average results and participation for the SAT are available in PDF reports [here](https://reports.collegeboard.org/sat-suite-program-results/state-results). 2018 ACT state-by-state mean composite scores and participation rates are [here](http://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf) and 2019 data can be found [here](https://www.act.org/content/dam/act/secured/documents/cccr-2019/Average-Scores-by-State.pdf).

**This data has been compiled into CSV files which are also included in the *data* directory of this repo**

---

### Deliverables

All of your projects will comprise of a written technical report and a presentation. As we continue in the course, your technical report will grow in complexity, but for this initial project it will consist of:
- A Jupyter notebook that describes your data with visualizations & statistical analysis.
- A README Markdown file the provides an an overview of your project.
- Your presentation slideshow rendered as a .pdf file.
**NOTE**: Your entire Github repository will be evaluated as your technical report. Make sure that your files and directories are named appropriately, that all necessary files are included, and that no unnecessary or incomplete files are included.

For your first presentation, you'll be presenting to a **non-technical** audience. You should prepare a slideshow with appropriately scaled visuals to complement a compelling narrative. Make sure you have little text on each slide and that your fonts are large.

Ensure that your recommendations make sense. These datasets have some limitations - think about granularity, aggregation, the relationships between populations size, rates, and performance. Consider the actual populations these data are drawn from.

It is okay if your conclusions are tentative. You do not want to make unsupported jumps in logic.

A rubric is available [here](./rubric).

---

### Technical Report Starter Code

Future projects will require you to decide on the entire structure of your technical report. Here, we provide you with suggested [starter code](./code/starter-code.ipynb) in a Jupyter notebook that will help to guide your data exploration and analysis. 

- Use Markdown cells to make your notebook easy to understand. 
- Use docstrings for any functions or classes.
- Comment your code cells as needed for clarity. 

---

### Suggested Resources

Here's a link on [how to give a good lightning talk](https://www.semrush.com/blog/16-ways-to-prepare-for-a-lightning-talk/), which provides some good recommendations for short presentations.

[Here's a great summary](https://towardsdatascience.com/storytelling-with-data-a-data-visualization-guide-for-business-professionals-97d50512b407) of the main points of the book _Storytelling with Data_, which I can't recommend enough. [Here's a blog post](http://www.storytellingwithdata.com/blog/2017/8/9/my-guiding-principles) by the author about his guiding principles for visualizations.

---

### Submission

**Your slides must be ready for presentation by the beginning of class on Monday, December 14.**

**Materials must be submitted in your GitHub repo and linked to in Google Classroom by 9pm ET on Dec 14.**

Your technical report will be hosted on Github Enterprise. Make sure it includes:

- A README.md (that isn't this file)
- Jupyter notebook(s) with your analysis (renamed to describe your project)
- Data files
- Presentation slides
- Any other necessary files (images, etc.)

---

### Presentation Structure

- **Maximum speaking time is 10 minutes. Then there will be a few minutes for Q & A.**
- Use Google Slides or some other presentation software (Keynote, Powerpoint, etc).
- Consider the audience. Assume you are presenting to non-technical executives with the College Board (the organization that administers the SATs).
- Start with the **problem**.
- Use visuals that are appropriately scaled and interpretable.
- Talk about your procedure/methodology (high level, **CODE IS ALWAYS INAPPROPRIATE FOR A NON-TECHNICAL AUDIENCE**).
- Talk about your primary findings.
- Make sure you provide 1 or 2 **clear recommendations** that follow logically from your analyses and answer your problem.
- Ensure that your recommendations make sense based on the data and your analysis. Watch out for jumps in logic that are unjustified!

**Be sure to rehearse and time your presentation before class.**


### Remember:

This is a learning environment and you are encouraged to try new things, even if they don't work out as well as you planned! While this rubric outlines what we look for in a _good_ project, it is up to you to go above and beyond to create a _great_ project. **Learn from your failures and you'll be prepared to succeed in the workforce**.


### Have fun on this learning exercise! 

Don't stress out or overthink it! You'll be okay! 😀