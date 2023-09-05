# terraform-module-template

<!-- TODO fill in resource name in link to product documentation -->
Terraform module for [Resource name](https://example.com).

## Example

<!-- todo update module name
```hcl
module "todo_resource_name" {
  source = "git@github.com:hmcts/terraform-module-postgresql-flexible?ref=master"
  ...
}

```

<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_azurerm"></a> [azurerm](#requirement\_azurerm) | >= 3.7.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_azurerm"></a> [azurerm](#provider\_azurerm) | >= 3.7.0 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_ctags"></a> [ctags](#module\_ctags) | github.com/hmcts/terraform-module-common-tags | n/a |

## Resources

| Name | Type |
|------|------|
| [azurerm_bastion_host.bastion_host](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/bastion_host) | resource |
| [azurerm_public_ip.p_ip_bastion](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/public_ip) | resource |
| [azurerm_subnet.azure_bastion_subnet](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/subnet) | resource |
| [azurerm_subscription.current](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/subscription) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_allocation_method"></a> [allocation\_method](#input\_allocation\_method) | Specify Static or Dynamic | `string` | n/a | yes |
| <a name="input_azbastion_subnet_address"></a> [azbastion\_subnet\_address](#input\_azbastion\_subnet\_address) | Virtual network subnet address that contains the azure bastion host | `any` | n/a | yes |
| <a name="input_bastion_name"></a> [bastion\_name](#input\_bastion\_name) | Name of the bastion host | `string` | n/a | yes |
| <a name="input_bastion_sku"></a> [bastion\_sku](#input\_bastion\_sku) | Specify SKU for the bastion host | `string` | n/a | yes |
| <a name="input_builtFrom"></a> [builtFrom](#input\_builtFrom) | Built from value. | `string` | n/a | yes |
| <a name="input_env"></a> [env](#input\_env) | Environment value. | `string` | n/a | yes |
| <a name="input_ip_config_name"></a> [ip\_config\_name](#input\_ip\_config\_name) | IP config name | `string` | n/a | yes |
| <a name="input_location"></a> [location](#input\_location) | Target Azure location to deploy the resource | `string` | `"UK South"` | no |
| <a name="input_product"></a> [product](#input\_product) | https://hmcts.github.io/glossary/#product | `string` | n/a | yes |
| <a name="input_public_ip_name"></a> [public\_ip\_name](#input\_public\_ip\_name) | Public IP of the Bastion | `string` | n/a | yes |
| <a name="input_public_ip_sku"></a> [public\_ip\_sku](#input\_public\_ip\_sku) | Enter the SKU for the Public IP of the Bastion | `string` | n/a | yes |
| <a name="input_resource_group_name"></a> [resource\_group\_name](#input\_resource\_group\_name) | Resource group name that contains the azure bastion host | `string` | n/a | yes |
| <a name="input_tunneling_enabled"></a> [tunneling\_enabled](#input\_tunneling\_enabled) | Select True or False, tunneling is only supported when sku is Standard | `bool` | n/a | yes |
| <a name="input_virtual_network_name"></a> [virtual\_network\_name](#input\_virtual\_network\_name) | Virtual network name that contains the bastion host | `string` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_resource_group_location"></a> [resource\_group\_location](#output\_resource\_group\_location) | n/a |
| <a name="output_resource_group_name"></a> [resource\_group\_name](#output\_resource\_group\_name) | n/a |
<!-- END_TF_DOCS -->

## Contributing

We use pre-commit hooks for validating the terraform format and maintaining the documentation automatically.
Install it with:

```shell
$ brew install pre-commit terraform-docs
$ pre-commit install
```

If you add a new hook make sure to run it against all files:
```shell
$ pre-commit run --all-files
```
