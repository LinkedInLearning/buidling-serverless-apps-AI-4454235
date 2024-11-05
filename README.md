# Building Serverless Apps with AI Services on AWS

This is the repository for the LinkedIn Learning course Building Serverless Apps with AI Services on AWS. The full course is available from [LinkedIn Learning][lil-course-url].

![lil-thumbnail-url]

## Course Description

<p>Looking to pair the flexibility and efficiency of serverless architecture with the power of generative AI? In this course, instructor Marcia Villalba shows you how to build serverless applications using AI services on AWS. The course focuses on integrating various services such as Amazon AI Service, Amazon Bedrock, AWS SAM, AWS Step Functions, and EventBridge. Along the way, practice your new skills in real time with hands-on demos and projects, building an application that can transcribe a video, translate its subtitles to another language, and then generate a title and a video description using generative AI.</p><p>Note: This course is designed for AWS developers and architects. Prior experience with AWS is required.</p>

_See the readme file in the main branch for updated instructions and information._

## Instructions

This repository has branches for each of the videos in the course. You can use the branch pop up menu in github to switch to a specific branch and take a look at the course at that stage, or you can add `/tree/BRANCH_NAME` to the URL to go to the branch you want to access.

## Branches

The branches are structured to correspond to the videos in the course. The naming convention is `CHAPTER#_MOVIE#`. As an example, the branch named `02_03` corresponds to the second chapter and the third video in that chapter.
Some branches will have a beginning and an end state. These are marked with the letters `b` for "beginning" and `e` for "end". The `b` branch contains the code as it is at the beginning of the movie. The `e` branch contains the code as it is at the end of the movie. The `main` branch holds the final state of the code when in the course.

When switching from one exercise files branch to the next after making changes to the files, you may get a message like this:

    error: Your local changes to the following files would be overwritten by checkout:        [files]
    Please commit your changes or stash them before you switch branches.
    Aborting

To resolve this issue:
Add changes to git using this command: git add .
Commit changes using this command: git commit -m "some message"

## Installing

1. To use these exercise files, you must have the following installed:
   - [Create an AWS account](https://portal.aws.amazon.com/gp/aws/developer/registration/index.html) if you do not already have one and log in. The IAM user that you use must have sufficient permissions to make necessary AWS service calls and manage AWS resources.
   - [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html) installed and configured
   - [AWS Serverless Application Model](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html) (AWS SAM) installed
   - [Git Installed](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
   - [NodeJS](https://nodejs.org/en) installed
2. Clone this repository into your local machine using the terminal (Mac), CMD (Windows), or a GUI tool like SourceTree.


## Instructor

**Marcia Villalba**
Principal Developer Advocate, Amazon Web Services

[Other courses by the instructor](https://www.linkedin.com/learning/instructors/marcia-villalba)

[GitHub profile](https://github.com/mavi888)


[0]: # 'Replace these placeholder URLs with actual course URLs'
[lil-course-url]: https://www.linkedin.com/learning/building-serverless-apps-with-ai-services-on-aws
[lil-thumbnail-url]: https://media.licdn.com/dms/image/D4D0DAQFP8u36n9BS5g/learning-public-crop_675_1200/0/1715735518041?e=2147483647&v=beta&t=XfiH-ky3x4P7wmR5Ttrqyudv9YuMssq0boo2hlGNqnQ
