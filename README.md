<H3>ENTER YOUR NAME : MOHAMED HAMEEM SAJITH J</H3>
<H3>ENTER YOUR REGISTER NO. 212223240090</H3>
<H3>DATE:29-04-25</H3>
<H1 Align="center">Project Based Experiment<H1>
  
### Objective:
Type your objective based on the question
  
### Program:
  ```
pip install pandas textblob
import pandas as pd
from textblob import TextBlob

# Load the CSV file into a DataFrame
df = pd.read_csv('fb_sentiment.csv')

# Function to perform sentiment analysis using TextBlob
def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

# Apply sentiment analysis to each row in the DataFrame
df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

# Output the DataFrame with sentiment analysis results
print(df.head())

# Filter out rows with positive sentiment (label 'P')
positive_feedback = df[df['Label'] == 'P']

# Output the negative feedback
print(positive_feedback)
```
### Output:
![image](https://github.com/user-attachments/assets/99c5d106-742c-4810-8791-310ed335908f)

![image](https://github.com/user-attachments/assets/f40ed6b0-311b-41d1-84f1-38b89f872654)

<H3>Inference:</H3>
Thus sentiment analysis using Facebook data is done and filtering the data that has only positive feedback for the code is executed successfully.
