<h2>Branch out to new workspace notebook</h2>  

This notebook mimics the [branch out to new workspace functionality](https://blog.fabric.microsoft.com/en-us/blog/introducing-new-branching-capabilities-in-fabric-git-integration) in the Fabric UI.

In addition to this:
<ul>
<li>Default lakehouses are updated to the corresponding "local" lakehouse</li>
<li>Creates shortcuts to tables or shortcuts in the source lakehouse </li>
<li>Sets lakehouse connections for semantic models to "local" lakehouse</li> 
<li>Rebinds reports to "local" semantic models</li></ul>

Requirements:
<ul>
<li>Source workspace ("source") needs to be connected to Azure Devops Git repos</li>
<li>Target workspace ("local") will be recreated using the same capacity</li>
<li>Azure Devops PAT token required for creating new branch</li>
<li>Requires Semantic Link Labs installed by pip install below.</li></ul>

Limitations of current script:

<ul>
<li>Recreates items using git. Please see <a href=https://learn.microsoft.com/en-us/fabric/cicd/git-integration/intro-to-git-integration?tabs=azure-devops#supported-items> git supported items </a></li>
<li>Does not recreate workspace roles, direct shares or lakehouse data access roles</li>
<li>Only updates connections of direct lake semantic models which use a lakehouse. Warehouse could be easily supported also using Semantic Link Labs see <a href=https://semantic-link-labs.readthedocs.io/en/stable/sempy_labs.directlake.html#sempy_labs.directlake.update_direct_lake_model_connection/>this link</a>
</li></ul>
