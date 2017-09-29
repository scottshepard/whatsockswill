# whatsockswill

Pushing the website
=======

First install s3cmd:

    brew install s3cmd  

Then put it recursively to the espark-refresh bucket:
  
    cd _site  
    s3cmd put --recursive * s3://whatsocksdoeswillhaveontoday.com/

Use your eSpark Amazon AWS credentials.
