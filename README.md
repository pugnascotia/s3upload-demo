# S3 Direct Upload Demo using Spring

This is a demonstration of how to perform direct uploads to AWS's S3
service from a browser. It's mostly based upon the blog post "[Direct
Browser Uploading – Amazon S3, CORS, FileAPI, XHR2 and Signed
PUTs](http://www.ioncannon.net/programming/1539/direct-browser-uploading-amazon-s3-cors-fileapi-xhr2-and-signed-puts/)",
with some Java inspiration from the
[EvaporateJS](https://github.com/TTLabs/EvaporateJS/blob/master/example/SigningExample.java)
repo.

# Provisioning

There is a [Terraform]() configuration under `src/main/terraform`. You can
build the necessary infrastructure to run this project as follows.


1. Set the following environment variables:
  * `TF_VAR_AWS_SECRET_KEY`
  * `TF_VAR_AWS_ACCESS_KEY`

2. Configure the remaining AWS variables in
   `src/main/terraform/variables.tf`.

3. Run the following to check all is well:

    `terraform plan`

4. Apply the config:

    `terraform apply`

# Running the project

1. Edit `src/main/resources/application.properties` to set the appropriate
   values.

2. Run maven with `mvn`.

3. Navigate to [http://localhost:8080/](http://localhost:8080/).
