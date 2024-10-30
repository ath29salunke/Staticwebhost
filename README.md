# Staticwebhost
To host a static website on Google Cloud Platform (GCP), you can use Google Cloud Storage (GCS), which is cost-effective and fast.

Step 1: Set Up a Google Cloud Project
Go to the Google Cloud Console.
Create a new project or select an existing one.
Enable billing for the project if it's not already enabled.



Step 2: Create a Cloud Storage Bucket
Go to Cloud Storage > Buckets in the console.
Click Create bucket.
Give your bucket a globally unique name (e.g., my-static-website-123).
Choose the region for your bucket.
Set the Access control to Uniform for easier configuration.
Click Create.


Step 3: Upload Your Website Files
Click on your newly created bucket.
Use the Upload files or Upload folder option to add your HTML, CSS, JS, and any other static files to the bucket.


Step 4: Set Up the Bucket for Website Hosting
In your bucket, go to the Settings tab and choose Edit website configuration.
Set the Main page (typically index.html) and Error page (e.g., 404.html).
Save the changes.


Step 5: Make Your Website Files Public
Go back to your bucket's Permissions tab.
Click + Grant access.
Under New principals, type allUsers.
Select Role as Storage Object Viewer.
Save the permissions to allow public access.


Step 6: Test Your Website
Open the Overview tab of your bucket.
Copy the Public URL for your index.html or other files.
Open the link in your browser to view your website.
Optional: Set Up a Custom Domain (If Desired)
Verify domain ownership in GCP by going to Search Console or through Cloud DNS.
Create a CNAME record pointing your domain to c.storage.googleapis.com if using a custom domain.
Configure SSL (optional, but recommended) by using Cloud Load Balancing with a Cloud Storage backend. This setup adds complexity but ensures secure HTTPS access.
Once completed, your static website should be live on GCP!
