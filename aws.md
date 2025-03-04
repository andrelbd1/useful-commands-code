### [AWS](https://aws.amazon.com/pt/cli) commands

#### General
- Login
````bash
    aws sso login
````
````bash
    aws sso login --profile <my profile> 
````
````bash
    aws sso login --profile 086874483813_sdz-data-eng-set
````

- List users
````bash
    aws iam list-users
````

#### EC2
- Connect to EC2 instance 
````bash
    # ssh -i <key_file_name>.pem <User>@<EC2 instance IP>
    ssh -i "andre_brandao_key.pem" ubuntu@10.11.152.158
````

#### S3
- List buckets
````bash
    aws s3 ls
````
````bash
    aws s3 ls --profile <my profile>
````

- List objects from a Bucket
````bash
    aws s3 ls s3://<bucket-name>
````
````bash
    aws s3 ls s3://<bucket-name> --profile gaivota-dev
````
````bash
    aws s3 ls s3://<bucket-name>/ --recursive --human-readable --summarize --profile avm_prod
````

- Count objects from a bucket
````bash
    aws s3 ls s3://<bucket-name> --recursive | wc -l
````
````bash
    aws s3 ls s3://sdz-log-receipts-prd/logs/year=2024/month=12/day=27/ --recursive | wc -l
````

- Copy all objects from a bucket to another one
````bash
    aws s3 sync s3://<bucket-origin-name>/<path> s3://<bucket-target-name>/<path>
````
````bash
    aws s3 sync s3://sdz-log-receipts-prd/logs/year=2024/month=12/day=27/ s3://sdz-log-receipts-dev/logs/year=2024/month=12/day=27/
````

- Remove all objects from a folder in a Bucket
````bash
    aws s3 rm s3://<bucket-name>/<folder>/ --recursive
````
````bash
    aws s3 rm s3://sdz-log-receipts-dev/logs/year=2024/month=12/day=27/ --recursive
````

#### SQS
- Count messages from a queuesudo apt-get install jq 
````bash
    aws sqs get-queue-attributes --queue-url <queue-url> --attribute-names All
````
````bash
    aws sqs get-queue-attributes --queue-url https://sqs.us-east-1.amazonaws.com/086874483813/sdz-platform-logs-to-lake-generate-index-dev --attribute-names All
````

- Get a message from a queue
````bash
    aws sqs receive-message --queue-url <queue-url>
````
````bash
    aws sqs receive-message --queue-url https://sqs.us-east-1.amazonaws.com/086874483813/sdz-platform-logs-to-lake-generate-index-dev
````

- Remove a message from a queue
````bash
    aws sqs delete-message --queue-url <queue-url> --receipt-handle <receipt-handle>
````
````bash
    aws sqs delete-message --queue-url https://sqs.us-east-1.amazonaws.com/086874483813/sdz-platform-logs-to-lake-generate-index-dev --receipt-handle AQEBFTFF4...
````

- Remove all messages from a queue
````bash
    aws sqs purge-queue --queue-url <your-queue-url>
````
````bash
    aws sqs purge-queue --queue-url https://sqs.us-east-1.amazonaws.com/086874483813/sdz-platform-logs-to-lake-generate-index-dev
````

#### ECR - Elastic Container Registry
- Login to ECR
````bash
    aws ecr get-login-password --region <REGION> | docker login --username AWS --password-stdin <ECR URL>
    aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 151019420220.dkr.ecr.us-east-1.amazonaws.com
````

