# aws-iaas-iam

Basic AWS IAM permissions for IAAS provisioning tool.  The bash script will use AWS CLI to
config AWS for Terraform and Packer.  

## Usage
```bash
sh bootstrap.sh
``` 

### Create a Local env vars file
env.rc file
```env.rc
export AWS_PROFILE=GSA
export AWS_REGION="us-east-1"
export AWS_ACCOUNT_ID=XXXXXXXXXXXX

export STAGE=build
export NAMESPACE="secureOS"

export GITOWNER=rbd80
export GITREPO=terraform-aws-ami-secure

export GITTOKEN=XXXXXXX
export ADMIN_GROUP=iaas_svc
export ADMIN_USERS="terraform_svc packer_svc"

export KEY_NAME=demo_bastion
```

## You need AWS CLI on your host


## AWS Accounts 
Terraform and Packer have their own svc accounts.  The base account need permission to 
be able to create these policies and accounts.  [Packer IAM permissions](https://www.packer.io/docs/builders/amazon.html#using-an-iam-instance-profile)

If policies changes are needed use the bootstrap.sh and select that menu option.  Then 
update the policy json files here.  And rerun the bootstrap and select the first option.

## Help

**Got a question?**

File a GitHub [issue](https://github.com/rbdgsa/aws-iaas-iam/issues), send us an [email](mailto:robert.donovan@gsa.gov).


## Contributing

### Bug Reports & Feature Requests

Please use the [issue tracker](https://github.com/rbd80/terraform-aws-ami-secure/issues) to report any bugs or file feature requests.

### Developing

If you are interested in being a contributor and want to get involved in developing `terraform-aws-ami-secure`, we would love to hear from you! Shoot us an [email](mailto:hello@cloudposse.com).

In general, PRs are welcome. We follow the typical "fork-and-pull" Git workflow.

 1. **Fork** the repo on GitHub
 2. **Clone** the project to your own machine
 3. **Commit** changes to your own branch
 4. **Push** your work back up to your fork
 5. Submit a **Pull request** so that we can review your changes

**NOTE:** Be sure to merge the latest from "upstream" before making a pull request!


## About
