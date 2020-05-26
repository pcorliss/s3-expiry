# What's all this?

Amazon S3 provides a great place to store all sorts of files but sometimes managing permissions can be a bit of a pain. Built-in to S3 is the ability to generate links to private files that expire after a set period of time. This tool generates those for you so you don't have to fiddle with the command line or install any 3rd party tools.

## How do I use it?

Visit http://s3-expiry.50projects.com/

## Won't you steal my key?

Your secret key is safe, all code runs client side. The code is also available in case you don't trust me.

## I still don't trust you, how would I do this on the command line?

AWS provides the [presign](https://docs.aws.amazon.com/cli/latest/reference/s3/presign.html) command.

`aws s3 presign expiry-test/hello.txt --expires-in 86400 --region us-east-1`

Make sure to set your credentials either via `aws configure` or via the `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY` environment variables.

## Who are you?

I'm Phil. I sometimes write things at blog.50projects.com

## Deployment

Specific instructions for this installation. Adjust targets and settings
for your specific installation.

`aws s3 sync ./ s3://s3-expiry.50projects.com/ --exclude ".git/*" --acl public-read --delete`
