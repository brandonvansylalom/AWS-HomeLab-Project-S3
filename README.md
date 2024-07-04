<h1>AWS Project - Hosting a static website using S3 on Route 53</h1>

<h2>Description</h2>
This is an entry-level/beginner project to introduce familiarity with AWS, starting with S3. I'll be setting up a website using Amazon S3 and connecting it to a custom domain via Amazon Route 53.
  
<h2>Lab walk-through/details:</h2>

<p align="center">

<b> Prepping the website template:

- <b> I'll be grabbing a custom template free-css.com to save time and download it to my workstation.

<img src="https://imgur.com/qIE9qqb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

ESTABLISH CUSTOM DOMAIN VIA ROUTE 53:

- <b> Registered and purchased a Domain from the Route 53 console
- <b> Set auto renew OFF in the meantime
- <b> Accept terms and conditions and registered/created domain name. (Takes about three days per AWS but can be quick as half an hour or less)

<img src="https://imgur.com/RwBzbHi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/hixJidH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

SET UP S3 BUCKET:

- <b> Create an S3 bucket and use the same domain name from when I registered it (it won't work if it's not matching)
- <b> I set the bucket permissions to allow public access (so the bucket is accessible to users).

<img src="https://imgur.com/4ekFrHD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/DTSNDiB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/83kDvTq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

UPLOAD THE WEBSITE:

- <b> I uploaded the website to the bucket.
- <b> I enabled static website hosting.
- <b> I set the permissions to attach a bucket policy, using a JSON script.

<img src="https://imgur.com/Fc2MW9m.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/muH0avB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/DhMjqF3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

REDIRECT URL BACK TO BUCKET NAME:

- <b> I created a new record on Route 53.
- <b> I configured a simple routing policy.
- <b> I set the traffic to be routed to the S3 website endpoint / to my region I hosted the bucket on.
- <b> The changes would take a few minutes but it'll be pointing to the S3 bucket afterwards.

<img src="https://imgur.com/dNeNtP8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/r7XQ9Hy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/dUXgmVu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

