# **Project: Build a daily portfolio insights pipeline for multiple accounts by leveraging Gemini alongside the Google Search API to automatically generate portfolio returns and relevant news headlines.**

## **By feeding information of multiple accounts, and index returns from Yahoo Finance, we utilize the Google Gemini LLM to generate a daily portfolio and news summary**


## **Gemini LLM Generation for Multiple Client Accounts**
We utilise the Gemini LLM model, and using each client's portfolio returns and positions as the input prompt, we will generate a summary of the portfolio returns and provide the latest market headline news from Reuters. 

GEMINI_API_KEY = userdata.get('GEMINI_API_KEY')
genai.configure(api_key=GEMINI_API_KEY)
model = genai.GenerativeModel('gemini-2.5-flash') # Changed from 'gemini-pro'
response = model.generate_content(prompt)

## **News Summary: Top Headlines from Reuters**
We utilize Google Search's results for Reuters top headlines to retrieve relevant market headlines for the day. For business scale, a direct API call to Reuters might be necessary. 

In this example, we are retrieving the relevant market headlines on 8th Apr 2026, when Trump had just announced a ceasefire with Iran. We are able to generate a list of headlines from the markets which helps clients get up to speed quickly on the latest world news, and be able to read in depth with a click of the button.

![alt text](https://github.com/Amos-THX/Portfolio-News-Summary-using-Gemini/blob/main/Reuters_google_search.png?raw=true)

