# Create_RBAC_custom-role_using_JSON-temp

--Step 1:Create a JSON file with custom RBAC role:-

{
   "Name": "Support Request Contributor (Custom)",
   "IsCustom": true,
   "Description": "Allows to create support requests",
   "Actions": [
       "Microsoft.Resources/subscriptions/resourceGroups/read",
       "Microsoft.Support/*"
   ],
   "NotActions": [
   ],
   "AssignableScopes": [
       "/providers/Microsoft.Management/managementGroups/az104-02-mg1",
       "/subscriptions/SUBSCRIPTION_ID"
   ]
}

**Note: AssignableScopes **Replace SUBSCRIPTION_ID with subscription id from your Azure Portal**
        Actions **You can also assign permission levels like read, owner, contributor**
      
      
      
--Step 2: **Upload the saved JSON file in Azure Cloud Shell to the right of the search box**


--Step 3: **After uploading the file run command "New-AzRoleDefinition -InputFile $HOME/az104-02a-customRoleDefinition.json"


**Note: Key point **az104-02a-customRoleDefinition.json** should be the file name of your JSON file**


--End Result - Check the assigned custom role under subscription tab **click on Access Control (IAM)** **Roles**


**Note: Allow few minutes for the changes/ refresh browser
