# S3 bucket

- from AWS console search for `s3` then choose `create bucket`

  ![create bucket](../../screenshots/S3-bucket/S3-bucket1.png)

- choose a unique name for your bucket

  ![name your bucket](../../screenshots/S3-bucket/S3-bucket2.png)

- make sure to uncheck block public access

  ![public access](../../screenshots/S3-bucket/S3-bucket3.png)

- in the `Default encryption` choose `disable` then create the bucket

  ![create access](../../screenshots/S3-bucket/S3-bucket4.png)

- bucket created successfully

  ![bucket created](../../screenshots/S3-bucket/S3-bucket5.png)

- set bucket policy by choosing `permissions` after choosing your bucket

  ![bucket permission](../../screenshots/S3-bucket/S3-bucket6.png)

- then click `Edit` and add

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": [
                "s3:GetObject"
            ],
            "Resource": [
                "arn:aws:s3:::mmasoud-udagram/*"
            ]
        }
    ]
}
```

    ![bucket policy](../../screenshots/S3-bucket/S3-bucket7.png)

- Configure static website hosting: scroll to `Static website hosting` and click edit

  ![edit static website hosting](../../screenshots/S3-bucket/S3-bucket8.png)

- AWS provide us with the Endpoint

  ![bucket endpoint](../../screenshots/S3-bucket/S3-bucket9.png)

- now we need to upload our files: first let's create a user
  search for `IAM` then from `users groups` click on `create group` give the group a name and attach `AdminstratorAcess` to it

  ![create group](../../screenshots/S3-bucket/S3-bucket10.png)

- then click on `users` and click `Add users`

  ![add users](../../screenshots/S3-bucket/S3-bucket11.png)

- give your user a name and check `Access Key Programtic Access`

  ![user name](../../screenshots/S3-bucket/S3-bucket12.png)

- select your group to attach the user to it then click create user
  ![create user](../../screenshots/S3-bucket/S3-bucket13.png)

- user created successfully
  ![user created](../../screenshots/S3-bucket/S3-bucket14.png)

- from the terminal add `aws configure` and add the `AWS ACCESS KEY ID` and `AWS SECRET ACCESS KEY` we have from the last step

- navigate to my project and run this command to upload my files `aws s3 cp --recursive --acl public-read ./www s3://mmasoud-udagram` and now my files uploaded successfully

![content uploaded](../../screenshots/S3-bucket/S3-bucket15.png)

frontend endpoint http://mmasoud-udagram.s3-website-us-east-1.amazonaws.com/
