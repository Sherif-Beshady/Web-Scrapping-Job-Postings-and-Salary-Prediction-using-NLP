# Web-Scrapping-Job-Postings-and-Salary-Prediction-using-NLP

## Summary 
This project was leveraging a variety of skills. The first will be to use the web-scraping to collect data on data jobs from Indeed.com; Second is to choose a machine learning model and use it to answer the question below:

### *What are the factors that impact the salary of Data Jobs?*

To predict salary, I have built a classification model, using location, title, and summary of the job. I had created labels from these salaries (high vs. low salary, for example) according to thresholds (such as median salary). moreover, using NLP, I tried to classify the job category and Salary Range.

## Methods:
### 1. Web Scrapping

Web scraping is a very tedious and time-consuming job, and it is just like data cleaning a necessary evil for any data scientist to know. The most important thing is to be able to break down the scrapper and make sure it works in parts before the assembly. and don't try to scrap all at once if possible. 
In the web scraping notebook, you will find it divided into small working functions and then I have integrated everything into one large scrapper that will go to indeed, do the search, collect data and put it into a CSV file ready to the next step.

### 2. Data Preprocessing

In this part, I had to clean and prepare scrapped text data indeed and put the data into a proper structure for modelling.
Also, in this section, I decided to proceed using a classification model; consequently, i divided the salary into three categories :
Cat 0 - less Than 85k
Cat 1 - Between 85k and 120k
Cat 2 - More than 120k
hence, this was my way to go to Modeling step

### 3. NLP Modelling 
In this part, I wanted to build a classification model to classify salary based on job summary. I started with a NaiveBase  Classifier with TfidfVectorizer and CountVectorizer to compare performance, and surprisingly, CountVectorizer gave me better results.
Then I wanted to improve my prediction, so I feed my data to a pipeline using Logistic Regression and Stochastic Gradient Descent (SGD) with a grid search to tune hyperparameters.

### 4. Job Catagory Factors Identification - Topic Modeling using __*"Latent Dirichlet Allocation (LDA)"*__

In this part, I will try to find the factors that distinguish the job category using the LDA model to map all the documents to the topics that best describe the job categories following the steps below:
- Step 1: Convert documents to a single list/matrix.
- Step 2: Tokenization to break text into tokens using the help of regular expressions.
- Step 3: Stemming the words into roots
- Step 4: Stop words removal
- Step 5: Apply to all documents
