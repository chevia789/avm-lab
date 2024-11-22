<!-- BEGIN_TF_DOCS -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | ~> 1.7 |
| <a name="requirement_azurerm"></a> [azurerm](#requirement\_azurerm) | ~> 3.105 |
| <a name="requirement_http"></a> [http](#requirement\_http) | ~> 3.4 |
| <a name="requirement_random"></a> [random](#requirement\_random) | ~> 3.5 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_azurerm"></a> [azurerm](#provider\_azurerm) | 3.117.0 |
| <a name="provider_http"></a> [http](#provider\_http) | 3.4.5 |
| <a name="provider_random"></a> [random](#provider\_random) | 3.6.3 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_azurerm_user_assigned_identity"></a> [azurerm\_user\_assigned\_identity](#module\_azurerm\_user\_assigned\_identity) | Azure/avm-res-managedidentity-userassignedidentity/azurerm | 0.3.3 |
| <a name="module_bastion"></a> [bastion](#module\_bastion) | Azure/avm-res-network-bastionhost/azurerm | 0.3.0 |
| <a name="module_bastion_public_ip"></a> [bastion\_public\_ip](#module\_bastion\_public\_ip) | Azure/avm-res-network-publicipaddress/azurerm | 0.1.2 |
| <a name="module_key_vault"></a> [key\_vault](#module\_key\_vault) | Azure/avm-res-keyvault-vault/azurerm | 0.9.1 |
| <a name="module_log_analytics_workspace"></a> [log\_analytics\_workspace](#module\_log\_analytics\_workspace) | Azure/avm-res-operationalinsights-workspace/azurerm | 0.3.5 |
| <a name="module_nat_gateway"></a> [nat\_gateway](#module\_nat\_gateway) | Azure/avm-res-network-natgateway/azurerm | 0.2.0 |
| <a name="module_network_security_group"></a> [network\_security\_group](#module\_network\_security\_group) | Azure/avm-res-network-networksecuritygroup/azurerm | 0.2.0 |
| <a name="module_private_dns_zone_key_vault"></a> [private\_dns\_zone\_key\_vault](#module\_private\_dns\_zone\_key\_vault) | Azure/avm-res-network-privatednszone/azurerm | 0.1.2 |
| <a name="module_private_dns_zone_storage_account"></a> [private\_dns\_zone\_storage\_account](#module\_private\_dns\_zone\_storage\_account) | Azure/avm-res-network-privatednszone/azurerm | 0.1.2 |
| <a name="module_storage_account"></a> [storage\_account](#module\_storage\_account) | Azure/avm-res-storage-storageaccount/azurerm | 0.2.5 |
| <a name="module_virtual_machine"></a> [virtual\_machine](#module\_virtual\_machine) | Azure/avm-res-compute-virtualmachine/azurerm | 0.16.0 |
| <a name="module_virtual_network"></a> [virtual\_network](#module\_virtual\_network) | Azure/avm-res-network-virtualnetwork/azurerm | 0.4.0 |

## Resources

| Name | Type |
|------|------|
| [azurerm_resource_group.this](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/resources/resource_group) | resource |
| [random_pet.unique_name](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/pet) | resource |
| [azurerm_client_config.current](https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/data-sources/client_config) | data source |
| [http_http.ip](https://registry.terraform.io/providers/hashicorp/http/latest/docs/data-sources/http) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_address_space_size"></a> [address\_space\_size](#input\_address\_space\_size) | The address space that is used the virtual network | `number` | n/a | yes |
| <a name="input_address_space_start_ip"></a> [address\_space\_start\_ip](#input\_address\_space\_start\_ip) | The address space that is used the virtual network | `string` | n/a | yes |
| <a name="input_location"></a> [location](#input\_location) | The location/region where the resources will be created | `string` | n/a | yes |
| <a name="input_subnets"></a> [subnets](#input\_subnets) | The subnets | <pre>map(object({<br/>    size                       = number<br/>    has_nat_gateway            = bool<br/>    has_network_security_group = bool<br/>  }))</pre> | n/a | yes |
| <a name="input_tags"></a> [tags](#input\_tags) | A map of tags to add to all resources | `map(string)` | n/a | yes |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_names"></a> [names](#output\_names) | n/a |
| <a name="output_subnets"></a> [subnets](#output\_subnets) | n/a |
<!-- END_TF_DOCS -->