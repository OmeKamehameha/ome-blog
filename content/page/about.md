---
title: "About" 
date: "2021-07-24" 
author: "Ghost" 
---

Hello everyone
This is a page made for Kelly to post her pictures in a secure serverless static website. 

-overview

created static files in hugo:
-uploaded them to Github
-used codebuild to run a sync to an s3 bucket (later removed this)
-purchased domain
-created records in Route53
-created Cloudfront distribution
--note: need to ensure used rest api endpoint rather than usding the bucket to serve the files
-used lambda@Edge function to create a redirect for the uri(see:https://dev.to/starpebble/hosting-the-hugo-quickstart-project-on-aws-cloudfront-with-lambda-edge-5g5f)
restrict access, to ensure only able to view via Cloudfront

The plan is to just get the text from her and the images and i will push it to github, lambda will detect, spin up lambda instance of hugo and create static files to serve.