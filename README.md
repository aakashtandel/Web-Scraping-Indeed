# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web Scraping & Classification

### Description

In week four we've learned about webscraping, and a few different classifiers. In week five we'll learn Natural Language Processing and some additional classification methods. Now we're going to put those skills to the test.

### Scenario

You're working as a data scientist for a contracting firm that's rapidly expanding. Now that they have their most valuable employee (you!), they need to leverage data to win more contracts. Your firm offers technology and scientific solutions and wants to be competitive in the hiring market. Your principal thinks the best way to gauge salary amounts is to take a look at what industry factors influence the pay scale for these professionals.

Aggregators like [Indeed.com](https://www.indeed.com) regularly pool job postings from a variety of markets and industries. Your job is to understand what factors most directly impact data science salaries and effectively, accurately find appropriate data science related jobs in your metro region.

#### Project Summary

In this project, we will practice two major skills. Collecting data by scraping a website and then building a binary predictor.

We are going to collect salary information on data science jobs in a variety of markets. Then, using the location, title, and summary of the job, we will attempt to predict a corresponding salary for that job. While most listings *DO NOT* come with salary information (as you will see in this exercise), being to able extrapolate or predict the expected salaries for other listings will be extremely useful for negotiations! :)

Normally we could use regression for this task; however, we will be converting this into a classification problem.

- **Question**: Why would we want this to be a classification problem?
- **Answer**: While more precision may be better, there is a fair amount of natural variance in job salaries; therefore, predicting a range **(above the median or below the median)** may be useful.

The first part of assignment will focus on scraping [Indeed.com](www.indeed.com) and the second will focus on using the listings with salary information to build a model and make predictions.

Your job is to:

1. Collect data from [Indeed.com](www.indeed.com) on data science salary trends for your analysis.
  - Select and parse data from at least 1000 postings for jobs, potentially from multiple location searches.
2. Find out what factors most directly impact salaries (title, location, department, etc.). In this case, we do not want to predict salary as would be done in a regression. Your boss instead believes that salary is better represented in categories. These categories will be **1 if above the median, and 0 if below the median**. If a salary happens to be at the median, allot that to the "0" category.
  - Test, validate, and describe your models. What factors predict salary category? How do your models perform?
  - You must engineer multiple features based on text (i.e. job title, job qualifications, etc.).
3. Discover which features have the greatest importance when determining a low vs. high paying job.
  - Your Boss is interested in what overall features hold the greatest significance.
  - HR is interested in which SKILLS and KEY WORDS hold the greatest significance.   
4. Author a report to your principal detailing your analysis.

**BONUS PROBLEMS:**
1. Your boss would rather tell a client incorrectly that they would get a lower salary job than tell a client incorrectly that they would get a high salary job. Adjust one of your models to ease his mind, and explain what it is doing and any tradeoffs. Plot the ROC curve.
2. Text variables and regularization:
  - **Part 1**: Job descriptions contain more potentially useful information you could leverage. Use the job summary to find words you think would be important and add them as predictors to a model.
  - **Part 2**: GridSearch parameters for Ridge and Lasso for this model and report the best model.
3. It’s not enough to know if a position will fall into one of two categories, your boss wants to be able to classify a salary to a tens-of-thousands range (or better yet thousands).  


**Goal:** Scrape & clean data, run your model, derive insights, present findings.

---

### Requirements

- Scrape and prepare your data using BeautifulSoup.
- **Create and compare two models**. One of these must be a random forest, however the other can be a classifier of your choosing: logistic regression, KNN, or SVM.
- A Jupyter Notebook with your analysis for a peer audience of data scientists.
- A written report directed to your (non-technical!) principal.
- A 10-12 minute presentation outlining your process and findings for a non-technical audience.

 **Pro Tip:** You can find a good example report [here](https://www.dlsweb.rmit.edu.au/lsu/content/2_assessmenttasks/assess_tuts/reports_ll/report.pdf).

 **Pro Tip 2:** Scraping is one of the most fun, useful and interesting skills out there!  Don’t lose out by copying someone else.
---

### Necessary Deliverables / Submission

- Materials must be in a clearly labeled Jupyter notebook.
- Materials must be pushed to student's GitHub master branch.
- Materials must be submitted by 9 a.m. Friday, July 28th.

---

### Dataset

1. We'll be utilizing a dataset derived from live web data: [Indeed.com](https://www.indeed.com)

2. To get the data, we will use the requests library and BeautifulSoup to scrape the webpage.

---

### Suggested Ways to Get Started

- Read the docs for whatever technologies you use. Most of the time, there is a tutorial that you can follow, but not always, and learning to read documentation is crucial to your success!
- Document **everything**.
- Look up sample executive summaries online.

### Additional Resources
- [Advice on How to Write for a Non-Technical Audience](http://programmers.stackexchange.com/questions/11523/explaining-technical-things-to-non-technical-people)
- [Documentation for BeautifulSoup can be found here](http://www.crummy.com/software/BeautifulSoup/).

---

### Project Feedback + Evaluation

[Attached here is a complete rubric for this project.](./project-04-rubric.md)

Your instructors will score your project using the scale below:

    Score | Expectations
    ----- | ------------
    **0** | _Incomplete._
    **1** | _Does not meet expectations._
    **2** | _Meets expectations, good job!_
    **3** | _Exceeds expectations, you wonderful creature, you!_
