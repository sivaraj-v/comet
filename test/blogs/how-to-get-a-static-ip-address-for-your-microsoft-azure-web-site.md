---
title: How to get a static IP address for your Windows App Service Web App
ms.date: 05/05/2014
archived_blog_id: "4073"
archived_blog_orig_url: https://blogs.msdn.microsoft.com/benjaminperkins
archived_blog_post_author: benjaminperkins
archived_blog_post_author_email: live@perkinsville.com
archived_blog_post_id: "213"
---

# How to get a static IP address for your Windows App Service Web App

This article has been moved to its new home here:  https://benperk.github.io/msdn/2014/2014-05-how-to-get-a-static-ip-address-for-your-microsoft-azure-web-site.html  
  
**11-AUG-2016:** This article discusses **INBOUND IPs**, if you are looking for a single outbound IP address, Web Apps do not support that, instead there is a group of \~4 outgoing IP addresses described [here](https://blogs.msdn.microsoft.com/benjaminperkins/2016/03/02/how-to-find-you-outgoing-azure-app-service-ip-address/).  If you want your own set of outbound IPs, consider an ASE described [here](https://azure.microsoft.com/en-us/documentation/articles/app-service-app-service-environment-intro/).  
  
**25-OCT-2017:** If you delete an exisiting binding during the certificate renewal process, then you likley will get a new inbound IP address allocated.  This would cause a problem with an A record DNS configuration.  Therefore, to renew a certificate, upload the new certificate, noting the new thumbprint and bind that one to the App Service domain without deleting the old one, I.e. replace/update instead of delete/add.  
  
When you host your web site on the Azure Web App platform it is bound to a virtual IP address that is shared with other web sites in that region stamp.  See in Figure 1 where I performed an NSLOOKUP of a few of my test Web App sites, they return the same IP address.  Sometimes you might need or want your own static IP address for your web site.  This article explains how you can do that.  
  
[![](https://msdnshared.blob.core.windows.net/media/MSDNBlogsFS/prod.evol.blogs.msdn.com/CommunityServer.Blogs.Components.WeblogFiles/00/00/01/47/48/2766.334.PNG)]()  
  
**Figure 1, same IP address for all Azure Web App**  
  
The basic concept is that you will need to install and configure an IP based SSL certificate.  A self-signed certificate will work fine, so there is no requirement to purchase an SSL certificate to get the static IP address.  The caveats are that your Web App must be in either Basic or Standard mode and there is likely some billing impact when using an SSL certificate.  See [here](https://azure.microsoft.com/en-us/pricing/details/web-sites/#ssl-connections).  
  
NOTE:  I have read/heard that when using [Web Hosting Plans / App Service Plans](https://azure.microsoft.com/en-us/documentation/articles/azure-web-sites-web-hosting-plans-in-depth-overview) that you get 1 free static IP address, so check out this link to see if you find the same.  
  
The steps required to setup a self-signed IP based SSL certificate so that you get a free static IP address is by following these steps.  

1.  Make sure your Web App is in either Basic or Standard mode
2.  Configure CNAME in DNS for your Web App
3.  Create a self-signed SSL certificate
4.  Upload an configure the certificate

# Scale your Web App to either Basic or Standard mode

  
Select the Web App that you want the static IP for and make sure it is scale to either Basic or Standard as shown in Figure 2.  
  
[![](https://msdnshared.blob.core.windows.net/media/MSDNBlogsFS/prod.evol.blogs.msdn.com/CommunityServer.Blogs.Components.WeblogFiles/00/00/01/47/48/1805.335.PNG)]()  
  
**Figure 2, Azure Web App in Basic or Standard mode**

# Configure CNAME in DNS

  
You will need to have a custom domain mapped to your Web App URL.  [Here](../waws/three-easy-steps-to-add-a-custom-domain-to-a-waws-site) are the instructions for achieving that.  

# Create a Self-Signed Certificate

  
I created an article on how to create and export a self-signed certificate [here](../benjaminperkins/make-your-own-ssl-certificate-for-testing-and-learning), so use that as a reference for this step.  Take note that the certificate Subject Name must match the custom domain name mapped to the MAWS.  That article discusses how to create the self-signed certificate using MAKECERT and then imports it into IIS, but you can import the same certificate into Web App.  

# Upload and configure the self-signed certificate

  
Once you are ready to configure the self-signed SSL certificate, access the Microsoft Azure management portal, select the web site which you would like the static IP address for and click on the CONFIGURE item at the top of the page.  Once on this page scroll down until you see CERTIFICATES as illustrated in Figure 3.  
  
[![](https://msdnshared.blob.core.windows.net/media/MSDNBlogsFS/prod.evol.blogs.msdn.com/CommunityServer.Blogs.Components.WeblogFiles/00/00/01/47/48/5314.336.PNG)]() [![1007](https://msdnshared.blob.core.windows.net/media/2014/05/1007.png)]()  
  
**Figure 3, uploading and configuring a self-signed certificate on Azure Web App**  
  
Click on the UPLOAD A CERTIFICATE button and upload the self-signed certificate.  Once uploaded, click on the drop-downs in the SSL BINDINGS section and map the self-signed certificate to the domain name.  Figure 4 illustrates an example of how this might look.  
  
[![](https://msdnshared.blob.core.windows.net/media/MSDNBlogsFS/prod.evol.blogs.msdn.com/CommunityServer.Blogs.Components.WeblogFiles/00/00/01/47/48/0207.337.PNG)]() [![1008](https://msdnshared.blob.core.windows.net/media/2014/05/1008.png)]()  
  
**Figure 4, configure an IP based SSL self-signed certificate Microsoft Azure Web Apps**  
  
When I tested this it did take some time for the static IP address to show up in NSLOOKUP.  But after some minutes it did happen.  Figure 5 illustrates that the Web App and custom domain now have a different IP address than my other Web App sites in the same region and stamp.  
  
[![](https://msdnshared.blob.core.windows.net/media/MSDNBlogsFS/prod.evol.blogs.msdn.com/CommunityServer.Blogs.Components.WeblogFiles/00/00/01/47/48/7183.338.PNG)]()  
  
**Figure 5, a free static IP using Azure Web App**  
  
Notice that the IP address has changed from the one shown previously in Figure 1.  This was the objective and it has been met.

