# terraform-aws-route53-cluster-hostname

Terraform module to define a consistent AWS Route53 hostname


## Makefile Targets
```
Available targets:

  help                                Help screen
  help/all                            Display help for all targets
  help/short                          This help short screen
  lint                                Lint terraform code

```
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| enabled | Set to false to prevent the module from creating any resources | bool | `true` | no |
| name | The Name of the application or solution  (e.g. `bastion` or `portal`) | string | - | yes |
| records | DNS records to create | list(string) | - | yes |
| ttl | The TTL of the record to add to the DNS zone to complete certificate validation | string | `300` | no |
| type | Type of DNS records to create | string | `CNAME` | no |
| zone_id | Route53 DNS Zone ID | string | - | yes |

## Outputs

| Name | Description |
|------|-------------|
| hostname | DNS hostname |




## Share the Love 

Like this project? Please give it a ★ on [our GitHub](https://github.com/cloudposse/terraform-aws-route53-cluster-hostname)! (it helps us **a lot**) 

Are you using this project or any of our other projects? Consider [leaving a testimonial][testimonial]. =)


## Related Projects

Check out these related projects.

- [terraform-aws-route53-alias](https://github.com/cloudposse/terraform-aws-route53-alias) - Terraform module to define vanity host/domain (e.g. `brand.com`) as an ALIAS record
- [terraform-aws-route53-cluster-zone](https://github.com/cloudposse/terraform-aws-route53-cluster-zone) - Terraform module to provision cluster domain (e.g. `prod.ourcompany.com`)
- [terraform-aws-kops-route53](https://github.com/cloudposse/terraform-aws-kops-route53) - Terraform module to lookup the IAM role associated with `kops` masters, and attach an IAM policy to the role with permissions to modify Route53 record sets
