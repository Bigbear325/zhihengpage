+++

# Date this page was created.
date = "2016-04-28"

# Project title.
title = "Traffic Engineering(TE) APP in SDN Controller"

# Project summary to display on homepage.
summary = "Design the SDN based DC Multi-tenancy and develop openation SDN App for VPC and Service Chain Services."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "bubbles.jpg"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["SDNTE"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
image = "headers/bubbles-wide.jpg"
caption = "My caption :smile:"

+++
# Project Background

![backboneNetwork](https://cl.ly/3G151O3k3h3i/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-08-18%203.57.32%20PM.png)



## Motivation
1. The average utilization of the backbone network is less than 50%.
2. Network congestion reported.

## Objective

骨干网内部整体轻载（全网均值利用率小于50%），但存在局部拥塞。骨干网缺少流量调度手段，可以在局部拥塞时调整流量去空闲路径
重要业务承载在CMNet网络上，需提供端到端的稳定带宽质量保障
VPN网络on demand业务的快速开通，可视化监控虚拟网络流量


# Traffic Engineering(TE) APP 
## Architecture 
![enter image description here](https://cl.ly/2T1S1i1v2K37/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-08-18%204.06.20%20PM.png)


![Architecture](https://cl.ly/05073t2P2c2Y/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-08-18%204.33.02%20PM.png)

## Algorithm
1. Predictive algorithm
2. Congestion algorithm
3. Hybrid
4. Traffic prediction algorithm
5. Splitting algorithm


## Field Trail 

![enter image description here](https://cl.ly/252m2C0F1O04/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-08-18%204.39.01%20PM.png)
Design of SDN TE in Fujian Metropolitan Area Network
## Result
![enter image description here](https://cl.ly/100j2A0y2n02/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-08-18%204.39.29%20PM.png)


![enter image description here](https://cl.ly/0Q0b2G1Z2q42/%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202017-08-18%204.39.52%20PM.png)

1. As IGW and IDC, third-party export, Railcom and other interconnection, simulated traffic scheduling IGW1-BR between the link utilization rate of 77%, IGW2-BR link between the utilization rate of 0%
2. Using the Huawei traffic scheduling scheme to analyze the link flow information between IGW1 and BR, the elephant traffic between IGW1 and BR is adjusted to the link between IGW2 and BR
3. After adjustment, the link bandwidth utilization between IGW1-BR and IGW2-BR is evenly distributed, averaging 40% and 37%
