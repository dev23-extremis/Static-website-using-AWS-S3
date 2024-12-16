# Static-website-using-AWS-S3
Deploying Static Website using AWS S3

### Set Up Static Website Hosting on AWS S3

1. **Create S3 Bucket:**
   - Go to AWS S3 and click "Create bucket."
   - Enter a unique name (e.g., `devbuck123`) and region and then click "Create."

2. **Enable Public Access:**
   - Click the "Permissions" tab.
   - Click "Block all public access" and save.
- Attach this bucket policy (replace `devbuck123` with your bucket name):
     ```json
     {
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "devbuck123",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": [
                "arn:aws:s3:::devbuck123/*",
                "arn:aws:s3:::devbuck123"
              ]
          }
        ]
  }


3. **Enable Static Website Hosting:**
   - Go to "Properties" and enable "Static website hosting."
- Set `index.html` as index document, optionally set `error.html`.
  Save changes.

4. **Upload Files:**
  Upload website files e.g. `index.html`, `style.css`
  Make them public

5. **Make Objects Public:**
  Select all files and go to "Actions" > "Make Public."

6. **Test Website:**
  Copy the URL from "Static website hosting" and open it in a browser.

**Note** :  For more detailed process check out the .txt file name "Steps to deploy static website using aws S3" in the files  
