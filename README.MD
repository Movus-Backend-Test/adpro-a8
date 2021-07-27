# ADPRO A-8

<!-- PROJECT LOGO -->
<br />
<p align="center">
  <h3 align="center">ADPRO A-8 Service</h3>

  <p align="center">
    Serverless Service for Movus Static File Upload
    <br />
    <br />
    <p align="center">Live Site</p>
    <p align="center">https://dikdjt4qzl.execute-api.ap-southeast-1.amazonaws.com/prod/upload?name={image_name}&type={image_type}</p>
  </p>
</p>

### How to use
1. Send Get Request to https://dikdjt4qzl.execute-api.ap-southeast-1.amazonaws.com/prod/upload?name={image_name}&type={image_type} with your file and desired filename
2. make sure input get 200 http response, example response below

```json
    {
    "putUrl": "https://adpro-a8-staticfile.s3.ap-southeast-1.amazonaws.com/images/acil?AWSAccessKeyId={Secret}&Content-Type=image%2Fpng&Expires=1627372464&Signature={Secret}",
    "getUrl": "https://adpro-a8-staticfile.s3.ap-southeast-1.amazonaws.com/images/acil"
}
```

3. Upload image to given putUrl
4. save getUrl to database for next fetch
5. to get image that already uploaded, fetch from getUrl

### Built With

-   [ExpressJS](https://expressjs.com/)
-   [AWS Lambda](https://aws.amazon.com/id/lambda/)
-   [AWS S3](https://aws.amazon.com/id/s3/)