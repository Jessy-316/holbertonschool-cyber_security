
# Holberton School Domain Report

### Overview

This report details the findings from investigating the `holbertonschool.com` domain using Shodan. It includes information on the IP ranges associated with the domain and the technologies/frameworks used within all subdomains.

---

## 1. IP Ranges Within HolbertonSchool.com Domain

Shodan provides data about internet-facing devices and their respective IP addresses. To gather information about all the IP ranges associated with the `holbertonschool.com` domain, the following IP addresses were identified:

| **IP Address**        | **Location**                   | **Region**            | **Organization**          |
|-----------------------|--------------------------------|-----------------------|---------------------------|
| 51.44.50.40           | Amazon Data Services France    | Paris, France         | Amazon                   |
| 13.39.186.120         | Amazon Data Services France    | Paris, France         | Amazon                   |
| 35.181.245.154        | Amazon Data Services France    | Paris, France         | Amazon                   |
| 15.236.138.29         | Amazon Data Services France    | Paris, France         | Amazon                   |
| 35.180.157.150        | Amazon Data Services France    | Paris, France         | Amazon                   |
| 13.37.138.187         | Amazon Data Services France    | Paris, France         | Amazon                   |
| 51.44.46.142          | Amazon Data Services France    | Paris, France         | Amazon                   |
| 13.39.75.248          | Amazon Data Services France    | Paris, France         | Amazon                   |
| 15.188.252.57         | Amazon Data Services France    | Paris, France         | Amazon                   |
| 52.47.143.83          | Amazon Data Services France    | Paris, France         | Amazon                   |

---

## 2. Technologies and Frameworks Used Within All Subdomains of HolbertonSchool.com

By analyzing the services associated with various subdomains of `holbertonschool.com`, the following technologies and frameworks were identified:

### 2.1. **Main Web Server**
- **Web Server**: `nginx/1.20.0`
  - A common web server used for handling HTTP requests.
  
### 2.2. **SSL/TLS Information**
- **SSL Certificate Issuer**: Amazon RSA 2048 M03, Let's Encrypt
- **Supported SSL Versions**: TLSv1.2, TLSv1.3 (depending on subdomain)
- These certificates help secure communications with encryption.

### 2.3. **Subdomains and their Associated Technologies**
- **Subdomains**: 
  - `read.holbertonschool.com`
  - `apply.holbertonschool.com`
  - `staging-apply.holbertonschool.com`
  - `yriry2.holbertonschool.com`
  
For each subdomain, the following technologies and frameworks were identified:

#### 2.3.1. **Subdomain: read.holbertonschool.com**
- **SSL Provider**: Amazon RSA 2048 M03
- **Web Server**: `nginx`
- **Security Headers**: 
  - `X-Frame-Options: SAMEORIGIN`
  - `X-XSS-Protection: 1; mode=block`
  - `X-Content-Type-Options: nosniff`
  - `X-Download-Options: noop`
  
#### 2.3.2. **Subdomain: apply.holbertonschool.com**
- **SSL Provider**: Amazon RSA 2048 M03
- **Web Server**: `nginx`
- **Security Headers**: 
  - `X-Frame-Options: SAMEORIGIN`
  - `X-XSS-Protection: 1; mode=block`
  - `X-Content-Type-Options: nosniff`
  - `X-Download-Options: noopen`
  
#### 2.3.3. **Subdomain: staging-apply.holbertonschool.com**
- **SSL Provider**: Amazon RSA 2048 M03 (or Let's Encrypt in some cases)
- **Web Server**: `nginx`
- **Security Headers**: 
  - `X-Frame-Options: SAMEORIGIN`
  - `X-XSS-Protection: 1; mode=block`
  - `X-Content-Type-Options: nosniff`
  - `X-Download-Options: noop`

#### 2.3.4. **Subdomain: yriry2.holbertonschool.com**
- **SSL Provider**: Let's Encrypt
- **Web Server**: `nginx`
- **Security Headers**: 
  - `X-Frame-Options: SAMEORIGIN`
  - `X-XSS-Protection: 0`
  - `X-Content-Type-Options: nosniff`
  - `X-Download-Options: noopen`
---