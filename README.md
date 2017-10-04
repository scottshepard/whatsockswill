# whatsockswill

Pushing the website
=======

First install s3cmd:

    brew install s3cmd  

Configure s3cmd

    s3cmd --configure

Create an IAM user on AWS and download the credentials, add them when prompted

Now push the repo recursively to the appropriate AWS bucket:
  
    cd _site  
    s3cmd put --recursive * s3://whatsocksdoeswillhaveontoday.com/

Or use the executable

    bin/deploy
