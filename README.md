# dynamodb-export-to-s3-and-query-with-athena-playground

## Files

* [`template.yaml`](template.yaml)
* [`main.sh`](main.sh)

## Running

```sh
sam deploy --guided

# update `STACK_NAME` variable in ./main.sh
# run export table to s3 script
./main.sh
```

`aws dynamodb list-exports # in progress`
```json
{
    "ExportSummaries": [
        {
            "ExportArn": "arn:aws:dynamodb:us-east-1:529276214230:table/dynamodb-export-to-s3-and-query-with-athena-playground-v2-MyTable-1WGSJ3W2WJWPK/export/01605130432834-8a918b87",
            "ExportStatus": "IN_PROGRESS"
        }
    ]
}
```

`aws dynamodb list-exports # completed`
```json
{
    "ExportSummaries": [
        {
            "ExportArn": "arn:aws:dynamodb:us-east-1:529276214230:table/dynamodb-export-to-s3-and-query-with-athena-playground-v2-MyTable-1WGSJ3W2WJWPK/export/01605130432834-8a918b87",
            "ExportStatus": "COMPLETED"
        }
    ]
}
```

## Resources

* [New – Export Amazon DynamoDB Table Data to Your Data Lake in Amazon S3, No Code Writing Required](https://aws.amazon.com/blogs/aws/new-export-amazon-dynamodb-table-data-to-data-lake-amazon-s3/)
* [Now you can export your Amazon DynamoDB table data to your data lake in Amazon S3 to perform analytics at any scale](https://aws.amazon.com/about-aws/whats-new/2020/11/now-you-can-export-your-amazon-dynamodb-table-data-to-your-data-lake-in-amazon-s3-to-perform-analytics-at-any-scale/)
* [Exporting DynamoDB table data to Amazon S3](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DataExport.html)