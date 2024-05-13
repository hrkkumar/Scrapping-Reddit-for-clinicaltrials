# Scrapping-Reddit-for-clinicaltrials
**README**

### Setup Instructions
1. Clone the repository to your local machine.
2. Install the required packages by running `pip install -r requirements.txt` in the terminal.(Note that this code was executed on Google Collab hence the requiremens.txt might be big instead try to implement directly on collab as per notebook)
3. Set up your Reddit API credentials by replacing `client_id`, `client_secret`, and `user_agent` with your own credentials.
4. Set up your OpenAI API key by replacing `openai.api_key` with your own key.
5. Run the script by executing `python script_name.py` in the terminal.

### Methodology and Challenges
This project utilizes natural language processing (NLP) and machine learning techniques to analyze Reddit posts and comments about medical research and clinical trials. The methodology includes:
- Data collection from relevant subreddits using the Reddit API.(Subreddits were chosen by querying MetaAI(Llama 3) as it could potentially give subreddits with the data until 2023) 
- Data preprocessing involving tokenization and padding.
- Sentiment analysis using a pre-trained model(twitter-roberta-base-sentiment-latest).
- Personalized message generation with OpenAI's GPT-3.5-turbo-instruct model.

Challenges faced during the project:
- Handling the large volume of data collected from the Reddit API.
- Finding the appropriate subreddits that would contain posts and comments related to clinical trials and health conditions related to it
- Choosing a model for performing sentimental analysis on medical-related text since here the Reddit posts may or may not be completely medical. I have used a pre-trained model for this project which could be further improved with In-house models.
- Since the Open AI account is of the free tier you may not execute many calls you might easily exceed the quota allocated to you, Hence make sure that you have a separate account dedicated to running this project if possible.

### Data Collected, Analysis Performed, and Messages Generated
#### Data Collected:
- Posts and comments from subreddits related to medical research and clinical trials.
#### Analysis Performed:
- Sentiment analysis results for each post and comment.

#### Messages Generated:

##### Negative Sentiment
###### Post: Free healthcare in Belize destroyed my niece's health.Free though
###### message generated
![image](https://github.com/hrkkumar/Scrapping-Reddit-for-clinicaltrials/assets/163475218/c573b284-5c46-46d0-96ad-8faaedb184ba)

##### Positive Sentiment
###### Post: I honestly can't thank you enough for sharing this. Because of this post, im sitting in the waiting room after getting my first vaccine in the Moderna adolescent trial. Thank you so much
###### message generated
![image](https://github.com/hrkkumar/Scrapping-Reddit-for-clinicaltrials/assets/163475218/85e8480d-2f2f-4551-9373-ed1434d66d00)

### Ethical Considerations
1. **Transparency:** Ensured transparency in data collection and analysis methods by searching through the most trusted subreddits posts based on the reliability percentage
2. **Privacy:** Avoided collecting personally identifiable information (PII) from Reddit users by masking emails and phone numbers in the data.
3. **Bias Prevention:** Implemented measures to prevent bias in sentiment analysis and generated messages by tailoring the output according to the context.

