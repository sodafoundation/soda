## Testing multicloud API using Postman
### Aim:
To test SODA Foundation project multicloud (gelato) using rest APIs.

### Howto:
To do this, one can use any API testing clients like cURL or Postman. Here we will show how to test multi-cloud functionalities using [Postman](https://www.postman.com/)

### Prerequisite:
SODA Foundation projects installation:

1.  Install sodafoundation/dashboard ([https://github.com/sodafoundation/dashboard](https://github.com/sodafoundation/dashboard))
    
2.  Install multi-cloud ([https://github.com/sodafoundation/multi-cloud](https://github.com/sodafoundation/multi-cloud))
    

#### You can use the sodafoundation/installer to do the required installation ([https://github.com/sodafoundation/installer](https://github.com/sodafoundation/installer))

  ### Get Started:

Once you have all the installation, We need to get two types of token/key to start using postman.
```
*  Get the multicloud AK/SK
    
*  Get the X-Auth-Token
```
  
 #### * Get the multicloud AK/SK:

1.  Login to the SODA Foundation Dashboard [http://<Your SODA Dashboard Installation Host IP>:8088/#/home](http://192.168.20.163:8088/#/home) using the appropriate credentials
 2.  Go to the “Resource” section and get the AK/SK using “Add AK/SK”
3.  Above step will ask to save the generated file. Get the accessKey and secretKey values from above file. This is the unified access and secret key for multicloud
 

 #### * Get the X-Auth-Token:
From, Postman run the following GET request:
```url
http://<Your SODA multicloud server installation Host IP>/identity/v3/auth/tokens
```
 The request body data is:
```json
{"auth":{
"identity": {
"methods":["password"],
"password":{
"user":{
"name":"admin",
"domain":{"id":"default"},
"password":"<password of identity host/the dashboard host: ex: opensds@123>"
}
}
},
"scope":{
"project":{
"name":"admin",
"domain":{"id":"default"}
}
}
}
}
```

#### Copy the X-Subject-Token from the response Header. Also, get the 'tenant ID' of the admin 

	!!Great!! Now we are ready to test the multi-cloud feature.

### Setup your Postman environment:
Multicloud now is S3 compatible. The multi-cloud APIs requests now support V4 Signature.
In postman, you can use the “AWS Signature” for Authorization.
Here is a snippet:

![](https://lh6.googleusercontent.com/QAswMqla0nvOcSj4J_qfmFSk7kIDh-u7MrTkBpab-Q3YNDMWX3M1jB5qqNlYl28E7HDN8ITat78PjlRd8B9Mcr52DGxT3aKvGHJKTmMfjHyuOF3FBjxtDGUO4HMlAISR-hlU9yeg)


#### Follow these steps:
```
1) Enter the “AccessKey” and “SecretKey” as the one you generated above with SODA Foundation Dashboard.
2) Enter the “AWS Region” of your AWS account
3) Enter “Service Name” as ‘s3’
In the Headers, enter the ‘Key’:’X-Auth-Token’ as the token generated above.
```
![](https://lh6.googleusercontent.com/jhLRAWDI3TiOV1pMBt6NSNBPkj1uYRMafh3ox9SqcXJvK-4NxM1KzmvMB__HbKK7f2A8tKtH7dDDzz8F8vnR_g7G7QtkIUS6Z1YAasjMzkVdHRYU2Zs48svZ0FtpiJDeZOii-CXD)

	!!! Now you are all set!!

### Start using multicloud:

Here are some of the examples:

1.  Register storage backend:
Method: POST
URL: http://<hostIP>/<admin_tenant_ID>/backends
Request body:
```json
{
"name": "<The Name you want to provide", #Ex: ak_awss3
"type": "aws-s3" # This is the type of the Backend.
"region": "<AWS Region Name>",
"endpoint": "s3.amazonaws.com",
"bucketName": "<AWS Cloud Bucket name>",
"access": "<AWS accessKey>",
"security":"<AWS SecretKey>"
}
```
2.  List storage backend:
Method: GET
URl: http://<hostIP>/<admin_tenant_ID>/backends

3.  Create Bucket for the registered backend
Method: POST
URL: http://<Host_IP>:8090/<your_bucket_name>
Request body:
```xml
<CreateBucketConfiguration xmlns="http://s3.amazonaws.com/doc/2006-03-01/">
<LocationConstraint>ak_awss3</LocationConstraint>
</CreateBucketConfiguration>
```
    Response: 200 OK
   4. Upload object into the bucket:
   Method: PUT
   URL: http://<Host_IP>:8090/<your_bucket_name>/<obj_to_be_uploaded>
   * Choose 'Body' as 'Binary'
   * Select the file to be uploaded from 'Select File'


### Refrences
https://github.com/sodafoundation/multi-cloud/blob/master/docs/installation_and_testing.md
