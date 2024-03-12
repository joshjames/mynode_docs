# Deploy on AWS Cloud

## Download And upload to s3

1. Download the OVA file from [mynodebtc.com](http://mynodebtc.com/download) (3.2GB)
2. Upload to a bucket on s3 

## Import OVA to AWS

1. Rename the uploaded s3 file to mnode.ova
2. create a IAM user with the appropriate permissions
3. permissions needed are here: link to aws import

**Note**: you will need the AWS CLI setup with admin api access to run the commands on the above page.

## Import the ova to ami

1. run the import command
2. check the progress.
2. once the ami is completed it will appear as AMIID in AMI in the ec2 console.

## Launch the AMI as ec2

1. select the new AMI deploy ec2 from this ami.
2. select the region and ec2 settings
3. when deployed it will appear under ec2.
4. find the public ip - add security rule for ssh access and for web (http and https) access - **note** best to set source to your ip only so nobody else can get to the web console at least untill you have updated the default password.

## log in to the console

1. go to the public ip address after updating security in a browser
2. Enter username as **admin** and password as **bolt**
4. Enter the password again in the Chromium window
5. the console should want to format the seconday drive for the blockchain
6. let it finish and update.
7. keep an eye on storage use you can ssh to the box and check server status using df etc

# Alternativly deploy an already created AMI

1. the ami ami-000b34ad804b7becb is public has already been converted and ready to launch jumping straight to the lanch step above.
