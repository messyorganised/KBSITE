# Set up VLAN

## Creating your VLAN

Click on Interface > Assignments > VLAN

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Click on Add&#x20;

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Select your primary LAN as your parent interface&#x20;

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

Enter your VLAN Tag. In this instance our VLAN tag will be "45"&#x20;

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

OPTIONAL: Enter your VLAN Description for easier identification.&#x20;

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

Click on Save

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

## Creating the Interface for your VLAN

Click on Interface Assignments&#x20;

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

Hit the drop down menu and select the newly made VLAN (VLAN 45)

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

Click on Add

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

Click on OPT4&#x20;

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

Update your Description name to reflect it on the Interface Assignment tab.&#x20;

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>



Set IPV4 Con6guration Type to 'Static IPv4'

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

Enter your desired address for the VLAN gateway. This section in particular is to allow access to your PFSense router while you are in the VLAN. Set your subnet to 24&#x20;

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

Check Enable interface&#x20;

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

Click on Save&#x20;

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

Click on Apply Changes&#x20;

<figure><img src="../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>



## Setting up DHCP Server for newly created Interface

Depending on your requirements. You will need to set up a DHCP Server on your newly created VLAN. This will assign any networking devices with DHCP setting turned on to acquire IP address provided by the router.&#x20;



Click on Services&#x20;

<figure><img src="../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

Click on DHCP Server&#x20;



<figure><img src="../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>



Click on TESTVLAN&#x20;

<figure><img src="../../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>



Set your DHCP VLAN range. First entry will skip all addresses PRIOR to the entry and second entry will skip all addresses AFTER the entry during the DHCP process.&#x20;

<figure><img src="../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

Check Enable DHCP server on TESTVLAN interface&#x20;

&#x20;

<figure><img src="../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

Click on Save

<figure><img src="../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

## Set up rule for internet access 8 Steps

If your VLAN does not required internet access. No further work is needed. However, my VLAN was set up so my Virtual Machines can access the internet. To make this happen, we will need to add a Firewall rule that allows all traffic from our VLAN to the internet&#x20;

Click on firewall > rules&#x20;

<figure><img src="../../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

Select your newly created VLAN (TESTVLAN)

<figure><img src="../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

Click on Add&#x20;

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>



Set your Action to PASS&#x20;

Interface is the new Interface that you ha7e created&#x20;

Address Family to IPV4&#x20;

Source: TESTVLAN net&#x20;

Destination: any&#x20;

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>



Enter your rule description&#x20;

<figure><img src="../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

Click on Save&#x20;

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

Click on Apply Changes&#x20;

<figure><img src="../../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

You should be able to access the web once everything is configured&#x20;

<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>
