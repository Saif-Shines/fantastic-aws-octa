# AWS for Frontend Engineers

- [00 - Introduction](content/00%20-%20Introduction.md)
- [01 - The AWS Free Tier](content/01%20-%20The%20AWS%20Free%20Tier.md)
- [02 - Account Set Up](content/02%20-%20Account%20Set%20Up.md)
- [03 - Billing](content/03%20-%20Billing.md)
- [04 - IAM](content/04%20-%20IAM.md)
- [05 - S3](content/05%20-%20S3.md)
- [06 - Registering a Domain Name](content/06%20-%20Registering%20a%20Domain%20Name.md)
- [07 - S3 Policies](content/07%20-%20S3%20Policies.md)
- [08 - AWS CLI](content/08%20-%20AWS%20CLI.md)
- [09 - Route 53](content/09%20-%20Route%2053.md)
- [10 - Routing](content/10%20-%20Routing.md)
- [11 - CloudFront](content/11%20-%20CloudFront.md)
- [12 - Using OAI](content/12%20-%20Using%20OAI.md)
- [13 - Creating a Custom Cache Policy](content/13%20-%20Creating%20a%20Custom%20Cache%20Policy.md)
- [14 - Build Pipeline](content/14%20-%20Build%20Pipeline.md)
- [15 - Lambda@Edge](content/15%20-%20Lambda@Edge.md)

```js
{
        "Version": "2008-10-17",
        "Id": "PolicyForCloudFrontPrivateContent",
        "Statement": [
            {
                "Sid": "AllowCloudFrontServicePrincipal",
                "Effect": "Allow",
                "Principal": {
                    "Service": "cloudfront.amazonaws.com"
                },
                "Action": "s3:GetObject",
                "Resource": "arn:aws:s3:::shines1729/*",
                "Condition": {
                    "StringEquals": {
                      "AWS:SourceArn": "arn:aws:cloudfront::570517961192:distribution/E32470YMCYIPIQ"
                    }
                }
            }
        ]
      }

      {
	"Version": "2012-10-17",
	"Id": "Policy1685943124698",
	"Statement": [
		{
			"Sid": "Stmt1685943121765",
			"Effect": "Allow",
			"Principal": {
				"AWS": "arn:aws:iam::cloudfront:user/CloudFront Origin Access Identity EP6AJZA5FKG3P"
			},
			"Action": "s3:GetObject",
			"Resource": "arn:aws:s3:::shines1729/*"
		}
	]
}

{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR_BUCKET_NAME_HERE/*"
    }
  ]
}
```
