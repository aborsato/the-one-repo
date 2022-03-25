# Hub and Spoke

This template is a modified version of the original from [this article](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/hybrid-networking/hub-spoke?tabs=bicep).
I added a VPN client certificate to the VPN gateway to configure my Point-to-site at deployment time.
The certificate must be valid (CA generated or SelfSigned) in orther for you VPN to work. Please, refer to [this document](https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-point-to-site-resource-manager-portal) on how to generate/renew your certificate.

## Windows 10/11 VPN
If you have the certificates already installed in your machine, follow these steps to set up your VPN:
1. Use the `Download VPN client` button at `Virtual network gateway` > `Point-to-site configuration`
1. Extract the `.zip` file
1. Use one of the `.exe` installers or refer to the file `Generic/VpnSettings.xml` to install it manually