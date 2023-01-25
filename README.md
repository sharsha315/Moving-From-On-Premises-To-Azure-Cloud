# Moving From On-Premises To Azure Cloud - Project 1

## Project Summary
In this project, you will help a fictitious company, Contoso, go through a migration from on-premises to Azure cloud.

## Project Statement
Contoso is an online cloth merchandise company specialization in selling activewear. They have rented space in a local data center. They have one system administrator who makes user all servers are working properly 24X7. Their hardware is getting old and they must decide on whether they need to spend $22,000 for new hardware or move their business to the Azure cloud services.

The following list represents their current on-premises infrastructure:

##Server 1
* Purpose: WordPress web server
* CPU: 8 Cores and 60% average utilization
* RAM: 16 GB and 87% average utilization
* HDD OS: 500 GB capacity with 57 GB used
* Web URL: Contoso.com
* IP # Public: 200.200.100.50
* IP #: 10.10.1.11
* Firewall: Inbound TCP 2222-2224, 80, 443
* Usage: This is Contoso's only web server. It runs WordPress and eCommerce services. Their on-line store is always open, and they receive orders 24x7
* This server uses ports 80 and 443 for HTTP and HTTPS traffic

##Servers 2 & 3:
* Purpose: Microsoft SQL 2019
* CPU: 8 Cores and 30% average utilization x2
* RAM: 16 GB and 87% average utilization x2
* HDD OS: 500 GB capacity with 240 GB used x2
* HDD Data: 2 TB SAN (Storage Area Network drive)
* IP #: 10.10.1.12 and 10.10.1.13
* SQL Cluster: SQLCluster.Contoso.Com
* IP #: 10.10.1.14
* Firewall: Inbound TCP 2222-2224, 1433
* Usage: These two servers are running Microsoft SQL cluster services. SQL Always-On service is fully configured as Active-Passive nodes. The 2 servers use an external attached SAN drive for all data storage such as product descriptions, transaction logs, and clients lists. Annual data growth is negligible.
* These servers use the standard SQL inbound TCP port 1433

##Server 4:
* Purpose: ABC Backup and Restore server
* CPU: 8 Cores and 30% average utilization
* RAM: 16 GB and 87% average utilization
* HDD OS: 500 GB capacity with 164 GB used
* HDD Backup: 40 TB
* IP #: 10.10.1.15
* Firewall: Inbound TCP 2222
* Usage: The ABS backup software runs daily at 8pm. It stores the last 18 months of all the SQL data drive contents onto a local D: drive (HDD Backup) with 40 TB capacity.

##Server 5:
* Purpose: XYZ Antivirus server
* CPU: 8 Cores and 30% average utilization
* RAM: 16 GB and 87% average utilization
* HDD: 500 GB capacity with 43 GB used
* IP #: 10.10.1.16
* Firewall: Inbound TCP 2222-2224
* This server uses ports TCP 2222-2224 for the antivirus client
* Usage: The XYZ anti-virus services are essential for the security of Contoso's operations security. The server is always on and constantly running. It monitors all Contoso's servers and mitigates against viruses and hack attacks. Data grown is negligible.

