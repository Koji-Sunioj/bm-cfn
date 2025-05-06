# What is this

... a collection of Cloudformation templates, Github action jobs, and Cloud-init instance initalization file, which done in sequence will bootstrap a fullstack application on EC2 with cloudfront as a proxy.

## Cool things

- Nginx is configured to only accept requests from Cloudfront for secure connectivity
- [Atlas](https://atlasgo.io/) is installed so database schema changes in fullstack repo, are applied on EC2 instance
- [Cloud-init](https://cloudinit.readthedocs.io/en/latest/index.html) used in combination with base64 data and github actions to programmatically initialize cloud instance
- Cloudformation templates one for initializing EC2 instance, and another for other AWS services using instance
- Using Github actions to apply infrastructure changes either manually or via push

## Why

I used to use AWS CDK, but since that outputs Cloudformation templates I thought it's better to use Cloudformation. Also the latter is a lot more compact to use, and no need to use npm or node.js. Then combining that with Github actions to learn how they can work together.

In a nutshell: just checking out how to bootstrap a full stack app on AWS with Cloudformation.
