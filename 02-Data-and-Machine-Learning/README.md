
---

# AI vs Machine Learning vs Deep Learning

Let’s simplify this.

## Artificial Intelligence (AI)

AI is the broad field. It includes systems that mimic human intelligence and perform tasks like reasoning, decision-making, and problem-solving.

AI is the umbrella.

## Machine Learning (ML)

Machine Learning is a subset of AI. It focuses on algorithms and statistical models that learn patterns from data instead of being explicitly programmed with rules.

Examples:
- Spam vs Not Spam
- Product recommendations
- Language translation

## Deep Learning (DL)

Deep Learning is a subset of Machine Learning. It uses neural networks with many layers (deep networks), inspired by how the human brain processes information.

Examples:
- Image recognition (Dog vs Cat)
- Speech recognition (Voice assistants)
- Self-driving systems

Quick hierarchy:

AI  
└── Machine Learning  
  └── Deep Learning  

---

# The Machine Learning Workflow

Machine Learning follows a lifecycle. It starts with data and ends with a deployed model that makes predictions in the real world.

## Step 1: Data Collection

Data can come from many sources, such as:
- Databases
- Sensors
- Web scraping
- APIs
- ERP systems
- CRM systems
- HR systems
- Customer support logs
- Social media
- Reviews
- Clickstream data

## Step 2: Data Preprocessing

Raw data is usually messy. It may include missing values, duplicates, noise, or inconsistent formats.

Preprocessing includes:
- Cleaning
- Standardizing formats
- Handling missing values
- Removing duplicates

Goal: make the data usable for the model.

## Step 3: Feature Engineering

A feature is a measurable property or characteristic that helps the model learn.

Example (Smartphone):
- Screen size
- Battery capacity
- Storage

Example (House price prediction):
- Year built
- Bedrooms
- Bathrooms
- Square footage
- Location

Feature engineering means:
- Selecting useful features
- Transforming features into usable formats
- Creating new features when needed

This is one of the most important steps in Machine Learning.

## Step 4: Train-Test Split

We typically split data into:
- Training data (example: 70%)
- Evaluation/Test data (example: 30%)

Reason: we must test how the model performs on new data it has never seen before.

## Step 5: Model Training

Training is the learning phase. Think of it like a student going to school.

The model learns patterns from training data and builds an internal “understanding” of what signals matter.

## Step 6: Model Evaluation

Now we test the model using the evaluation data.

We measure:
- Accuracy
- Precision
- Recall
- F1 score (and more)

If the model performs poorly, we improve it.

## Step 7: Model Tuning

We adjust:
- Hyperparameters
- Feature selection
- Model settings

This is iterative. Train, test, tune, repeat.

## Step 8: Model Deployment (Inference)

Once performance is good, we deploy the model.

Deployment means the model is now used in real life, such as:
- Detecting spam emails
- Identifying fraud transactions
- Predicting house prices
- Recognizing objects in images

Inference refers to the model making predictions after deployment.

---

# Types of Data

Data can be grouped into three categories.

## Structured Data

Structured data fits into rows and columns, like spreadsheets and relational databases.

Examples:
- Sales tables
- Employee records
- Finance transactions

## Unstructured Data

Unstructured data does not fit neatly into rows and columns.

Examples:
- Images
- Videos
- Audio
- PDFs
- Emails
- Word documents

Most enterprise data is unstructured.

## Semi-Structured Data

Semi-structured data sits between structured and unstructured. It has partial organization.

Examples:
- JSON
- XML

---

# Data Types: Qualitative and Quantitative

## Qualitative (Categorical)

### Nominal
Categories without an inherent order.

Examples:
- Gender
- Hair color
- Country

### Ordinal
Categories with a natural order.

Examples:
- Education level (Bachelor’s, Master’s, PhD)
- Grades (A, B, C)

## Quantitative (Numerical)

### Discrete
Countable whole numbers.

Examples:
- Number of students
- Number of cars

### Continuous
Values that can include decimals.

Examples:
- Height
- Temperature

---

# Metadata

Metadata means “data about data.”

Example (structured):
In a table, the column headers like Country, Capital, Population are metadata.

Example (unstructured):
For an image, metadata could be represented as key-value information, such as:
- Animal: Dog
- Breed: Golden Retriever
- Age: 4

Metadata helps machines interpret and organize information.

---

# Data Pipeline

In real organizations, data typically flows through a pipeline:

Data Sources  
→ Collection  
→ Cleansing  
→ Preprocessing  
→ Transformation  
→ Storage (Data Lake)  
→ Machine Learning Model  

A data lake is a central place where large volumes of raw data from multiple sources are stored.

---

# Feature Engineering: The Diamond Analogy

Raw data is like an uncut diamond.

Feature engineering is the process of:
- selecting what matters
- transforming and shaping it
- making it valuable for learning

The model becomes effective only when the input features are meaningful.

---

# Real-World Example: Predicting House Prices

A house price prediction model might use features like:
- Year built
- Number of bedrooms
- Number of bathrooms
- Square footage
- Neighborhood
- School quality

The model learns how these features influence price based on historical examples.

---

# Key Takeaways

- AI is the broad field
- Machine Learning is a subset of AI
- Deep Learning is a subset of Machine Learning
- Data quality matters (garbage in, garbage out)
- Feature engineering often decides model quality
- Model development is an iterative cycle: train, evaluate, tune
- Deployment is when models deliver real value

---

# Reflection Questions

1. What kinds of data exist around you (personal, school, workplace)?
2. Which of that data is structured vs unstructured?
3. If you wanted to build a prediction system, what features would matter most?
4. Where do you see ethical concerns in how data is collected or used?

---

Next, we will go deeper into Machine Learning types and how models learn patterns from data.
