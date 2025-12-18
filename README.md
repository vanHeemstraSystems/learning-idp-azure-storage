# Learning IDP: Azure Storage

This repository focuses on mastering Azure storage services using Python and Azure SDK to build, manage, and automate storage infrastructure for Internal Development Platform (IDP) development.

- [References](./REFERENCES.md)

## 🎯 Learning Objectives

By working through this repository, you will:

1. Master Azure Storage Account management and configuration
1. Implement Blob storage operations and lifecycle management
1. Work with Azure Files and File Shares
1. Understand Azure Queue and Table storage patterns
1. Implement Data Lake Storage Gen2 for analytics
1. Configure storage security and access control
1. Optimize storage performance and costs

## 📚 Prerequisites

- Python 3.11 or higher
- Azure subscription with contributor access
- Azure CLI installed and configured
- Completed [learning-idp-python-azure-sdk](https://github.com/vanHeemstraSystems/learning-idp-python-azure-sdk)
- Basic understanding of storage concepts
- Git and GitHub account

## 🗂️ Directory Structure

```
learning-idp-azure-storage/
├── README.md                          # This file
├── REFERENCES.md                      # Links to resources and related repos
├── pyproject.toml                     # Python project configuration
├── requirements.txt                   # Python dependencies
├── requirements-dev.txt               # Development dependencies
├── .python-version                    # Python version for pyenv
├── .gitignore                         # Git ignore patterns
├── .env.example                       # Environment variables template
│
├── docs/
│   ├── concepts/
│   │   ├── 01-storage-overview.md
│   │   ├── 02-storage-account-types.md
│   │   ├── 03-blob-storage.md
│   │   ├── 04-file-storage.md
│   │   ├── 05-queue-table-storage.md
│   │   └── 06-data-lake-gen2.md
│   ├── guides/
│   │   ├── getting-started.md
│   │   ├── storage-account-management.md
│   │   ├── blob-operations.md
│   │   ├── file-share-setup.md
│   │   └── security-configuration.md
│   └── examples/
│       ├── simple-storage-account.md
│       ├── blob-lifecycle.md
│       ├── file-share-access.md
│       ├── queue-messaging.md
│       └── data-lake-analytics.md
│
├── src/
│   ├── __init__.py
│   │
│   ├── core/
│   │   ├── __init__.py
│   │   ├── authentication.py          # Azure authentication
│   │   ├── config.py                  # Configuration management
│   │   ├── exceptions.py              # Custom exceptions
│   │   └── logging_config.py          # Logging setup
│   │
│   ├── storage_accounts/
│   │   ├── __init__.py
│   │   ├── account_manager.py         # Storage account CRUD
│   │   ├── account_types.py           # Account type utilities
│   │   ├── replication.py             # Replication configuration
│   │   └── access_keys.py             # Key management
│   │
│   ├── blob_storage/
│   │   ├── __init__.py
│   │   ├── blob_client.py             # Blob operations
│   │   ├── container_manager.py       # Container management
│   │   ├── blob_upload.py             # Upload operations
│   │   ├── blob_download.py           # Download operations
│   │   ├── blob_metadata.py           # Metadata management
│   │   └── lifecycle_manager.py       # Lifecycle policies
│   │
│   ├── file_storage/
│   │   ├── __init__.py
│   │   ├── file_share_manager.py      # File share operations
│   │   ├── file_client.py             # File operations
│   │   ├── directory_manager.py       # Directory management
│   │   └── share_snapshots.py         # Share snapshots
│   │
│   ├── queue_storage/
│   │   ├── __init__.py
│   │   ├── queue_manager.py           # Queue operations
│   │   ├── message_handler.py         # Message operations
│   │   └── queue_patterns.py          # Queue patterns
│   │
│   ├── table_storage/
│   │   ├── __init__.py
│   │   ├── table_manager.py           # Table operations
│   │   ├── entity_manager.py          # Entity CRUD
│   │   └── query_builder.py           # Query operations
│   │
│   ├── data_lake/
│   │   ├── __init__.py
│   │   ├── filesystem_manager.py      # Filesystem operations
│   │   ├── directory_client.py        # Directory operations
│   │   ├── file_client.py             # File operations
│   │   └── acl_manager.py             # ACL management
│   │
│   ├── security/
│   │   ├── __init__.py
│   │   ├── sas_token.py               # SAS token generation
│   │   ├── rbac_manager.py            # RBAC configuration
│   │   ├── encryption.py              # Encryption settings
│   │   └── network_rules.py           # Network configuration
│   │
│   └── monitoring/
│       ├── __init__.py
│       ├── diagnostics.py             # Diagnostic settings
│       ├── metrics.py                 # Storage metrics
│       └── analytics.py               # Storage analytics
│
├── examples/
│   ├── 01_storage_accounts/
│   │   ├── 01_create_storage_account.py
│   │   ├── 02_list_storage_accounts.py
│   │   ├── 03_configure_replication.py
│   │   ├── 04_manage_access_keys.py
│   │   └── 05_account_properties.py
│   │
│   ├── 02_blob_storage/
│   │   ├── 01_create_container.py
│   │   ├── 02_upload_blob.py
│   │   ├── 03_download_blob.py
│   │   ├── 04_list_blobs.py
│   │   ├── 05_blob_metadata.py
│   │   ├── 06_blob_snapshots.py
│   │   ├── 07_lifecycle_management.py
│   │   └── 08_blob_versioning.py
│   │
│   ├── 03_file_storage/
│   │   ├── 01_create_file_share.py
│   │   ├── 02_upload_file.py
│   │   ├── 03_download_file.py
│   │   ├── 04_directory_operations.py
│   │   ├── 05_share_snapshots.py
│   │   └── 06_file_share_access.py
│   │
│   ├── 04_queue_storage/
│   │   ├── 01_create_queue.py
│   │   ├── 02_send_message.py
│   │   ├── 03_receive_message.py
│   │   ├── 04_peek_messages.py
│   │   └── 05_queue_patterns.py
│   │
│   ├── 05_table_storage/
│   │   ├── 01_create_table.py
│   │   ├── 02_insert_entity.py
│   │   ├── 03_query_entities.py
│   │   ├── 04_update_entity.py
│   │   └── 05_batch_operations.py
│   │
│   ├── 06_data_lake/
│   │   ├── 01_create_filesystem.py
│   │   ├── 02_directory_operations.py
│   │   ├── 03_file_operations.py
│   │   ├── 04_acl_management.py
│   │   └── 05_data_analytics.py
│   │
│   ├── 07_security/
│   │   ├── 01_generate_sas_token.py
│   │   ├── 02_configure_rbac.py
│   │   ├── 03_encryption_setup.py
│   │   ├── 04_network_rules.py
│   │   └── 05_private_endpoints.py
│   │
│   └── 08_advanced/
│       ├── 01_async_operations.py
│       ├── 02_large_file_upload.py
│       ├── 03_geo_replication.py
│       ├── 04_cdn_integration.py
│       └── 05_backup_strategies.py
│
├── templates/
│   ├── storage_accounts/
│   │   ├── basic_storage.json        # Basic storage account
│   │   ├── premium_storage.json      # Premium storage
│   │   └── data_lake_gen2.json       # Data Lake Gen2
│   ├── policies/
│   │   ├── lifecycle_policy.json     # Lifecycle management
│   │   ├── access_policy.json        # Access policies
│   │   └── retention_policy.json     # Retention policies
│   └── scripts/
│       ├── backup_blob.sh            # Blob backup script
│       ├── sync_files.sh             # File sync script
│       └── cleanup_old_data.py       # Data cleanup
│
├── notebooks/
│   ├── 01_storage_basics.ipynb
│   ├── 02_blob_operations.ipynb
│   ├── 03_file_share_management.ipynb
│   ├── 04_data_lake_analytics.ipynb
│   └── 05_storage_optimization.ipynb
│
├── scripts/
│   ├── setup_storage_environment.sh   # Setup script
│   ├── cleanup_resources.sh           # Cleanup script
│   ├── storage_audit.py               # Storage audit tool
│   └── cost_analysis.py               # Cost analysis tool
│
├── tests/
│   ├── __init__.py
│   ├── conftest.py
│   ├── unit/
│   │   ├── test_account_manager.py
│   │   ├── test_blob_client.py
│   │   ├── test_file_share_manager.py
│   │   ├── test_queue_manager.py
│   │   └── test_table_manager.py
│   └── integration/
│       ├── test_storage_account_lifecycle.py
│       ├── test_blob_operations.py
│       ├── test_file_operations.py
│       └── test_data_lake_operations.py
│
└── .github/
    └── workflows/
        ├── test.yml                   # Run tests
        ├── examples.yml               # Test examples
        └── cleanup.yml                # Cleanup resources
```

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/vanHeemstraSystems/learning-idp-azure-storage.git
cd learning-idp-azure-storage
```

### 2. Set Up Python Environment

```bash
# Create virtual environment
python3 -m venv venv

# Activate virtual environment
# On Linux/MacOS:
source venv/bin/activate
# On Windows:
# venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
pip install -r requirements-dev.txt
```

### 3. Configure Azure Authentication

```bash
# Login to Azure
az login

# Set subscription
az account set --subscription "your-subscription-id"

# Create service principal (optional)
az ad sp create-for-rbac --name "idp-storage-sp" --role "Storage Blob Data Contributor"

# Configure environment variables
cp .env.example .env
# Edit .env with your credentials
```

### 4. Run Your First Example

```bash
# Create a storage account
python examples/01_storage_accounts/01_create_storage_account.py

# Create a blob container and upload a file
python examples/02_blob_storage/01_create_container.py
python examples/02_blob_storage/02_upload_blob.py

# Create a file share
python examples/03_file_storage/01_create_file_share.py
```

## 📖 Learning Path

Follow this recommended sequence:

### Week 1: Storage Fundamentals

**Day 1-2: Understanding Azure Storage**

1. Read `docs/concepts/01-storage-overview.md`
1. Study `docs/concepts/02-storage-account-types.md`
1. Run `examples/01_storage_accounts/01_create_storage_account.py`

**Day 3-5: Blob Storage**

1. Read `docs/concepts/03-blob-storage.md`
1. Complete all examples in `examples/02_blob_storage/`
1. Practice upload, download, and metadata operations

**Day 6-7: Blob Lifecycle Management**

1. Study lifecycle policies
1. Implement tiering strategies
1. Configure versioning and snapshots

### Week 2: File & Queue Storage

**Day 1-3: Azure Files**

1. Read `docs/concepts/04-file-storage.md`
1. Work through `examples/03_file_storage/`
1. Configure file shares and SMB access

**Day 4-5: Queue Storage**

1. Complete examples in `examples/04_queue_storage/`
1. Implement message patterns
1. Practice queue-based architectures

**Day 6-7: Table Storage**

1. Study NoSQL patterns
1. Work through `examples/05_table_storage/`
1. Implement entity operations

### Week 3: Data Lake & Security

**Day 1-3: Data Lake Gen2**

1. Read `docs/concepts/06-data-lake-gen2.md`
1. Complete `examples/06_data_lake/`
1. Configure hierarchical namespace
1. Implement ACL management

**Day 4-7: Storage Security**

1. Read `docs/guides/security-configuration.md`
1. Complete all examples in `examples/07_security/`
1. Configure SAS tokens and RBAC
1. Implement encryption and network rules

### Week 4: Advanced Topics & Production

**Day 1-3: Advanced Operations**

1. Work through `examples/08_advanced/`
1. Implement async operations
1. Configure geo-replication

**Day 4-5: Performance Optimization**

1. Study performance best practices
1. Implement caching strategies
1. Configure CDN integration

**Day 6-7: Production Readiness**

1. Implement monitoring and alerting
1. Configure backup strategies
1. Optimize costs

## 🔑 Key Azure SDK Packages

### Storage Management & Data Plane

```python
# Management (Control Plane)
azure-mgmt-storage>=21.0.0          # Storage account management

# Data Plane - Blob Storage
azure-storage-blob>=12.19.0         # Blob operations
azure-storage-blob-changefeed>=12.0.0  # Change feed

# Data Plane - File Storage
azure-storage-file-share>=12.15.0   # File share operations
azure-storage-file-datalake>=12.14.0  # Data Lake Gen2

# Data Plane - Queue Storage
azure-storage-queue>=12.9.0         # Queue operations

# Supporting Libraries
azure-identity>=1.15.0              # Authentication
azure-core>=1.29.0                  # Core functionality
```

## 💡 Common Operations Examples

### Create Storage Account

```python
from azure.identity import DefaultAzureCredential
from azure.mgmt.storage import StorageManagementClient
from azure.mgmt.storage.models import (
    StorageAccountCreateParameters,
    Sku,
    SkuName,
    Kind
)

credential = DefaultAzureCredential()
storage_client = StorageManagementClient(credential, subscription_id)

# Create storage account
storage_params = StorageAccountCreateParameters(
    sku=Sku(name=SkuName.STANDARD_LRS),
    kind=Kind.STORAGE_V2,
    location='westeurope',
    tags={
        'environment': 'development',
        'project': 'idp-learning'
    },
    enable_https_traffic_only=True,
    minimum_tls_version='TLS1_2',
    allow_blob_public_access=False
)

storage_account = storage_client.storage_accounts.begin_create(
    'my-rg',
    'mystorageaccount',
    storage_params
).result()

print(f"Created storage account: {storage_account.name}")
print(f"Primary endpoint: {storage_account.primary_endpoints.blob}")
```

### Upload and Download Blobs

```python
from azure.identity import DefaultAzureCredential
from azure.storage.blob import BlobServiceClient, ContainerClient, BlobClient

# Initialize clients
credential = DefaultAzureCredential()
account_url = "https://mystorageaccount.blob.core.windows.net"
blob_service_client = BlobServiceClient(account_url, credential=credential)

# Create container
container_name = "my-container"
container_client = blob_service_client.create_container(container_name)
print(f"Created container: {container_name}")

# Upload blob
blob_name = "sample.txt"
blob_client = blob_service_client.get_blob_client(
    container=container_name,
    blob=blob_name
)

with open("local-file.txt", "rb") as data:
    blob_client.upload_blob(data, overwrite=True)
    print(f"Uploaded blob: {blob_name}")

# Download blob
with open("downloaded-file.txt", "wb") as download_file:
    download_file.write(blob_client.download_blob().readall())
    print(f"Downloaded blob: {blob_name}")

# Set blob metadata
metadata = {
    'author': 'Willem',
    'category': 'documentation'
}
blob_client.set_blob_metadata(metadata)

# Get blob properties
properties = blob_client.get_blob_properties()
print(f"Content type: {properties.content_settings.content_type}")
print(f"Metadata: {properties.metadata}")
```

### Implement Lifecycle Management

```python
from azure.identity import DefaultAzureCredential
from azure.mgmt.storage import StorageManagementClient
from azure.mgmt.storage.models import (
    ManagementPolicy,
    ManagementPolicySchema,
    ManagementPolicyRule,
    ManagementPolicyDefinition,
    ManagementPolicyAction,
    ManagementPolicyBaseBlob,
    ManagementPolicySnapShot,
    DateAfterModification
)

credential = DefaultAzureCredential()
storage_client = StorageManagementClient(credential, subscription_id)

# Define lifecycle policy
policy = ManagementPolicy(
    policy=ManagementPolicySchema(
        rules=[
            ManagementPolicyRule(
                enabled=True,
                name='move-to-cool',
                type='Lifecycle',
                definition=ManagementPolicyDefinition(
                    actions=ManagementPolicyAction(
                        base_blob=ManagementPolicyBaseBlob(
                            tier_to_cool=DateAfterModification(
                                days_after_modification_greater_than=30
                            ),
                            tier_to_archive=DateAfterModification(
                                days_after_modification_greater_than=90
                            ),
                            delete=DateAfterModification(
                                days_after_modification_greater_than=365
                            )
                        ),
                        snapshot=ManagementPolicySnapShot(
                            delete=DateAfterModification(
                                days_after_creation_greater_than=90
                            )
                        )
                    ),
                    filters={
                        'blobTypes': ['blockBlob'],
                        'prefixMatch': ['logs/']
                    }
                )
            )
        ]
    )
)

# Apply lifecycle policy
storage_client.management_policies.create_or_update(
    'my-rg',
    'mystorageaccount',
    'default',
    policy
)
print("Lifecycle policy applied")
```

### Create and Use File Share

```python
from azure.identity import DefaultAzureCredential
from azure.storage.fileshare import ShareServiceClient, ShareClient, ShareFileClient

# Initialize clients
credential = DefaultAzureCredential()
account_url = "https://mystorageaccount.file.core.windows.net"
share_service_client = ShareServiceClient(account_url, credential=credential)

# Create file share
share_name = "my-share"
share_client = share_service_client.create_share(share_name, quota=100)
print(f"Created file share: {share_name}")

# Create directory
directory_name = "my-directory"
directory_client = share_client.get_directory_client(directory_name)
directory_client.create_directory()
print(f"Created directory: {directory_name}")

# Upload file
file_name = "sample.txt"
file_client = share_client.get_file_client(f"{directory_name}/{file_name}")

with open("local-file.txt", "rb") as source_file:
    file_client.upload_file(source_file)
    print(f"Uploaded file: {file_name}")

# Download file
with open("downloaded-file.txt", "wb") as file_handle:
    data = file_client.download_file()
    data.readinto(file_handle)
    print(f"Downloaded file: {file_name}")

# Create share snapshot
snapshot = share_client.create_snapshot()
print(f"Created snapshot: {snapshot['snapshot']}")
```

### Work with Queue Storage

```python
from azure.identity import DefaultAzureCredential
from azure.storage.queue import QueueServiceClient, QueueClient
import json

# Initialize clients
credential = DefaultAzureCredential()
account_url = "https://mystorageaccount.queue.core.windows.net"
queue_service_client = QueueServiceClient(account_url, credential=credential)

# Create queue
queue_name = "my-queue"
queue_client = queue_service_client.create_queue(queue_name)
print(f"Created queue: {queue_name}")

# Send message
message_data = {
    'task': 'process_data',
    'file': 'data.csv',
    'priority': 'high'
}
message = json.dumps(message_data)
queue_client.send_message(message)
print(f"Sent message: {message}")

# Receive messages
messages = queue_client.receive_messages(messages_per_page=5)
for msg in messages:
    print(f"Received message: {msg.content}")
    
    # Process message
    data = json.loads(msg.content)
    print(f"Processing task: {data['task']}")
    
    # Delete message after processing
    queue_client.delete_message(msg.id, msg.pop_receipt)
    print(f"Deleted message: {msg.id}")

# Peek at messages without removing them
peeked_messages = queue_client.peek_messages(max_messages=5)
for msg in peeked_messages:
    print(f"Peeked message: {msg.content}")
```

### Data Lake Gen2 Operations

```python
from azure.identity import DefaultAzureCredential
from azure.storage.filedatalake import (
    DataLakeServiceClient,
    FileSystemClient,
    DataLakeDirectoryClient
)

# Initialize clients
credential = DefaultAzureCredential()
account_url = "https://mystorageaccount.dfs.core.windows.net"
service_client = DataLakeServiceClient(account_url, credential=credential)

# Create file system
file_system_name = "my-filesystem"
file_system_client = service_client.create_file_system(file_system_name)
print(f"Created file system: {file_system_name}")

# Create directory
directory_name = "data/raw"
directory_client = file_system_client.create_directory(directory_name)
print(f"Created directory: {directory_name}")

# Upload file
file_name = "dataset.csv"
file_client = directory_client.create_file(file_name)

with open("local-dataset.csv", "rb") as data:
    file_contents = data.read()
    file_client.upload_data(file_contents, overwrite=True)
    print(f"Uploaded file: {file_name}")

# Set ACL (Access Control List)
acl = "user::rwx,group::r--,other::---"
directory_client.set_access_control(acl=acl)
print(f"Set ACL: {acl}")

# List files in directory
paths = file_system_client.get_paths(path=directory_name)
for path in paths:
    print(f"Path: {path.name}")
```

## 🎯 Best Practices

### 1. Storage Account Configuration

```python
# Use appropriate redundancy
storage_params = StorageAccountCreateParameters(
    sku=Sku(name=SkuName.STANDARD_GRS),  # Geo-redundant for production
    kind=Kind.STORAGE_V2,
    enable_https_traffic_only=True,
    minimum_tls_version='TLS1_2',
    allow_blob_public_access=False,  # Security best practice
    is_hns_enabled=True  # Enable hierarchical namespace for Data Lake Gen2
)
```

### 2. Secure Access with SAS Tokens

```python
from azure.storage.blob import BlobServiceClient, generate_blob_sas, BlobSasPermissions
from datetime import datetime, timedelta

# Generate SAS token with limited permissions and expiry
sas_token = generate_blob_sas(
    account_name='mystorageaccount',
    container_name='my-container',
    blob_name='sensitive-data.txt',
    account_key=account_key,
    permission=BlobSasPermissions(read=True),
    expiry=datetime.utcnow() + timedelta(hours=1)
)

# Use SAS token
blob_url = f"https://mystorageaccount.blob.core.windows.net/my-container/sensitive-data.txt?{sas_token}"
```

### 3. Implement Retry Logic

```python
from azure.core.pipeline.policies import RetryPolicy
from azure.storage.blob import BlobServiceClient

# Configure retry policy
retry_policy = RetryPolicy(
    retry_total=3,
    retry_backoff_factor=2,
    retry_backoff_max=30
)

blob_service_client = BlobServiceClient(
    account_url,
    credential=credential,
    retry_policy=retry_policy
)
```

### 4. Use Async Operations for Better Performance

```python
from azure.storage.blob.aio import BlobServiceClient
import asyncio

async def upload_multiple_blobs():
    async with BlobServiceClient(account_url, credential=credential) as client:
        container_client = client.get_container_client("my-container")
        
        tasks = []
        for i in range(10):
            blob_client = container_client.get_blob_client(f"file-{i}.txt")
            task = blob_client.upload_blob(f"Data {i}", overwrite=True)
            tasks.append(task)
        
        await asyncio.gather(*tasks)

asyncio.run(upload_multiple_blobs())
```

## 🔧 Development Tools

### Essential Tools

```bash
# Install storage tools
pip install azure-storage-blob
pip install azure-storage-file-share
pip install azure-storage-queue

# Storage Explorer (GUI)
# Download from: https://azure.microsoft.com/en-us/products/storage/storage-explorer/

# Code quality
black src/ examples/
ruff check src/ examples/
mypy src/

# Testing
pytest tests/
```

### Storage Testing

```bash
# Use Azurite for local testing
npm install -g azurite

# Start Azurite
azurite --silent --location /tmp/azurite --debug /tmp/azurite-debug.log

# Connect to Azurite in Python
from azure.storage.blob import BlobServiceClient

# Azurite default connection string
connection_string = "DefaultEndpointsProtocol=http;AccountName=devstoreaccount1;AccountKey=Eby8vdM02xNOcqFlqUwJPLlmEtlCDXJ1OUzFT50uSRZ6IFsuFq2UVErCz4I6tq/K1SZFPTOtr/KBHBeksoGMGw==;BlobEndpoint=http://127.0.0.1:10000/devstoreaccount1;"

blob_service_client = BlobServiceClient.from_connection_string(connection_string)
```

## 📊 Storage Architecture Patterns

### Tiered Storage Strategy

```
Hot Tier (Frequent Access)
    ↓ After 30 days
Cool Tier (Infrequent Access)
    ↓ After 90 days
Archive Tier (Rare Access)
    ↓ After 365 days
Delete
```

### Data Lake Organization

```
/raw/                   # Raw ingested data
  /source1/
  /source2/
/processed/            # Cleaned and transformed
  /daily/
  /monthly/
/curated/              # Business-ready data
  /reports/
  /analytics/
```

## 🔗 Related Repositories

- [learning-internal-development-platform](https://github.com/vanHeemstraSystems/learning-internal-development-platform) - Main overview
- [learning-idp-python-azure-sdk](https://github.com/vanHeemstraSystems/learning-idp-python-azure-sdk) - Azure SDK fundamentals
- [learning-idp-azure-compute](https://github.com/vanHeemstraSystems/learning-idp-azure-compute) - Compute resources
- [learning-idp-azure-networking](https://github.com/vanHeemstraSystems/learning-idp-azure-networking) - Network configuration
- [learning-idp-azure-security](https://github.com/vanHeemstraSystems/learning-idp-azure-security) - Security configuration

## 🤝 Contributing

This is a personal learning repository, but suggestions and improvements are welcome!

1. Fork the repository
1. Create a feature branch
1. Make your changes with tests
1. Ensure all tests pass
1. Submit a pull request

## 📄 License

This project is for educational purposes. See LICENSE file for details.

## 📧 Contact

Willem van Heemstra

- GitHub: [@vanHeemstraSystems](https://github.com/vanHeemstraSystems)
- LinkedIn: [Willem van Heemstra](https://www.linkedin.com/in/willemvanheemstra/)

-----

*Last updated: December 18, 2025*
*Part of the learning-internal-development-platform series*
