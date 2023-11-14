# Automate Edge Browser settings

In continuation to my pursuit in fully automating new PC installs for non managed customers, I have finally moved onto automating Edge Browser configurations.



Unfortunately there are limitations of the script when running it on workgroup PCs due to the nature of the edge policy feature only supporting workstations that are managed by Active Directory.&#x20;



Microsoft KB Page for all Edge Policies lists and its features.

{% embed url="https://learn.microsoft.com/en-us/deployedge/microsoft-edge-policies" %}

ADMX Page for all Edge Policies lists and its feature - More forgiving to the eyes.

{% embed url="https://admx.help/?Category=EdgeChromium&Policy=Microsoft.Policies.Edge::DefaultSearchProviderSearchURL" %}



