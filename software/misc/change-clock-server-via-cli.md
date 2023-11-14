# Change clock server via CLI



```
w32tm /config /syncfromflags:MANUAL /manualpeerlist: [Enter time server]
w32tm /config /update
```
