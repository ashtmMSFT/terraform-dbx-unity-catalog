Files here were populated with content as described by [Automate Unity Catalog setup using Terraform](https://learn.microsoft.com/en-us/azure/databricks/data-governance/unity-catalog/automate).

Update the resourceId for your Databricks service in *auth.auto.tfvars*.

The tutorial instructions say to specify your workspace id in *metastore.auto.tfvars*. [This link](https://docs.databricks.com/workspace/workspace-details.html) will tell you how to learn your workspaceId. Note: specifying a non-default workspaceId (i.e., not "0") resulted in this error for me: 
```
	 Error: Attribute must be a whole number, got 2.xxxxxxxxxxxxxxxe+15
	│
	│   with databricks_metastore_assignment.default_metastore,
	│   on metastore.tf line 26, in resource "databricks_metastore_assignment" "default_metastore":
	│   26:   workspace_id         = var.default_metastore_workspace_id
```
