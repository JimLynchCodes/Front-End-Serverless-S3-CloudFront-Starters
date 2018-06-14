# Front-End-Serverless-S3-CloudFront-Starters
Some starter projects for various front-ends frameworks meant to be serverlessly hosted on AWS S3 and CloudFront.

## The S3 Deploy Script
To me, it's very interesting that the deploy script is pretty independent of whatever front-end framework you want to use (aside from the naming conventions each framework uses for the final build output folder). This makes it really nice from a dev ops point of view because:

- Devs can use any framework they like (as long as it outputs static files).
- We don't need to manage webservers to host the front-end.
- We can you basically the same deploy script for any front-end project.

Pretty hot, eh? Anyway, here's the gist of how you would deploy your dist/ directory to an S3 bucket.

```
aws s3 cp ./dist s3://BUCKETNAME --recursive --acl public-read
```


## Thanks

Thanks to Abvraham Szilagyi for writing this [post](https://medium.com/codefactory/angular2-s3-love-deploy-to-cloud-in-6-steps-3f312647a659) whichi inspired the deploy scripts in this project. Thanks!
