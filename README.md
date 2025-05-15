# aws_s3
s3 stands for simple storage service. where we can store data in terms of obects like images,text files and videos e.t.c
what we push files are data in the bucket we can access any where in the world.

if you moveing to the process of creating the bucket we need to know few important terms or steps to create a bucket for accurate use.
first we have region : we can chose the region where we have to host the data

bucket type:
in this we have two types 1. general purpose 2.directoey 
first talk about general purpose:
Amazon S3 supports two types of buckets. You can't change the bucket type after you have created the bucket.
General purpose buckets – A general purpose bucket is the default Amazon S3 bucket type. General purpose buckets are recommended for the majority of use cases in Amazon S3. These buckets support most Amazon S3 storage classes and all Amazon S3 features.
General purpose buckets have a flat storage structure instead of a hierarchical structure like you might see in a file system. However, the Amazon S3 console supports the folder concept as a means of grouping objects by using a shared name prefix for objects in the same folder. A general purpose bucket's name must be globally unique and follow a specific set of bucket naming rules.
When you create a general purpose bucket, you specify the AWS Region where you want Amazon S3 to create your bucket. The objects inside of your buckets are stored across a minimum of three Availability Zones (AZs) in the specified AWS Region.

Directory bucket – A directory bucket is an Amazon S3 bucket type that is used for workloads or performance-critical applications that require consistent single-digit millisecond latency. Directory buckets organize data hierarchically into directories, and can elastically scale performance to support hundreds of thousands of transactions per second (TPS). Directory buckets support only the S3 Express One Zone storage class and a limited set of Amazon S3 features.
You can create a directory bucket in a supported Availability Zone (AZ) that you choose. Unlike general purpose buckets, directory buckets exist only in a single Availability Zone in a single AWS Region. For optimal performance, we recommend that you co-locate your directory bucket and your computer resources in the same Availability Zone.
Directory bucket names must be unique within the chosen AZ, and the AZ ID is automatically included in the directory bucket name's suffix.


