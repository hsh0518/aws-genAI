# aws-genAI

In the SageMaker Studio's top navigation bar, please click on File-->New-->Terminal to open new Terminal window.
Once the terminal is open, copy the following command, replace REPLACE-S3-Bucket-URI with the URI copied in Step 2 and execute the command to download the code.
```

aws s3 cp <REPLACE-S3-Bucket-URI> .  --recursive
```
Run following command to extract the code.
```

tar -xf fsi-llm-demo.tar.gz
```
Confirm that you see folder "FSI-LLM-Demo" as per the screenshot. This folder contains all the necessary code for this workshop.
You have successfully completed the Overview of the Environment.


## RUN STREAMLIT APPLICATION

Overview
Streamlit is an open-source Python library that makes it easy to create and share beautiful, custom web apps for machine learning and data science. In just a few minutes you can build and deploy powerful data apps. So let's get started!

In this lab, you will learn how to run a StreamLit application to visually experience the questions and answers based solution using LLMs on your browser. You will ask natural language based questions to gather information and get hands on experience interacting with Foundation models, Amazon Kendra, Amazon OpenSearch, and LangChain.

Instructions
The steps are outlined below:

Set up configurations: ~5 mins
Install and Run other requirements: ~2 min
Start StreamLit application: ~1 mins
Setup configurations
Go to src folder

Open config.yml file.

Change following sections in config.yml file

Modify kendra: section. Replace index_id value with Kendra Index ID.

You can get this value by navigating to Kendra service page in AWS console.

Copy the Index ID value and replace it in the config file.
Modify data_source value with the correct S3 Bucket Url.
You can get this value by navigating to S3 service page in AWS console.
Copy the S3 bucket URL and replace it in the config file.
Modify aos: section.
Replace aos_host value with the correct OpenSearch Domain EndPoint URL.
You can get this value by navigating to OpenSearch service page in AWS console.
Remove https:// from this URL and replace it in the config file.
Modify llm section.
Replace t5_endpoint and embedding_endpoint values with correct deployment endpoints.
You can navigate to JumpStart screen in SageMaker Studio Console window.
Copy both the endpoint values and replace them in the config file.
Open a new terminal window in SageMaker Studio and navigate to the FSI-LLM-Demo folder.

Pip install requirement.txt
```

pip install -r requirements.txt
```
Next, execute setup.sh
```

sh setup.sh
```

Start StreamLit application
Navigate to StreamLit folder cd streamlit/ and execute run.sh.
```
sh run.sh
```
This should run the Streamlit application.
Copy the the URL highlighted in green color at the end of the output.

Modify the URL and add port number 8501 in the URL. (Note: don't forget to add a forward slash at the end of the URL)
You should see a web page with HTML properties 
