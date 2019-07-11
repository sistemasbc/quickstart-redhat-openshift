# Instructions

To deploy this repository and use it, follow these instructions.

1. First, create an S3 Bucket to host this repository and be able to deploy it throgh AWS CloudFormations
1. Make S3 Bucket public and Static WebSite accessible
1. Init and update git submodules
  1. Run following command in this repository roothttps://github.com/sistemasbc/quickstart-redhat-openshift
```
git submodule init
git submodule update
```
1. Upload the contents of this repository to S3 Bucket (in this case, we used _grupobc-quickstarts_ S3 Bucket Name, and _quickstart-redhat-openshift_ folder, to follow the original folder naming)
```
. ~/Seafile/grupobc-it/aws/....
aws s3 sync . s3://grupobc-quickstarts/quickstart-redhat-openshift/
```
1. Follow this link https://console.aws.amazon.com/cloudformation/home?region=eu-west-1#/stacks/new?stackName=Red-Hat-OpenShift&templateURL=https://grupobc-quickstarts.s3.amazonaws.com/quickstart-redhat-openshift/templates/openshift-master.template