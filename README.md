## Intelbras Wi-Force GF1200  Buffer overflow vulnerability exists



### Description of Product

Intelbras is a manufacturer of products and solutions in the fields of security, communications, networking and energy from Brazil. The company operates the manufacture of image management, apartment centers, electronics, switches and telephones

GF1200 routing device ( the latest firmware GF 1200 v1.10.6)  ，It's a WiFi router produced by Intelbras





### Vulnerability information

When the GF1200 router processes information in the HTTP service, the buffer on the device overflows, causing the HTTP service to crash and resulting in a denial of service effect.

1. In the bifrost binary component of the device, there is a risk of buffer overflow for the Authorization parameter obtained in the check_token function.
2. A buffer overflow vulnerability can become a denial of service vulnerability in the router
3. This vulnerability can be triggered without authentication

### Vulnerability details

In the firmware of the device, there is bifrost binary file. Through reverse engineering, it is found that the chen_token function of the binary file has the vulnerability of buffer overflow, and this function is used to handle the authorization value during login.
![image](https://github.com/tigerOrtiger/XXXXXXX1/blob/main/img/image-20210628223241514.png)
