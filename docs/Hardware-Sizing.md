The hardware compute and storage requirements for MOSIP core platform are estimated as below.

## Production
### Compute
Compute hardware estimates for a production deployment:

|Module|Capacity|n Servers|Configuration|
|---|---|---|---|
|Pre-registration | 7200 pre-regs/hour\* | 10 | 4 VCPU\**, 16 GB RAM | 
|Registration Processor | 200,000 registrations per day | 80 | 4 VCPU, 16 GB RAM| 
|ID Authentication | 2,000,000 auth requests per day | 20 | 4 VCPU, 16 GB RAM | 
|Resident Services | 7200 resident services/hour\* | 10 | 4 VCPU, 16 GB RAM | 

\* Average throughput 

\** VCPU:  Virtual CPU


We estimate 30% (approx) additional compute capacitiy for administration, monitoring and maintenance. This may be optimized by the System Integrator.

**Notes**

1. High availability is taken into consideration with assumed replication factor of 2 per service pod/docker
1. The above estimates **do not** include compute servers needed for

   1. Database
   1. HDFS/CEPH
   1. [Bio SDK](Biometric-SDK.md)
   1. [HSM](Hardware-Security-Module-HSM-Specifications.md)
   1. [ABIS](Automated-Biometric-Identification-System-ABIS.md)
   1. Virus scan
   1. Load balancers
   1. External IAM
   1. Disaster recovery 

### Storage
Storage estimates for production deployment:

[MOSIP Storage Requirement Calculator XLS]( https://github.com/mosip/documentation/blob/master/docs/_sources/hardware_sizing/MOSIP_Storage_Estimate-v1.1.xlsx)


## Dev, QA, Staging, Preprod
Additional compute and storage may be needed for the following setups.

| Environment | Setup | n Servers | Configuration | Storage |
|---|---|---|---|---|
| Dev | Sandbox | 13 | 4 VCPU, 16 GB RAM | 128 GB SSD|
| QA | Sandbox | 13 | 4 VCPU, 16 GB RAM | 128 GB SSD|
| Staging | Sandbox | 13 | 4 VCPU, 16 GB RAM | 128 GB SSD|
| Pre-production | Cell | * | 4 VCPU, 16 GB RAM | * |

\* To be decided by the country/System Integrator.
