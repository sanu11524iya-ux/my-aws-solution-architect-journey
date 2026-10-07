# My AWS Solutions Architect Journey 

This is my official live report tracking my hands-on experience, cloud architecture designs, and theoretical understanding of Amazon Web Services.

# 1.Amazon S3 & Serverless Storage

 # 1. Core Architecture Concepts
 **Buckets & Objects**: Learned that buckets are globally unique containers and files are stored as independent "Objects" with keys and metadata.
 **Flat File Architecture**: S3 does not have real physical folders; it uses object paths (Keys) like `photos/waves.html` to simulate folder structures.
 **Static vs Dynamic**: S3 is perfect for serverless static hosting (HTML, CSS, Images, Videos) . Dynamic backends (Node.js/Python) and databases go to Amazon EC2 or RDS, not S3.

# 2. Request & Response Cycle
**Client Request:** User types a website URL in the browser window.
**DNS Resolution AWS Route 53:** translates the human URL into a computer-readable **IP Address**.
**Security Gatekeeper:** The request passes through AWS Security Groups/Firewalls.
**Data Retrieval:** S3 fetches the requested root object (like `waves.html`) .
**Server Response:** The files are sent back to the browser, making the website live in milliseconds!

# 3. Security Access Policies
 **User-Based Policy:** Permissions assigned directly to a specific user/employee (e.g., Amit can access this bucket).
**Resource-Based Policy:** Permissions attached directly to the S3 Bucket (e.g., S3 Bucket Policy allowing partner companies or the general public to view images).

##  Hands-on Project Completed (Simulator Lab)
1. Created a globally unique S3 bucket.
2. Uploaded `waves.html` and an image file from my local computer.
3. Enabled **Static Website Hosting** in bucket properties and changed the Index Document root file from `index.html` to `waves.html.
4. Successfully resolved issues where filenames did not match settings (`web.html` vs `index.html`) to validate the DIY task.
