# What's all this?

Amazon S3 provides a great place to store all sorts of files but sometimes managing permissions can be a bit of a pain. Built-in to S3 is the ability to generate links to private files that expire after a set period of time. This tool generates those for you so you don't have to fiddle with the command line or install any 3rd party tools.

## Won't you steal my key?

Your secret key is safe, all code runs client side. The code is also available in case you don't trust me.

## Who are you?

I'm Phil. I sometimes write things at blog.50projects.com

## Deployment

Specific instructions for this installation. Adjust targets and settings
for your specific installation.

`aws s3 sync ./ s3://s3-expiry.50projects.com/ --exclude ".git/*" --acl public-read --delete`
