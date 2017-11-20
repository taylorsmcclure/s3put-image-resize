# Serverless Image Resizing to Thumbnails

## How to Use

1) Follow [AWS tutorial](http://docs.aws.amazon.com/lambda/latest/dg/with-s3-example.html) for basics.
2) Create S3 bucket with `images/` and `thumbs/` directories.
3) Enable Public list access to bucket.
4) Create IAM Policy and Role for lambda to access bucket with `list*`, `putObject`, and `putObjectAcl`
5) In repo use `make dist`
6) Upload `dist/function.zip` to lambda and associate role with policy
7) Add trigger in S3 for `putObject` to execute lambda
