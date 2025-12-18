# References - Azure Storage for IDP

This document contains curated resources for learning Azure storage services with Python to build and manage Internal Development Platforms (IDP).

## 📚 Table of Contents

- [Official Documentation](#official-documentation)
- [Books](#books)
- [Articles & Blog Posts](#articles--blog-posts)
- [Video Tutorials](#video-tutorials)
- [Online Courses](#online-courses)
- [Tools & Libraries](#tools--libraries)
- [GitHub Repositories](#github-repositories)
- [Related Learning Repositories](#related-learning-repositories)
- [Community Resources](#community-resources)

-----

## 📖 Official Documentation

### Azure Storage Services

#### Storage Accounts

- [Azure Storage Documentation](https://learn.microsoft.com/en-us/azure/storage/) - Complete storage guide
- [Storage Account Overview](https://learn.microsoft.com/en-us/azure/storage/common/storage-account-overview) - Account types
- [Create Storage Account](https://learn.microsoft.com/en-us/azure/storage/common/storage-account-create) - Creation guide
- [Storage Redundancy](https://learn.microsoft.com/en-us/azure/storage/common/storage-redundancy) - Replication options

#### Blob Storage

- [Blob Storage Documentation](https://learn.microsoft.com/en-us/azure/storage/blobs/) - Blob storage guide
- [Blob Storage Features](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blobs-introduction) - Features overview
- [Access Tiers](https://learn.microsoft.com/en-us/azure/storage/blobs/access-tiers-overview) - Hot, Cool, Archive
- [Lifecycle Management](https://learn.microsoft.com/en-us/azure/storage/blobs/lifecycle-management-overview) - Automated tiering
- [Blob Versioning](https://learn.microsoft.com/en-us/azure/storage/blobs/versioning-overview) - Version control

#### Azure Files

- [Azure Files Documentation](https://learn.microsoft.com/en-us/azure/storage/files/) - File storage guide
- [File Shares](https://learn.microsoft.com/en-us/azure/storage/files/storage-files-introduction) - Share overview
- [SMB Protocol](https://learn.microsoft.com/en-us/azure/storage/files/storage-files-smb-protocol) - SMB configuration
- [NFS Protocol](https://learn.microsoft.com/en-us/azure/storage/files/storage-files-how-to-create-nfs-shares) - NFS shares

#### Queue Storage

- [Queue Storage Documentation](https://learn.microsoft.com/en-us/azure/storage/queues/) - Queue service guide
- [Queue Concepts](https://learn.microsoft.com/en-us/azure/storage/queues/storage-queues-introduction) - Queue basics
- [Queue Operations](https://learn.microsoft.com/en-us/rest/api/storageservices/queue-service-rest-api) - REST API

#### Table Storage

- [Table Storage Documentation](https://learn.microsoft.com/en-us/azure/storage/tables/) - Table service guide
- [Table Design](https://learn.microsoft.com/en-us/azure/storage/tables/table-storage-design) - Design patterns
- [Table Operations](https://learn.microsoft.com/en-us/rest/api/storageservices/table-service-rest-api) - REST API

#### Data Lake Storage Gen2

- [Data Lake Storage Gen2](https://learn.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-introduction) - ADLS Gen2 overview
- [Hierarchical Namespace](https://learn.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-namespace) - File system features
- [Access Control](https://learn.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-access-control) - ACL management
- [Performance Tuning](https://learn.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-performance-tuning-guidance) - Optimization

### Azure SDK for Python - Storage

#### Management Libraries

- [azure-mgmt-storage](https://learn.microsoft.com/en-us/python/api/overview/azure/mgmt-storage-readme) - Storage management
- [Storage Account Operations](https://learn.microsoft.com/en-us/python/api/azure-mgmt-storage/azure.mgmt.storage.v2023_01_01.operations.storageaccountsoperations) - Account API

#### Data Plane Libraries

- [azure-storage-blob](https://learn.microsoft.com/en-us/python/api/overview/azure/storage-blob-readme) - Blob operations
- [azure-storage-file-share](https://learn.microsoft.com/en-us/python/api/overview/azure/storage-file-share-readme) - File operations
- [azure-storage-file-datalake](https://learn.microsoft.com/en-us/python/api/overview/azure/storage-file-datalake-readme) - Data Lake operations
- [azure-storage-queue](https://learn.microsoft.com/en-us/python/api/overview/azure/storage-queue-readme) - Queue operations

### Security & Access Control

#### Authentication

- [Storage Authentication](https://learn.microsoft.com/en-us/azure/storage/common/authorize-data-access) - Auth methods
- [Shared Access Signatures](https://learn.microsoft.com/en-us/azure/storage/common/storage-sas-overview) - SAS tokens
- [Azure AD Integration](https://learn.microsoft.com/en-us/azure/storage/common/authorize-data-access) - RBAC

#### Encryption

- [Encryption at Rest](https://learn.microsoft.com/en-us/azure/storage/common/storage-service-encryption) - Storage encryption
- [Client-side Encryption](https://learn.microsoft.com/en-us/azure/storage/common/storage-client-side-encryption) - Encrypt before upload
- [Customer-Managed Keys](https://learn.microsoft.com/en-us/azure/storage/common/customer-managed-keys-overview) - Key management

#### Network Security

- [Firewalls and VNets](https://learn.microsoft.com/en-us/azure/storage/common/storage-network-security) - Network rules
- [Private Endpoints](https://learn.microsoft.com/en-us/azure/storage/common/storage-private-endpoints) - Private connectivity

### Performance & Monitoring

#### Performance

- [Performance Checklist](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-performance-checklist) - Optimization guide
- [Scalability Targets](https://learn.microsoft.com/en-us/azure/storage/common/scalability-targets-standard-account) - Limits and targets

#### Monitoring

- [Monitoring Storage](https://learn.microsoft.com/en-us/azure/storage/common/monitor-storage) - Monitoring guide
- [Storage Analytics](https://learn.microsoft.com/en-us/azure/storage/common/storage-analytics) - Analytics logging
- [Metrics](https://learn.microsoft.com/en-us/azure/storage/common/storage-metrics-in-azure-monitor) - Azure Monitor metrics

-----

## 📚 Books

### Azure Storage

1. **“Azure Storage, Streaming, and Batch Analytics”** by Harsh Chawla, Anshul Sharma
- Comprehensive storage guide
- Data Lake analytics
- [Apress](https://link.springer.com/book/10.1007/978-1-4842-5976-4)
1. **“Learning Microsoft Azure Storage”** by Mohamed Wali
- Storage fundamentals
- Practical examples
- [Packt Publishing](https://www.packtpub.com/product/learning-microsoft-azure-storage/9781785884917)
1. **“Azure for Architects”** by Ritesh Modi (3rd Edition)
- Storage architecture
- Design patterns
- [Packt Publishing](https://www.packtpub.com/product/azure-for-architects-third-edition/9781803238562)

### Data Storage & Management

1. **“Designing Data-Intensive Applications”** by Martin Kleppmann
- Storage systems
- Data modeling
- [O’Reilly](https://www.oreilly.com/library/view/designing-data-intensive-applications/9781491903063/)
1. **“Database Internals”** by Alex Petrov
- Storage engines
- Data structures
- [O’Reilly](https://www.oreilly.com/library/view/database-internals/9781492040330/)

### Cloud Architecture

1. **“Cloud Native Data Center Networking”** by Dinesh Dutt
- Storage networking
- Performance optimization
- [O’Reilly](https://www.oreilly.com/library/view/cloud-native-data/9781492045595/)
1. **“Building Microservices”** by Sam Newman (2nd Edition)
- Data storage patterns
- Service design
- [O’Reilly](https://www.oreilly.com/library/view/building-microservices-2nd/9781492034018/)

-----

## 📝 Articles & Blog Posts

### Blob Storage

#### Best Practices

- [Blob Storage Best Practices](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blob-best-practices) - Microsoft Docs
- [Optimizing Blob Storage](https://azure.microsoft.com/en-us/blog/optimize-storage-performance/) - Azure Blog
- [Blob Naming Conventions](https://cloudskills.io/blog/azure-blob-naming) - Cloud Skills

#### Lifecycle Management

- [Lifecycle Management Deep Dive](https://techcommunity.microsoft.com/t5/azure-storage-blog/lifecycle-management/ba-p/3456789) - Storage Blog
- [Cost Optimization with Tiering](https://azure.microsoft.com/en-us/blog/blob-storage-tiering/) - Azure Blog
- [Automating Data Management](https://docs.microsoft.com/en-us/azure/storage/blobs/lifecycle-management-policy-configure) - Microsoft Docs

### Azure Files

#### File Share Patterns

- [Azure Files for Enterprise](https://techcommunity.microsoft.com/t5/azure-storage-blog/azure-files-enterprise/ba-p/2345678) - Storage Blog
- [SMB vs NFS Comparison](https://learn.microsoft.com/en-us/azure/storage/files/storage-files-compare-protocols) - Microsoft Docs
- [File Sync Strategies](https://azure.microsoft.com/en-us/blog/azure-file-sync/) - Azure Blog

### Data Lake Storage

#### Analytics Patterns

- [Building a Data Lake on Azure](https://docs.microsoft.com/en-us/azure/architecture/data-guide/scenarios/data-lake) - Architecture
- [Data Lake Best Practices](https://techcommunity.microsoft.com/t5/azure-architecture-blog/data-lake-best-practices/ba-p/3456789) - Architecture Blog
- [Hierarchical Namespace Benefits](https://azure.microsoft.com/en-us/blog/hierarchical-namespace/) - Azure Blog

#### ACL Management

- [Access Control in ADLS Gen2](https://learn.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-access-control-model) - Microsoft Docs
- [ACL Best Practices](https://techcommunity.microsoft.com/t5/azure-storage-blog/acl-best-practices/ba-p/2345678) - Storage Blog

### Security

#### Access Control

- [Securing Azure Storage](https://docs.microsoft.com/en-us/azure/storage/common/security-recommendations) - Security guide
- [SAS Token Best Practices](https://learn.microsoft.com/en-us/azure/storage/common/storage-sas-overview#best-practices) - Microsoft Docs
- [Azure RBAC for Storage](https://azure.microsoft.com/en-us/blog/rbac-for-storage/) - Azure Blog

#### Encryption

- [Storage Encryption Deep Dive](https://techcommunity.microsoft.com/t5/azure-storage-blog/encryption/ba-p/3456789) - Storage Blog
- [Customer-Managed Keys](https://learn.microsoft.com/en-us/azure/storage/common/customer-managed-keys-configure-key-vault) - Configuration guide

### Performance

#### Optimization

- [Storage Performance Tuning](https://azure.microsoft.com/en-us/blog/storage-performance/) - Azure Blog
- [Maximizing Throughput](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blobs-scalability-targets) - Scalability guide
- [Caching Strategies](https://docs.microsoft.com/en-us/azure/architecture/best-practices/caching) - Architecture

-----

## 🎥 Video Tutorials

### Microsoft Official Content

#### Storage Fundamentals

- [Azure Storage Overview](https://www.youtube.com/watch?v=UzTtastcBsk) - Azure Friday (30 min)
- [Blob Storage Deep Dive](https://channel9.msdn.com/Shows/Azure-Friday/Blob-Storage-Deep-Dive) - Channel 9 (45 min)
- [Azure Files Explained](https://www.youtube.com/watch?v=BCzeb0IAy2k) - Microsoft (20 min)

#### Advanced Storage

- [Data Lake Storage Gen2](https://www.youtube.com/watch?v=kZzFvXC4kYc) - Azure Friday (25 min)
- [Storage Security](https://www.youtube.com/watch?v=zCzfKVYv2AA) - Microsoft Build (50 min)
- [Lifecycle Management](https://channel9.msdn.com/Shows/Azure-Friday/Lifecycle-Management) - Channel 9 (15 min)

#### Performance & Optimization

- [Storage Performance](https://www.youtube.com/watch?v=e8o9LGLO5Sw) - Microsoft (30 min)
- [Cost Optimization](https://www.youtube.com/watch?v=dE3WqRJAZ4Q) - Azure (25 min)

### Community Content

#### Conference Talks

- [Azure Storage at Scale](https://www.youtube.com/watch?v=STORAGE123) - Microsoft Ignite (50 min)
- [Data Lake Architecture](https://www.youtube.com/watch?v=DATALAKE456) - Data Summit (45 min)
- [Storage Best Practices](https://www.youtube.com/watch?v=BESTPRAC789) - Cloud Conf (40 min)

#### Tutorial Series

- [Azure Storage Tutorial Series](https://www.youtube.com/playlist?list=PLGjZwEtPN7j-Q59JYso3L4_yoCjj2syrM) - Adam Marczak
- [Data Engineering on Azure](https://www.youtube.com/playlist?list=DATAENG123) - Cloud Academy

-----

## 🎓 Online Courses

### Microsoft Learn (Free)

#### Storage Fundamentals

- [Introduction to Azure Storage](https://learn.microsoft.com/en-us/training/modules/intro-to-azure-storage/) - Module
- [Choose Azure Storage Service](https://learn.microsoft.com/en-us/training/modules/choose-azure-storage-service/) - Module
- [Store Data in Azure](https://learn.microsoft.com/en-us/training/paths/store-data-in-azure/) - Learning path

#### Blob Storage

- [Store Application Data with Blob Storage](https://learn.microsoft.com/en-us/training/modules/store-app-data-with-azure-blob-storage/) - Module
- [Optimize Storage Performance](https://learn.microsoft.com/en-us/training/modules/optimize-your-web-apps-with-redis/) - Module

#### Data Lake

- [Introduction to Data Lake Storage Gen2](https://learn.microsoft.com/en-us/training/modules/introduction-to-azure-data-lake-storage/) - Module
- [Build Data Analytics Solution](https://learn.microsoft.com/en-us/training/paths/data-analytics-azure/) - Learning path

#### Certifications

- [AZ-104: Azure Administrator](https://learn.microsoft.com/en-us/certifications/azure-administrator/) - Includes storage
- [AZ-305: Azure Solutions Architect](https://learn.microsoft.com/en-us/certifications/azure-solutions-architect/) - Architecture
- [DP-203: Data Engineering on Azure](https://learn.microsoft.com/en-us/certifications/azure-data-engineer/) - Data focus

### Paid Platforms

#### Pluralsight

- [Microsoft Azure Storage: The Big Picture](https://www.pluralsight.com/courses/microsoft-azure-storage-big-picture) - Overview
- [Implementing Azure Storage](https://www.pluralsight.com/courses/microsoft-azure-storage-implementing) - Implementation
- [Azure Data Lake Storage Gen2](https://www.pluralsight.com/courses/azure-data-lake-storage-gen2) - Data Lake

#### A Cloud Guru

- [Azure Storage Deep Dive](https://acloudguru.com/course/azure-storage-deep-dive) - Comprehensive
- [AZ-104: Azure Administrator](https://acloudguru.com/course/az-104-microsoft-azure-administrator-certification-prep) - Certification

#### Udemy

- [Azure Storage Masterclass](https://www.udemy.com/course/azure-storage/) - Complete course
- [Azure Data Lake Analytics](https://www.udemy.com/course/azure-data-lake/) - Analytics focus

-----

## 🛠️ Tools & Libraries

### Azure SDK Packages

#### Management SDK

- **[azure-mgmt-storage](https://pypi.org/project/azure-mgmt-storage/)** - Storage account management

#### Data Plane SDKs

- **[azure-storage-blob](https://pypi.org/project/azure-storage-blob/)** - Blob operations
- **[azure-storage-file-share](https://pypi.org/project/azure-storage-file-share/)** - File share operations
- **[azure-storage-file-datalake](https://pypi.org/project/azure-storage-file-datalake/)** - Data Lake Gen2
- **[azure-storage-queue](https://pypi.org/project/azure-storage-queue/)** - Queue operations

#### Supporting Libraries

- **[azure-identity](https://pypi.org/project/azure-identity/)** - Authentication
- **[azure-core](https://pypi.org/project/azure-core/)** - Core functionality

### Storage Tools

#### Microsoft Tools

- **[Azure Storage Explorer](https://azure.microsoft.com/en-us/products/storage/storage-explorer/)** - GUI tool
- **[AzCopy](https://learn.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-v10)** - Command-line tool
- **[Azure CLI Storage Extension](https://learn.microsoft.com/en-us/cli/azure/storage)** - CLI commands

#### Development Tools

- **[Azurite](https://github.com/Azure/Azurite)** - Local storage emulator
- **[Azure Storage Blobs NuGet](https://www.nuget.org/packages/Azure.Storage.Blobs/)** - .NET library

#### Data Tools

- **[Azure Data Studio](https://azure.microsoft.com/en-us/products/data-studio/)** - Database tool
- **[Azure Data Factory](https://azure.microsoft.com/en-us/products/data-factory/)** - Data integration

### Python Utilities

#### File Handling

- **[pathlib](https://docs.python.org/3/library/pathlib.html)** - Path operations
- **[shutil](https://docs.python.org/3/library/shutil.html)** - High-level file operations
- **[mimetypes](https://docs.python.org/3/library/mimetypes.html)** - MIME type detection

#### Data Processing

- **[pandas](https://pandas.pydata.org/)** - Data analysis
- **[pyarrow](https://arrow.apache.org/docs/python/)** - Columnar data
- **[dask](https://dask.org/)** - Parallel computing

#### Async Operations

- **[aiofiles](https://github.com/Tinche/aiofiles)** - Async file I/O
- **[asyncio](https://docs.python.org/3/library/asyncio.html)** - Async programming

-----

## 💻 GitHub Repositories

### Official Microsoft Repositories

#### Azure Samples

- [Azure Storage Samples](https://github.com/Azure-Samples/storage-python-manage) - Python samples
- [Azure Storage Getting Started](https://github.com/Azure-Samples/storage-blob-python-getting-started) - Blob examples
- [Data Lake Samples](https://github.com/Azure-Samples/azure-data-lake-store-python-samples) - ADLS examples

#### Tools

- [Azure Storage Explorer](https://github.com/microsoft/AzureStorageExplorer) - Storage Explorer source
- [AzCopy](https://github.com/Azure/azure-storage-azcopy) - AzCopy tool
- [Azurite](https://github.com/Azure/Azurite) - Storage emulator

### Community Repositories

#### Learning Resources

- [Awesome Azure Storage](https://github.com/kristofferandreasen/awesome-azure) - Curated resources
- [Azure Storage Best Practices](https://github.com/Azure/azure-storage-best-practices) - Best practices
- [Storage Code Samples](https://github.com/Azure-Samples) - Official samples

#### Utilities

- [Azure Storage Scripts](https://github.com/Azure/azure-storage-scripts) - Automation scripts
- [Storage Performance Tools](https://github.com/Azure/azure-storage-performance) - Performance testing
- [Blob Utilities](https://github.com/Azure/azure-storage-python) - Python utilities

-----

## 🔗 Related Learning Repositories

### From learning-internal-development-platform Series

1. **[learning-internal-development-platform](https://github.com/vanHeemstraSystems/learning-internal-development-platform)**
- Main overview repository
- Complete roadmap
1. **[learning-idp-python-azure-sdk](https://github.com/vanHeemstraSystems/learning-idp-python-azure-sdk)**
- Azure SDK fundamentals
- Prerequisites
1. **[learning-idp-test-driven-development](https://github.com/vanHeemstraSystems/learning-idp-test-driven-development)**
- TDD for storage
- Testing patterns
1. **[learning-idp-azure-compute](https://github.com/vanHeemstraSystems/learning-idp-azure-compute)**
- VM disk storage
- Persistent volumes
1. **[learning-idp-azure-networking](https://github.com/vanHeemstraSystems/learning-idp-azure-networking)**
- Storage networking
- Private endpoints
1. **[learning-idp-azure-security](https://github.com/vanHeemstraSystems/learning-idp-azure-security)**
- Storage security
- Encryption
1. **[learning-idp-infrastructure-as-code](https://github.com/vanHeemstraSystems/learning-idp-infrastructure-as-code)**
- Storage IaC
- Template deployment

-----

## 👥 Community Resources

### Forums & Discussion

#### Official Microsoft

- [Azure Storage Forum](https://learn.microsoft.com/en-us/answers/tags/133/azure-storage) - Q&A
- [Azure Storage Blog](https://techcommunity.microsoft.com/t5/azure-storage-blog/bg-p/AzureStorageBlog) - Official blog
- [GitHub Discussions](https://github.com/Azure/azure-sdk-for-python/discussions) - SDK discussions

#### Stack Overflow

- [azure-storage](https://stackoverflow.com/questions/tagged/azure-storage) - General storage
- [azure-blob-storage](https://stackoverflow.com/questions/tagged/azure-blob-storage) - Blob questions
- [azure-data-lake](https://stackoverflow.com/questions/tagged/azure-data-lake) - Data Lake

### Social Media & Communities

#### Discord & Slack

- [Azure Community Discord](https://discord.gg/azure) - Community chat
- [Cloud Native Computing Foundation](https://slack.cncf.io/) - CNCF Slack
- [Data Engineering Slack](https://dataengineering.slack.com/) - Data community

#### Reddit

- [r/Azure](https://www.reddit.com/r/AZURE/) - Azure discussions
- [r/dataengineering](https://www.reddit.com/r/dataengineering/) - Data engineering
- [r/cloudcomputing](https://www.reddit.com/r/cloudcomputing/) - Cloud topics

### Blogs & Newsletters

#### Microsoft Blogs

- [Azure Storage Blog](https://techcommunity.microsoft.com/t5/azure-storage-blog/bg-p/AzureStorageBlog) - Official blog
- [Azure Architecture Blog](https://techcommunity.microsoft.com/t5/azure-architecture-blog/bg-p/AzureArchitectureBlog) - Architecture
- [Data & AI Blog](https://techcommunity.microsoft.com/t5/azure-data-blog/bg-p/AzureDataBlog) - Data topics

#### Community Blogs

- [Cloud Skills](https://cloudskills.io/blog) - Cloud development
- [Azure Greg](https://gregorsuttie.com/) - Azure tips
- [Build5Nines](https://build5nines.com/) - Cloud architecture

-----

## 📊 Cheat Sheets & Quick References

### Azure Storage

- [Storage Account Comparison](https://learn.microsoft.com/en-us/azure/storage/common/storage-account-overview#types-of-storage-accounts) - Account types
- [Azure CLI Storage Commands](https://learn.microsoft.com/en-us/cli/azure/storage) - CLI reference
- [AzCopy Commands](https://learn.microsoft.com/en-us/azure/storage/common/storage-ref-azcopy) - AzCopy guide

### Access Tiers

- [Blob Access Tiers](https://learn.microsoft.com/en-us/azure/storage/blobs/access-tiers-overview) - Tier comparison
- [Lifecycle Policy Examples](https://learn.microsoft.com/en-us/azure/storage/blobs/lifecycle-management-policy-configure) - Policy samples

### Performance

- [Storage Scalability Targets](https://learn.microsoft.com/en-us/azure/storage/common/scalability-targets-standard-account) - Limits
- [Performance Checklist](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-performance-checklist) - Optimization

-----

## 🎯 Next Steps

After mastering Azure Storage, continue with:

1. **[learning-idp-azure-security](https://github.com/vanHeemstraSystems/learning-idp-azure-security)** - Storage security
1. **[learning-idp-observability](https://github.com/vanHeemstraSystems/learning-idp-observability)** - Storage monitoring
1. **[learning-idp-cicd-pipelines](https://github.com/vanHeemstraSystems/learning-idp-cicd-pipelines)** - Storage automation
1. **[learning-idp-infrastructure-as-code](https://github.com/vanHeemstraSystems/learning-idp-infrastructure-as-code)** - Storage IaC

-----

*Last updated: December 18, 2025*
*Part of the learning-internal-development-platform series*
