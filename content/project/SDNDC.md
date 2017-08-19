+++

# Date this page was created.
date = "2016-04-28"

# Project title.
title = "SDN Multi-tenancy and Serveice Chain"

# Project summary to display on homepage.
summary = "Design the SDN based DC Multi-tenancy and develop openation SDN App for VPC and Service Chain Services."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "sdndc.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["SDNDC"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
image = "headers/bubbles-wide.jpg"


+++


# Project Background

![background](https://cl.ly/373y3O2F3Q3L/Image%202017-08-18%20at%2012.21.47%20PM.png)


## Motivation(Before)
1. Users select the network, computing, storage of resources through the different page. To complete and bad user experience.
2. Current CMCC DC pool can only allocate for less than 4K enterprise users. Besides, users can not customize their network.
3. Network Function Virtualization(NFV) capacity is limited, can not provide users with value-added network services.


## Objective(After)

1. Users can define their network resources, configuration, management, maintenance of private network through the graphical web interface.
2. Within a single resource pool, the network can support maximum 10K users, the tenant can allocate unlimited subnets within its VPC.
3. Virtual application of LB / NAT / VPN / VR / FW , to provide user-defined service chain function, flexible definition of rental network.

# VPC+ Service Chain APP
## Architecture 
![System Architecture](https://cl.ly/3o0y0g393i1u/Image%202017-08-18%20at%203.20.18%20PM.png)
1. Develop CMCC SDN VPC APP
Tenants can custom cloud network, and firewall, load balancing service chain via the WEB interface(self-service portal). 
2. Based on OpenStack
Based on OpenStack to collaborate with the virtual platform (VMware and KVM).
3. Controller
Support OpenStack NBI and SDN APP API. Support OpenFlow/XMPP/netconf/ovsdb protocol.
4. Forwarding Devices
Support VM and legacy device management.


## SDN DC Topology
![SDN DC Topology](https://cl.ly/1N0x3u1x2l1r/Image%202017-08-18%20at%203.24.03%20PM.png)

1. Network Topology:
Using Spine & Leaf architecture, including underlay + overlay and pure overlay.
2. SDN:
physical switches and vsw oriented SDN controller(CMCC developed)
3. Graphic and services chain APP: Our works
4. Performance support:  1000 openflows / s +  40 users concurrent configuration.
5. Configuration free: After the vsw starts, the controller is automatically connected. All subsequent configurations are controlled by the controller

## System Demo

![Self Service Portal](https://cl.ly/1q0C2B012g0r/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-08-18%203.25.51%20PM.png)
User self service portal UI.

![online deployment](https://cl.ly/1b2O2o2a0g47/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-08-18%203.27.28%20PM.png)

User online network deployment.

![online configuration](https://cl.ly/1r3J0f0E433x/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-08-18%203.27.59%20PM.png)

User online network configuration.

## Application
1. China Mobile Jiangxi DC
2. China Mobile Fujian Private Cloud Datacenter

