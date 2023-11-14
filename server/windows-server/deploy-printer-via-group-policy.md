# Deploy Printer via Group Policy

For a domain site it is easier to set up printer as a group policy. The reasoning behind this is because we can make the changes on a host driver, and it would be applied to all client-side driver.



There 3 sections involve in making this a reality. We will go through each process from start to finish.



1. Create AD Security Groups

Our first order of business is to create a Security Groups. This group is used to allow 'Members' of the group to have access to the group policy that is assigned to the Security Groups.

