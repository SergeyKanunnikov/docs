---
editable: false
---
# Pricing policy for [!KEYREF mpg-name]

## What goes into the cost of using [!KEYREF mpg-short-name] {#rules}

The cost of [!KEYREF mpg-name] usage is based on:

* Storage (disk space) type and size.

* [The DB class](concepts/instance-types.md) selected for the cluster.

* How many DB hosts are in the clusters.

* Settings and number of backups.

* The amount of outgoing traffic.

[!INCLUDE [pricing-gb-size](../_includes/pricing-gb-size.md)]

### Use of DB hosts {#rules-hosts-uptime}

The cost is calculated for each hour of the host's operation in accordance with its class. The exact class characteristics are given in the section [[!TITLE]](concepts/instance-types.md).

The minimum billing unit is one hour (for example, the cost of 1.5 hours of operation is the same as the cost of 2 hours of operation). You are not charged for time when the host [!KEYREF PG] is not performing its main functions.

### Disk space use {#rules-storage}

The following is charged:

* Storage allocated for DB clusters.
    * Storage on fast local disks (NVMe) can only be ordered for clusters with more than 3 hosts, in 100 GB increments.

* Space used by DB backups in excess of the storage specified for the cluster.

    * Backups are stored free of charge as long as the combined size of the DB and all backups is less than the selected storage volume.

    * During an automatic backup, [!KEYREF mpg-short-name] does not create a new copy but saves changes in the DB as compared to the previous copy. This means that storage used by automatic backups increases only in proportion to the volume of changes that are made.

    * The number of hosts in the cluster does not affect the size of the storage and, consequently, that of free backups.

The cost is specified for one month of use.  The minimum billing unit is 1 GB per hour (for example, the cost of storing 1 GB for 1.5 hours is equal to the cost of storage for 2 hours).

## Prices {#prices}

### Hosts {prices-hosts}

Host class | Cost of 1 hour, without VAT | Cost of 1 hour, with VAT
----- | ----- | ----- 
s1.nano | ₽2.1610 | ₽2.5932 |
s1.micro | ₽4.3136 | ₽5.1763 |
s1.small | ₽8.6186 | ₽10.3424 |
s1.medium | ₽17.2458 | ₽20.6949 |
s1.large | ₽34.4831 | ₽41.3797 |
s1.xlarge | ₽68.9746 | ₽82.7695 ₽

### Storage and backups {#prices-storage}

Service | Cost of 1 GB per month, without VAT | Cost of 1 GB per month, with VAT
 ----- | ----- | ----- 
The standard NAS | ₽1.9068 | ₽2.2881 |
Fast network storage | ₽6.7797 | ₽8.1356 |
Fast local storage | ₽6.7797 | ₽8.1356 |
Backup over storage size | ₽2.1186 | ₽2.5424 ₽

### Outgoing traffic {#prices-traffic}

[!INCLUDE-NOTITLE [pricing-egress-traffic](../_includes/pricing/pricing-egress-traffic.md)]

