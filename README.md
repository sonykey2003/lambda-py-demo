# Deploy A Serverless Python App on AWS

## 1. Create Lambda function

* AWS Console → Lambda → Create function

* Runtime: Python 3.14

* Use this code
```py
import json
HTML = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <title>BISP Python Workshop</title>
</head>
<body>
    <h1>Welcome to the IT page!</h1>
    <p>Welcome to BISP Python Workshop</p>
    <p>Hello World!</p>
    <p>你好!</p>
    <p>こんにちは!</p>
    <p>สวัสดี!</p>
</body>
</html>
"""


def lambda_handler(event, context):
    # TODO implement
    return {
        'statusCode': 200,
          "headers": {
            "Content-Type": "text/html; charset=utf-8"
        },
        'body': HTML
    }


```


## 2. Create public URL

* Lambda → Configuration → Function URL

* Create → Auth = NONE

* Copy the URL

## 3. Try it
Open the URL in a browser.
