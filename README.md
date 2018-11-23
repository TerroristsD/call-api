Welcome to the AWS CodeStar sample web service
==============================================

This sample code helps get you started with a simple Express web service
deployed by AWS CloudFormation to AWS Lambda and Amazon API Gateway.

What's Here
-----------

This sample includes:

* README.md - this file
* buildspec.yml - this file is used by AWS CodeBuild to package your
  service for deployment to AWS Lambda
* app.js - this file contains the sample Node.js code for the web service
* index.js - this file contains the AWS Lambda handler code
* template.yml - this file contains the AWS Serverless Application Model (AWS SAM) used
  by AWS CloudFormation to deploy your service to AWS Lambda and Amazon API
  Gateway.
* tests/ - this directory contains unit tests for your application


What Do I Do Next?
------------------

If you have checked out a local copy of your repository you can start making
changes to the sample code.  We suggest making a small change to app.js first,
so you can see how changes pushed to your project's repository are automatically
picked up by your project pipeline and deployed to AWS Lambda and Amazon API Gateway.
(You can watch the pipeline progress on your AWS CodeStar project dashboard.)
Once you've seen how that works, start developing your own code, and have fun!

To run your tests locally, go to the root directory of the
sample code and run the `npm test` command, which
AWS CodeBuild also runs through your `buildspec.yml` file.

To test your new code during the release process, modify the existing tests or
add tests to the tests directory. AWS CodeBuild will run the tests during the
build stage of your project pipeline. You can find the test results
in the AWS CodeBuild console.

Learn more about AWS CodeBuild and how it builds and tests your application here:
https://docs.aws.amazon.com/codebuild/latest/userguide/concepts.html

Learn more about AWS Serverless Application Model (AWS SAM) and how it works here:
https://github.com/awslabs/serverless-application-model/blob/master/HOWTO.md

AWS Lambda Developer Guide:
http://docs.aws.amazon.com/lambda/latest/dg/deploying-lambda-apps.html

Learn more about AWS CodeStar by reading the user guide, and post questions and
comments about AWS CodeStar on our forum.

User Guide: http://docs.aws.amazon.com/codestar/latest/userguide/welcome.html

Forum: https://forums.aws.amazon.com/forum.jspa?forumID=248

What Should I Do Before Running My Project in Production?
------------------

AWS recommends you review the security best practices recommended by the framework
author of your selected sample application before running it in production. You
should also regularly review and apply any available patches or associated security
advisories for dependencies used within your application.

Best Practices: https://docs.aws.amazon.com/codestar/latest/userguide/best-practices.html?icmpid=docs_acs_rm_sec



# REST-API

common IDs:
- eventid : nnnnn (unique) - GUID
- nfctagid : nnnnnnnn (for Event) (unique) 
- userid : xxxxx (unique) - GUID generated by smartphone -> + SALT

## Subscribe Event

used IDs: 
- userid
- eventid

POST - Request
{ 
  userid : "12242354"
  eventid : "1231231233"
}

Resopnse
{ statuscode : 200, message: "OK"}

exapmle:
 200 - event subscribed
 400 - BAD REQUEST

## Create Event

used IDs: 
- userid
- eventid

POST - Request
{
  userid : "12242354"
  (optional) nfctagid : "13123123123"
  title : "Mittagessen"
}

Resopnse
{ 
  EventID : "1231231233"
  statusCode : 200, message: "Creted"  }

exapmle:
 200 - event subscribed
 401 - BAD REQUEST



## Call Event

## Edit Event

## List allEvents

## Edit Event

## Create UserID

Resopnse
{ 
  UserID : "12242354"
  statusCode : 200, message: "Created"  }


Post
