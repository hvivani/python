# Signing Requests with Signature Version 4

This script is based on this documentation:
http://docs.aws.amazon.com/general/latest/gr/sigv4_signing.html

To sign a URL with Signature Version 4:

1) Export your key and secret-key:
```
   export AWS_ACCESS_KEY=your-aws-access-key-id
   
   export AWS_SECRET_KEY=your-aws-secret-key
```   
   
2) Execute the script passing the endpoint and the region, as example:
```
   python sign-req-url-v4.py my-endpoint-test.es.amazonaws.com eu-west-1
   
```   




