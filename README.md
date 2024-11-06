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

### Limitations:
- **Rate Limiting**: Reddit API imposes limits on the number of requests that can be made within a certain period. If you hit the rate limit, the script will pause execution until the limit resets. This may cause delays in fetching data, especially if you're trying to retrieve a large number of posts.
  
  You can avoid hitting the rate limit by:
  - Reducing the number of posts fetched (`count` parameter).
  - Spacing out your requests using sleep intervals between them.
  
- **API Authentication**: If your Reddit API credentials are incorrect or have expired, you will encounter authentication errors. Ensure that your credentials (client_id, client_secret, user_agent) are correct and up-to-date.
  
- **Limited Access to Data**: The sentiment analysis only works with the posts available in the subreddits you've chosen. Reddit users may not always post content about healthcare, economics, or crime policies. You may not capture all public opinions on the topic.

- **NSFW and Moderation Issues**: Some subreddits may contain NSFW (Not Safe for Work) content, and if you try to access those, you may get blocked or restricted data. The script avoids NSFW subreddits to reduce the risk of encountering such content, but always verify the subreddit content yourself before proceeding.

- **Sentiment Analysis Accuracy**: The sentiment analysis is performed using the TextBlob library, which is not perfect. It may misclassify some posts, especially in cases where the language is ambiguous or uses sarcasm. Additionally, the polarity score might not always reflect the true sentiment accurately.

- **Post Deletions or Edits**: Reddit posts are often deleted or edited after they are published. This may result in missing or inconsistent data if posts are unavailable when the sentiment analysis is being performed.

- **Data Availability and Bias**: The sentiment analysis only reflects the posts retrieved from the specified subreddits. If a subreddit does not have many active discussions about healthcare, economics, or crime, the results may not be representative of the wider public opinion. Additionally, discussions in subreddits may be biased based on the demographic of the users who frequent them.

- **TextBlob Limitations**: TextBlob's sentiment analysis is based on basic text-processing algorithms and may not capture the nuances of complex statements or contextual meanings. If you need more advanced sentiment analysis, consider using a more sophisticated model such as BERT or VADER.

### Reddit API Credentials Template

To use the Reddit API, you need to create an application on Reddit and obtain the following credentials:
- **client_id**: This is a unique identifier for your Reddit application.
- **client_secret**: A secret key used to authenticate your application with Reddit.
- **user_agent**: A string that describes your application to Reddit.

#### Steps to Get Reddit API Credentials:
1. **Go to Reddit's Developer Portal**: [Reddit Developer](https://www.reddit.com/prefs/apps)
2. **Create a Reddit Application**:
   - Scroll down and click on **Create App**.
   - Fill out the required fields:
     - **Name**: Your application name (e.g., RedditSentimentAnalysis).
     - **App Type**: Select `script` as the app type.
     - **Description**: You can leave this blank or add a short description (optional).
     - **About URL**: You can leave this blank.
     - **Redirect URI**: Set this to `http://localhost:8000` (for testing purposes).
     - **Permissions**: You do not need any special permissions for this project.
3. **Save the credentials** after creating the application.

#### Template:
Here’s a template for adding your credentials to the code:

```python
client_id = 'YOUR_REDDIT_CLIENT_ID'        # Replace with your Reddit application's client_id
client_secret = 'YOUR_REDDIT_CLIENT_SECRET'  # Replace with your Reddit application's client_secret
user_agent = 'YOUR_REDDIT_USER_AGENT'       # Replace with a user agent string describing your app



