# static-website-aws
A static website hosted on AWS using S3 and Route 53

I recently embarked on a project to host a static website using Amazon Web Services (AWS), specifically leveraging S3 for storage and Route 53 for DNS management. Here’s a brief overview of the steps I took, the challenges I faced, and how I overcame them. 🚀

Step 1: Setting Up the S3 Bucket 🗄️

Action: Created an S3 bucket to store the static files of the website. Defined the bucket properties in a CloudFormation template, enabling static website hosting.

Challenge: Initially faced issues with the bucket policy, which restricted public access to the files.

Solution: Modified the bucket policy to allow public read access, ensuring users could access the website without restrictions.

Step 2: Configuring the Website ⚙️

Action: Configured the S3 bucket to serve an index.html file as the landing page and an error.html file for handling errors.

Challenge: Encountered a "404 Not Found" error when trying to access the website, indicating that the specified files did not exist in the bucket.

Solution: Realized I needed to upload the index.html and error.html files to the S3 bucket. Created simple HTML files and uploaded them, resolving the issue.

Step 3: Setting Up Route 53 🌍

Action: Configured Route 53 to create a DNS record pointing to the S3 bucket, making the website accessible via a custom domain.

Challenge: Ensuring that the DNS settings were correctly configured to point to the S3 bucket's website endpoint was tricky.

Solution: Double-checked the bucket's website URL and ensured the CNAME record in Route 53 was set up correctly. This attention to detail paid off, as the website became accessible through the custom domain.

Step 4: Testing and Validation ✅
Action: Tested the website by accessing it through the browser. Pleased to see the index.html page load successfully, confirming that the deployment was successful.

Challenge: Had to ensure that the files were named correctly and that the S3 bucket was configured for static website hosting.
Solution: Carefully reviewed the file names and the bucket configuration, ensuring everything was in order. This meticulous approach helped avoid any further issues.

Conclusion 🎉

This project was a valuable learning experience that deepened my understanding of AWS services and cloud infrastructure. By overcoming challenges related to permissions, file management, and DNS configuration, I successfully deployed a static website that is now live and accessible.
I’m excited to continue exploring AWS and cloud technologies, and I look forward to applying these skills in future projects! 🌟
