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

Here is an example generating a signed request for Amazon Elasticsearch Service endpoint:
```
[ec2-user@ip-172-31-12-131 python]$ python sign-req-url-v4.py search-hvivani-test-674xdhdclxwxwxwxwxw5yokdi.eu-west-1.es.amazonaws.com eu-west-1

BEGIN REQUEST++++++++++++++++++++++++++++++++++++
Request URL = https://search-hvivani-test-674xdhdcltycwxwxwxwxwdi.eu-west-1.es.amazonaws.com?Action=CreateUser&UserName=NewUser&Version=2010-05-08&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJYOUR-KEYO3%2F20151009%2Feu-west-1%2Fes%2Faws4_request&X-Amz-Date=20151009T042326Z&X-Amz-Expires=30&X-Amz-SignedHeaders=host&X-Amz-Signature=5bb87c8e3dawxwxwxwxwxwxe74679c091717d0f5096

RESPONSE++++++++++++++++++++++++++++++++++++
Response code: 200

{
  "status" : 200,
  "name" : "Radius",
  "cluster_name" : "32A22387:hvivani-test",
  "version" : {
    "number" : "1.5.2",
    "build_hash" : "62ff9xwxwxwxwxwx8ab1c",
    "build_timestamp" : "2015-04-27T09:21:06Z",
    "build_snapshot" : false,
    "lucene_version" : "4.10.4"
  },
  "tagline" : "You Know, for Search"
}
```

