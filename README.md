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

Bucket Versioning:
Bucket versioning in S3 is a feature that allows you to keep multiple versions of an object in the same bucket. When versioning is enabled, any time an object is modified or deleted, S3 retains the previous versions instead of overwriting or permanently deleting them.

Benefits and Use Cases
🛡️ Protect Against Accidental Deletion or Overwrites
If someone accidentally deletes or overwrites a file, you can restore the previous version.
📂 Keep File History (Audit/Backup)
Useful for tracking changes to data or retaining historical backups.
🔁 Easy Recovery
Quickly roll back to an earlier version of a file.
💼 Compliance and Data Retention
Helps meet regulatory requirements for data retention and recovery.

Default Encryption in an S3 Bucket?
Default encryption in Amazon S3 automatically encrypts all new objects when they are stored in the bucket, without requiring the uploader to explicitly specify encryption.
It helps enforce data protection by ensuring that all objects are encrypted at rest.
Key Points
Applies to new objects only (existing objects are not automatically encrypted).
Automatic encryption happens during object upload.
You can choose the encryption method.
It doesn't change the way you access your objects — encryption and decryption are handled transparently by S3.
🔑 Supported Encryption Types
SSE-S3 (Server-Side Encryption with Amazon S3-Managed Keys)
No key management needed
AWS handles key creation, rotation, and storage
✅ Simple & sufficient for most users
Header: x-amz-server-side-encryption: AES256
SSE-KMS (Server-Side Encryption with AWS KMS Keys)
Uses AWS Key Management Service (KMS)
Offers better control, logging, and auditing

Slight additional cost

Header: x-amz-server-side-encryption: aws:kms

SSE-C (Customer-Provided Keys) — Not supported for default encryption

The user supplies their own key each time (not recommended for default encryption)

🧘 Why Use Default Encryption?
✅ Data security compliance

✅ No need to rely on developers to specify encryption headers

✅ Peace of mind: everything uploaded is encrypted by default

##################################################

executed a simple project on hosting a website on s3 bucket 

 Sample Project: Static Website Hosting using S3
We’ll host a basic HTML website on S3.
🛠️ Files:
Create two files locally:

index.html

html
Copy
Edit
<!DOCTYPE html>
<html>
<head>
  <title>My S3 Website</title>
</head>
<body>
  <h1>Hello from AWS S3!</h1>
</body>
</html>

error.html

html
Copy
Edit
<!DOCTYPE html>
<html>
<head>
  <title>Error</title>
</head>
<body>
  <h1>Oops! Page not found.</h1>
</body>
</html>

📤 Upload to S3
Create a bucket: my-s3-website-yourname

Uncheck “Block all public access”

Go to Properties → Static Website Hosting

Enable

Index: index.html

Error: error.html

Upload both files to the root

Make files public

🌐 Test Website
Copy Endpoint URL from “Static website hosting”

Open in browser — you’ll see your hosted website

















