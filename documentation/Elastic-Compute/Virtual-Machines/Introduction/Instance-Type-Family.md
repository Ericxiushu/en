# Instance Type

An instance is the smallest unit that JD Cloud provides computing services for your business. Different instances identify their corresponding computing, memory, storage, and networking capabilities by their types and specific specifications. Meanwhile, the instance type family you specified when you create an instance determines the hardware configuration of this instance. You can select the appropriate instance type family and specific specification based on the type and size of the application you need to deploy.

The following is the example specification type information of the current JD Cloud. The types and specifications of the saleable instances in different regions are not identical. Please refer to the example creation page. The specific Instance Type specifications can be classified according to different application scenarios:

* General: [General Shared Type](#g.s), [General Standard Type](#g.n)
* Compute-Optimized Standard type: [Compute Optimized Standard Type](#c.n)
* Memory-Optimized type: [Memory Optimized Standard Type](#m.n)
* High-frequency calculation type: [High-frequency calculation optimization type](#h.g)

## Universal type
The universal model currently provides General Shared Type and General Standard types, providing you with balanced computing and memory resources to meet the needs of most business scenarios. Each of the vCPUs in the common standard type corresponds to an Intel Xeon processor hyper-threaded core with a vCPU to memory ratio of 1:4.

### General Shared Type>
**Specification type features:**

* vCPU to memory ratio is 1:1 or 1:2
* Processor: 2.1 GHz Intel Xeon E5-2683 v4 (Broadwell) processor
* Support for the following two types of cloud disk services:
	*Premium Hdd Cloud Disk
	* SSD cloud disk
* Applicable scenario:
	* Primary stage of personal website with small visit flows
	* Microservices
	* Test environment

**Instance Type**

Instance Type|vCPU (core)|Memory (GB)
:---|:---|:---
g.s1.micro|1|	1
g.s1.small|1|2

### General Standard Type>
**Specification type features:**

* vCPU to memory ratio is 1:4 (except for g.n1.xlarge_m specification)
* Processor:
	* Second generation: 2.4 GHz Intel Xeon Gold 6148 (Skylake) processor
	* First generation: 2.1 GHz Intel Xeon E5-2683 v4 (Broadwell) processor
* Support for the following two types of cloud disk services:
	*Premium Hdd Cloud Disk
	* SSD cloud disk
* Applicable scenario:
	* Enterprise applications of all types and sizes
	* Small and medium data systems, caches, search clusters
	* Data analysis and calculation
	* Compute cluster, memory dependent data processing

**Instance Type**

Second generation

Instance Type|vCPU (core)|Memory (GB)|Network Interface Multi-Queue
:---|:---|:---|:---
g.n2.medium|1|4|1
g.n2.large|2|8|2
g.n2.xlarge|4|16|4
g.n2.2xlarge|8|32|4
g.n2.4xlarge|16|64|4
g.n2.8xlarge|32|128|4
g.n2.16xlarge|64|256|4
g.n2.18xlarge|72|288|4

First generation

Instance Type|vCPU (core)|Memory (GB)|Network Interface Multi-Queue|Remarks
:---|:---|:---|:---	|:---
g.n1.medium|1|4|1
g.n1.large|2|8|2
g.n1.xlarge_m	|4|12|4|*|
g.n1.xlarge|4|16|4	
g.n1.2xlarge|8|32|4	
g.n1.4xlarge|16|64|4	
g.n1.8xlarge|32|128|4	

The standard * indicates that the Virtual Machine is not supported by this specification, and you are not allowed to adjust the current Virtual Machine to this specification, but it does not affect the use of your existing Virtual Machine.

## Compute Optimized Type
Compute Optimized Type currently offer Compute-Optimized Standard that provide you with high-performance computing resources that can be met. Each vCPU corresponds to a hyper-threaded core of an Intel Xeon processor.

### Compute-Optimized Standard>
**Specification type features:**

* vCPU to memory ratio is 1:2 (except for c.n1.xlarge_m, c.n1.2xlarge_s, c.n1.2xlarge_m and c.n1.4xlarge_m specifications)
* Processor:
	* Second generation: 2.4 GHz Intel Xeon Gold 6148 (Skylake) processor
	* First generation: 2.1 GHz Intel Xeon E5-2683 v4 (Broadwell) processor
* Support for the following two types of cloud disk services:
	*Premium Hdd Cloud Disk
	* SSD cloud disk
* Applicable scenario:
	* Batch workload
	* Web frontend server
	* Large multiplayer online game (MMO) front end
	* Data analysis, batch calculation, video coding
	* High performance science and engineering applications

**Instance Type**

Second generation

Instance Type|vCPU (core)|Memory (GB)|Network Interface Multi-Queue
:---|:---|:---|:---
c.n2.large|2|4|2
c.n2.xlarge|4|8|4
c.n2.2xlarge|8|16|4
c.n2.4xlarge|16|32|4
c.n2.8xlarge|32|64|4
c.n2.16xlarge|64|128|4
c.n2.18xlarge	|72|144|4

First generation

Instance Type|vCPU (core)|Memory (GB)|Network Interface Multi-Queue|Remarks
:---|:---|:---|:---	|:---
c.n1.large|2|4|2	
c.n1.xlarge_m	|4|4|4|	*
c.n1.xlarge|4|8|	4
c.n1.2xlarge_s|8|8|4|*
c.n1.2xlarge_m|8|12|4|*
c.n1.2xlarge|8|16|4	
c.n1.4xlarge_m|16|16|4|*
c.n1.4xlarge|16|32|4	
c.n1.8xlarge|32|64|4	

The standard * indicates that the Virtual Machine is not supported by this specification, and you are not allowed to adjust the current Virtual Machine to this specification, but it does not affect the use of your existing Virtual Machine.

## Memory Optimized Type
Memory-Optimized Type currently offer a Memory-Optimized Standard Type for applications with large memory operations, lookups, and calculations. Each vCPU corresponds to a hyper-threaded core of an Intel Xeon processor.

### Memory-Optimized Standard>
**Specification type features:**

* vCPU to memory ratio is 1:8 (except for m.n1.medium specification)
* Processor:
	* Second generation: 2.4 GHz Intel Xeon Gold 6148 (Skylake) processor
	* First generation: 2.1 GHz Intel Xeon E5-2683 v4 (Broadwell) processor
* Support for the following two types of cloud disk services:
	*Premium Hdd Cloud Disk
	* SSD cloud disk
* Applicable scenario:
	* High performance database, in-memory database
	* Data analysis and mining, distributed memory caching
	* Hadoop, Spark clusters and other enterprise large memory requirements applications

**Instance Type**

Second generation

Instance Type|vCPU (core)|Memory (GB)|Network Interface Multi-Queue
:---|:---|:---|:---
m.n2.large|2|16|2
m.n2.xlarge|4|32|4
m.n2.2xlarge|8|64|4
m.n2.4xlarge|16|128|4
m.n2.8xlarge|32|256|4
m.n2.16xlarge|64|512|4
m.n2.18xlarge|72|576|4

First generation

Instance Type|vCPU (core)|Memory (GB)|Network Interface Multi-Queue|Remarks
:---|:---|:---|:---	|:---
m.n1.small|1|8|1|*
m.n1.medium|2	|12|2|*
m.n1.large|2|16|2
m.n1.xlarge|4|32	|4
m.n1.2xlarge|8|64|4	
m.n1.4xlarge|16|128|4	

The standard * indicates that the Virtual Machine is not supported by this specification, and you are not allowed to adjust the current Virtual Machine to this specification, but it does not affect the use of your existing Virtual Machine.

## High frequency calculation type

High-frequency computing models currently offer high-frequency computing general-purpose models that provide you with high-performance computing resources. Each vCPU corresponds to a hyper-threaded core of an Intel Xeon processor.

### High-Frequency-Compute General Type>
**Specification type features:**

* vCPU to memory ratio is 1:4
* Computational performance is stable, the processor frequency is high
* Processor:
	* Second generation: 3.2 GHz Intel Xeon Gold 6146 (Skylake) processor
	* First generation: 3.2 GHz Intel Xeon E5-2667 v4 (Broadwell) processor
* Support for the following two types of cloud disk services:
	*Premium Hdd Cloud Disk
	* SSD cloud disk
* Applicable scenario:
	* High-performance web front-end server
	* High performance science and engineering applications
	* MMO games, video coding

**Instance Type**

Second generation:

Instance Type|vCPU (core)|Memory (GB)|Network Interface Multi-Queue
:---|:---|:---|:---
h.g2.large|2|8|2
h.g2.xlarge|4|16|4
h.g2.2xlarge|8|32|4
h.g2.4xlarge|16|64|4
h.g2.8xlarge|32|128|4

First generation:

Instance Type|vCPU (core)|Memory (GB)|Network Interface Multi-Queue
:---|:---|:---|:---
h.g1.large|2|8|2
h.g1.xlarge|4|16|4
h.g1.2xlarge|8|32|4
h.g1.4xlarge|16|64|4
h.g1.6xlarge|24|96|4

Please note:

* The second-generation Virtual Machine (except for high-frequency computing) is temporarily open only in cn-north-1, cn-east-2 and cn-south-1, and the high-frequency computing type is only available in cn-south-1;
* The first generation of general, compute optimized, and memory optimized virtual machines in cn-north-1 and cn-east-2 regions may also run on 2.3 GHz Intel Xeon E5-2698 v3 (Haswell) processor;
* After purchasing an instance, you can modify the configuration of the instance according to the change of business scale. For details, please refer to [Resize](../Operation-Guide/Instance/Resize-Instance.md).

## Related Reference

[Resize]](../Operation-Guide/Instance/Resize-Instance.md)