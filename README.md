# Automated-workflows

This n8n workflow provides a systematic, automated workflow to fetch topics from Google sheets, using Dumpling AI to find the current hot topics and articles, summarize them, and write the post, also with the help of GPT. An image prompt is also generated, and further, Dumpling AI is used to generate an AI image based on the prompt. 
The Google Sheets get updated with the 'status' now being 'created' (at first, it fetches the Topics from the row where the status was 'To do'). Once the article seems right, so does the image; the authorized person may set the 'status' to 'approve'. The loop will run and fetch rows from the Google Sheet every hour will continue going until the status is 'approved'. 
Lastly, the image, which is initially in the URL format, will be converted to the required binary format by the HTTP node, and a LinkedIn post will be made with the article and the image. 

AI agents used: OpenAI's GPT (generally use the 4o-mini version). OpenAI has strict limits, so it is not possible to make a lot of posts at one time. Good pacing between two consecutive posts is recommended. 
Dumpling AI: For prolonged use of this workflow, updating to the paid version is recommended. 

Credentials to be created in n8n:
1. Linkedin
2. OpenAI
3. Google Sheets
4. Dumpling AI
