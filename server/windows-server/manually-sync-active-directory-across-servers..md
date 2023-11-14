# Manually sync active directory across servers.

### Intro

I have stumbled upon a minor problem where some of my Group Policy created doesn't sync across servers as fast as I need it to be during troubleshooting process. This KB will provide you with a step by step guide on how to manually sync your Active Directory across servers.



### Steps

Open Command prompt and simply type the following code:

```
repadmin /syncall /AeD
```

This command will sync ITSELF to its domain controller partners.



But what does each command do? The following data explains what each code does:



This is the key string that calls the sync process.

```
repadmin /syncall
```

Below are the commands that can be used during the sync process.

```
A = All Partitions
e = Enterprise (Cross Site)
D = Identify servers by distinguished name in messages.
```



but what if you want to sync your active directory FROM the server that you have it configured on?

```
P = Push
```



So if you were to push changes FROM source, it will look like this instead:

```
repadmin /syncall /APeD
```

### Outro

Now you have learned how to manually sync domain controller config across site, here is a neat command line that might be useful to you:

```
gpresult /R
```

What does it do? I'm gonna let you figure that one out.



{% embed url="http://technet.microsoft.com/en-us/library/cc736571(v=ws.10).aspx" %}

