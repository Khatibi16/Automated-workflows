# Automated-workflows

This n8n workflow provides a systematic, automated workflow to fetch topics from Google sheets, using Dumpling AI to find the current hot topics and articles, summarize them, and write the post, also with the help of GPT. An image prompt is also generated, and further, Dumpling AI is used to generate an AI image based on the prompt. 
The Google Sheets get updated with the 'status' now being 'created'. Once the article seems right, so does the image; the authorized person may set the 'status' to 'approve'. The loop will run and fetch rows from the Google Sheet every hour will continue going until the status is 'approved'. 
Lastly, the image, which is initially in the URL format, will be converted to the required binary format by the HTTP node, and a LinkedIn post will be made with the article and the image. 

AI agents used: OpenAI's GPT (generally use the 4o-mini version, (OpenAI has strict limits, so it is not possible to make a lot of posts at one time, good pacing between two consecutive posts is recommended). Dumpling AI
