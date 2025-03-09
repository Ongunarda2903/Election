# 📊 Analysis of Application X for Predicting Parliamentary General Election Results

## 📋 Project Proposal
In this project, I will analyze **Application X** to find a correlation between:
- Number of tweets 
- Average number of likes to tweets 
- Average number of comments to tweets 

and the results of parliamentary general elections. 

Based on the correlation I find, I will predict the possible outcome of the next parliamentary general election. The prediction will be made using the number of tweets, likes, and comments between the last election and the upcoming election (which has not happened yet). 

---

## 📊 Description of Dataset

### 🟢 1. Number of Tweets
- **Latest Election:**  
   - I will collect tweets from the **five years** between the last parliamentary election and the second to last election.  
   - Only tweets with a **positive relationship** to a party will be included.  
   - **Positive relationship:**  
      - Specific keywords will be used to filter tweets.  
      - If a tweet contains any of these keywords, it will be included.  

- **Second to Last Election:**  
   - Same approach as above but for the period between the second to last election and the one before it.

---

### 🟢 2. Average Number of Likes
- **Latest Election:**  
   - I will calculate the **average number of likes** for tweets related to the latest election.  

- **Second to Last Election:**  
   - Same method as above for tweets related to the second to last election.

---

### 🟢 3. Average Number of Comments
- **Latest Election:**  
   - I will calculate the **average number of comments** for tweets related to the latest election.  

- **Second to Last Election:**  
   - Same method as above for tweets related to the second to last election.

---

### 🟢 4. Election Vote Percentage
- **Latest Election:**  
   - The percentage of votes each party received in the **latest parliamentary election**.  

- **Second to Last Election:**  
   - The percentage of votes each party received in the **second to last parliamentary election**.  

---

## 📥 Data Collection

### 🟢 1. Collecting Data from Application X
- I will use **`snscrape`** to collect:  
   - Number of tweets  
   - Likes  
   - Comments  

- **CSV File:**  
   - Collected data will be saved in a CSV file.  
   - The CSV will be **continuously updated** with new tweets.  

- **Updating CSV:**  
   - To update the CSV file, I will use:  
     ```python
     mode='a'
     ```
   - This will **append new tweets** without deleting the existing data.  
   - The updated CSV will be used to predict the next election results.

---

### 🟢 2. Collecting Data from YSK (Election Results)
- **Source:** YSK’s official website.  
- **Tool:** **`Selenium`** to collect:  
   - Percentage of votes each party received in the last two elections.  

---

### 🟢 3. Future Elections: Automatic Data Collection
- **Problem:** How to collect data for future elections that haven’t happened yet?  
- **Solution:**  
   - Use **`schedule`** to check YSK’s website periodically for new election results.  
   - If new results are available, they will be **appended to the CSV** using `mode='a'`.  

---

