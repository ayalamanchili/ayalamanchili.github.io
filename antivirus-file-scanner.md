#### Organizations do intake files across multiple channels to support typical business functions.  It is critical to detect and quarantine virus and malware from these channels.

This article we provide a architecture walk through of implementing a file antivirus and antimalware scanner service that you could use in your organization.

#### Components
##### Antivirus Scan  Software
There are many commercial and open source options available. Research and identify the virus scanning software the fits your need. 
###### Things to consider

 - It's critical to keep the software up to date.
 - Create automation to keep the virus database up to date.
 - Fine tune the settings to make sure the right files are scanned eg: file extensions, content types etc.

##### Identify Incoming File sources
Conduct a thorough review of all your systems to identify all sources of files into your boundary. The number widely varies and that determines the effort of implementing the solution.  
###### Things to identify for each source

 - Identify interface to download the files
 - Gather needed access information
 - Gather file type, content types, size etc
 - Identify the uploader context and risk associated to them.

##### Setup Publishers for incoming files
Build Publishers to your file intake sources to send file metadata to a central file scanner Topic with the necessary information needed to scan the file.
A simple publisher can be a AWS Event that get triggered upon a file being uploaded to your s3 bucket.

##### Build File Scanner 
Create a service to listen to a Central file Scanner Topic. For each file that gets uploaded this service will evaluate the preconditions, download and scan the file. 
If a virus is detected create default action to quarantine it by moving it from source to a quarantine folder and send appropriate alerts.

Optionally you can publish the virus detected metadata information to a central Topic that the file source application can subscribe to take further action.
 

