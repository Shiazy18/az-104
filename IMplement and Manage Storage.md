# Implement and manage storage

Azure Storage accounts support a maximum of 5 stored access policies per container.
Azure Storage accounts support a maximum of 2 immutable blob storage policies per container.

'`azcopy copy`' command is used to upload files from an on-premises folder to an Azure Storage container. Blob storage and File storage are supported by az copy
`az storage blob` copy start is intended for copying blobs within Azure Storage
`azcopy sync` is used to synchronize files between a local folder and a storage container, rather
`az storage blob` copy start-batch is designed for batch copying blobs within Azure Storage,

the net use command relies on the SMB (Server Message Block) protocol, which only supports authentication using the Azure Storage account key for access to Azure File Shares.

when using `customer-managed keys` with Azure Storage, the service supports `RSA keys` for encryption stored in Azure Key Vault.
`AES` is commonly used for encryption
`customer-managed keys` stored in Azure Key Vault, the maximum supported bit length for RSA encryption keys is `4096` bits.

`App Service` backups do not use Backup vaults; they rely on Azure Storage accounts.
`Recovery Services vaults` are used for Azure Backup and Azure Site Recovery, not for App Service backups.

`Azure App Service`, you can exclude specific files or folders from a backup by creating a _backup.filter file in the root directory of the app.
WebJobs are used to run background tasks in Azure App Service,

`Azure Files` provides a fully managed SMB file share that can be mounted by Azure container instances as persistent storage. This is essential for scenarios like running Microsoft SQL Server in a container, where data needs to persist across container restarts. However, it is important to note that volume mounting, including Azure Files, is currently only supported for Linux-based Azure container instances. Therefore, this solution assumes that Image1 is a Linux container image running SQL Server for Linux (which is fully supported).

`Azure's availability zones` are designed to protect against datacenter-level failures, providing high availability by distributing resources across multiple zones within a region.

`Azure Backup` uses block blobs to store backup data, making BlobStorage an appropriate type for this purpose. Additionally, placing backup data in the same region as the resource being backed up minimizes latency and avoids additional costs associated with cross-region data transfers.

`Lifecycle management policies` are supported for block blobs and append blobs in general-purpose v2, premium block blob, and Blob Storage accounts.

AzCopy supports copying data to Blob storage and File storage,

only storage accounts configured with `LRS` (Locally Redundant Storage), `GRS` (Geo-Redundant Storage), or `RA-GRS` (Read-Access Geo-Redundant Storage) support moving blob data to the Archive access tier.

 Azure Blob Storage is configured using `immutability` policies (such as time-based retention or legal hold), which are set at the container level.

`stored access policies` are used in conjunction with Shared Access Signatures (SAS) to manage shared access over time, but they cannot enforce access based on blob index tags.


- `Azure Storage` accounts allow a maximum of `five` `stored access policies` per container.
- In Azure Blob Storage, you can create up to `two immutable blob stored access policies per container`. 

The `Cool tier` has a minimum retention `period of 30 days`, meaning that if a blob is deleted, overwritten, or moved to another tier before 30 days, an early deletion penalty applies.

The `Archive tier` has a minimum retention period of 180 days.

 `Azure Object Replication` is a feature of Azure Blob Storage, and it works at the container level. only to block blobs

 frequency you can choose while configuring backup for blob storage can be either daily or weekly.

 Azure Backup supports taking snapshots of Azure File Shares up to six times per day, ie, every 4 hours

 the frequency you can choose while configuring `backup` for blob storage can be either daily or weekly.

`Global Admins` do not have permissions to assign custom security attributes to Entra objects.

`custom security` attributes cannot be assigned to Microsoft 365 groups.

`Encryption scopes` in Azure are designed to apply to Blob storage, specifically to containers and individual blobs within a storage account.

Azure Backup requires that the storage account used for diagnostic settings (like Azure Backup reports) be in the same region as the Recovery Services vault (Vault1).

The location of the `Log Analytics workspace` does not need to match the location of the Recovery Services vault.

Availability zones provide resilience within a region, but they do not protect against a full regional outage.