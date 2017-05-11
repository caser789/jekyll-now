---
layout: post
title: IAM DynamoDB to Kinesis
---
```json
{
  "Statement": [
    {
      "Action": [
        "logs:*"
      ],
      "Effect": "Allow",
      "Resource": [
        "*"
      ],
      "Sid": "Stmt1446202596000"
    },
    {
      "Action": [
        "firehose:DescribeDeliveryStream",
        "firehose:ListDeliveryStreams",
        "firehose:PutRecord",
        "firehose:PutRecordBatch"
      ],
      "Effect": "Allow",
      "Resource": [
        "arn:aws:kinesis:us-east-1:115200798215:stream/ohippo-muid"
      ],
      "Sid": "Stmt1446202630000"
    },
    {
      "Action": [
        "dynamodb:DescribeStream",
        "dynamodb:DescribeTable",
        "dynamodb:GetItem",
        "dynamodb:GetRecords",
        "dynamodb:GetShardIterator",
        "dynamodb:ListStreams",
        "dynamodb:ListTables"
      ],
      "Effect": "Allow",
      "Resource": [
        "arn:aws:kinesis:us-east-1:115200798215:table/ohippo-muid"
      ],
      "Sid": "Stmt1447079825000"
    },
    {
      "Effect": "Allow",
      "Action": [
        "logs:CreateLogGroup",
        "logs:CreateLogStream",
        "logs:PutLogEvents"
      ],
      "Resource": "arn:aws:logs:*:*:*"
    }
  ]
}
```
