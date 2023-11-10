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
