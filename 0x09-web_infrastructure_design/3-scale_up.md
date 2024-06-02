# Scaled Up Web Infrastructure


## Description

This web infrastructure is a scaled up version of the infrastructure described [here](2-secured_and_monitored_web_infrastructure.md). It removes all single points of failure by separating the major components (web, app, database) onto individual servers. SSL termination is now handled at the load balancer level, ensuring end-to-end encryption. Each server's network is also protected by its own firewall, and all servers are monitored.

## Specifics About This Infrastructure

+ **Firewalls between each server**  
The addition of firewalls between the individual servers provides more granular network segmentation and protection, rather than relying on a single firewall for the entire infrastructure.

## Issues With This Infrastructure

+ **Higher Maintenance Costs**  
Deploying each component on a dedicated server increases the overall hardware and operational costs, as more servers need to be purchased, powered, and maintained compared to the previous 3-server setup.