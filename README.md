from textblob import TextBlob
def analyze_sentiment(text):
    blob = TextBlob(text)
    polarity= blob.sentiment.polarity

    if polarity > 0:
        return "Positive"
    elif polarity < 0:
        return "Negative"
    else:
        return "Neutral"
user_answer= input("Enter a statement: ")
result = analyze_sentiment(user_answer)
print(f"Sentiment: {result}")
