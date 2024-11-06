# Reddit Sentiment Analysis on Democratic Government Policies

This project performs sentiment analysis on Reddit posts related to the policies of the **Democratic Government**. The goal is to analyze how people feel about specific government policies in the domains of **Healthcare**, **Economics**, and **Crime**. It uses the **PRAW** (Python Reddit API Wrapper) library to fetch posts from relevant subreddits and **TextBlob** for sentiment analysis.

### Purpose:
The primary objective of this project is to:
- **Analyze public sentiment** regarding healthcare, economics, and crime policies.
- **Understand the impact** of the Democratic government's policies through Reddit discussions.
- **Provide a visual representation** of sentiment through pie charts for better insights.

### Steps:
1. **Fetching Posts**: The code fetches posts from multiple non-NSFW subreddits related to healthcare, economics, and crime policies.
2. **Sentiment Analysis**: It analyzes the sentiment of each post using TextBlob, classifying them as **Positive**, **Negative**, or **Neutral**.
3. **Visualization**: It generates a **pie chart** showing the percentage of positive, negative, and neutral posts for each category (Healthcare, Economics, Crime).

### Subreddits Used:
Below are the subreddits related to **Healthcare**, **Economics**, and **Crime** used for fetching posts:

#### **Healthcare**:
- `healthcare`
- `medicine`
- `mentalhealth`
- `healthcarepolicy`
- `AffordableCareAct`
- `universalhealthcare`
- `HealthPolicy`
- `Medicare`
- `Health`
- `AskDocs`
- `healthcareworkers`
- `MedicalEthics`
- `medtech`
- `PublicHealth`

#### **Economics**:
- `economics`
- `finance`
- `worldnews`
- `politics`
- `investing`
- `USPolitics`
- `libertarian`
- `Business`
- `Economics101`
- `PersonalFinance`
- `FinancialIndependence`
- `Economists`
- `MacroEconomics`
- `PoliticalEconomy`

#### **Crime**:
- `TrueCrime`
- `criminology`
- `politics`
- `law`
- `USPolitics`
- `CriminalJustice`
- `TrueCrimeDiscussion`
- `CriminalJusticeReform`
- `Law`
- `justice`
- `PoliceReform`
- `LegalAdvice`
- `LegalTips`
- `CriminalJustice`
- `PrisonReform`

### Libraries Used:
- **PRAW**: A Python package for interacting with Reddit's API.
- **TextBlob**: A library used to perform sentiment analysis on the text of Reddit posts.
- **Matplotlib**: Used for creating pie charts to visualize the sentiment analysis results.

### Setup:
1. **Install the Required Libraries**:
   You will need the following libraries:
   - `praw`
   - `textblob`
   - `matplotlib`

   You can install them using pip:
   ```bash
   pip install praw textblob matplotlib

