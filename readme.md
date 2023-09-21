# DigitalOcean Droplet Script - October 2023 Update

## Change Summary

- **2023:** Updated the way to retrieve the IP address from `item.data.ip_address` to `item.data.droplet.networks.v4.0.ip_address` for compatibility with the latest DigitalOcean API changes, which can be found [here](https://docs.digitalocean.com/reference/api/)

## Description

This repository contains an updated script for managing DigitalOcean Droplets as of October 2023. It includes a critical modification to adapt to changes in the DigitalOcean API, specifically the retrieval of the Droplet's IP address. In 2022, the API used ```item.data.ip_address``` to obtain the IP address, but due to changes in the API structure, the correct method is now ```item.data.droplet.networks.v4.0.ip_address```. This adjustment is essential for seamless operation with the latest DigitalOcean infrastructure.

## Usage

To retrieve the IP address of a Droplet, you should use the following code snippet in your scripts:

```python
droplet_ip = droplet_result.results[0].data.droplet.networks.v4.0.ip_address
```
Feel free to clone or fork this repository to ensure your DigitalOcean Droplet management scripts remain up-to-date and compatible with the latest API changes.

Contributions:
Contributions are welcome! If you encounter any issues or have suggestions for improvements, please open an issue or submit a pull request.

License:
