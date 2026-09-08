# AWS Static Website Hosting with S3


## What this is about
I wanted to actually deploy something on AWS instead of just learning the theory — so I set up a simple static website hosted entirely on S3, from creating the account to getting a live public URL.

## Tools
- Amazon S3 (Static Website Hosting)
- Bucket Policies (IAM-based access control)

## What I did

### 1. Setting up the bucket
Created an S3 bucket and disabled "Block all public access" — since a public website needs to be reachable by anyone.

### 2. Uploading the site
Built a simple HTML page and uploaded it to the bucket as `index.html`.

### 3. Enabling static website hosting
Turned on S3's static website hosting feature and set `index.html` as the index document, which gave me a live website endpoint.

### 4. Configuring public access
Added a bucket policy granting public `s3:GetObject` permission, so visitors could actually load the page without needing AWS credentials.

## Live site
[shahadlfa.s3-website.eu-north-1.amazonaws.com](http://shahadlfa.s3-website.eu-north-1.amazonaws.com)

## What I took away from it
Going from "I understand what S3 is" to "I have a live URL that actually works" made the whole concept click in a way theory never did — especially figuring out why the site wasn't public at first (Block Public Access + missing bucket policy).
