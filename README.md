# Brent's List of Azure AppIDs
Provides a list of App IDs that are known in AAD claims. 

AppIDs are denoted in an AAD claim by the 'appid' attribute of the claim, and represented by a GUID.

AppIDs are represented by their friendly name, and the GUID that represents them.

These can be pulled into an Azure Log Analytics query to do resolution of appID GUIDs to their friendly names.
An example query for this is:
`externaldata (AppDisplayName: string, AppId: string) [h"https://raw.githubusercontent.com/bkolasin/azure-appids/main/appids.csv"] with (ignoreFirstRecord=true, format="csv")`
