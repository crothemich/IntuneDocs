---
# required metadata

title: Intune quick start guide | Microsoft Intune
description:
keywords:
author: Staciebarker
manager: jeffgilb
ms.date: 04/28/2016
ms.topic: get-started-article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: d158503c-1276-422b-ab81-5f66c1cd7e7a

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: jeffgilb
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---


# Intune quick start guide
This walkthrough leads you through the steps of setting up a paid subscription of Microsoft Intune to quickly and easily begin managing mobile devices and Windows PCs in use by your organization. You can follow each step in order or just skip ahead if a step is not applicable to your specific environment or business needs.

>[!NOTE]
>This article focuses on setting up Intune as a standalone service. Alternatively, if you're currently using Microsoft System Center Configuration Manager to manage computers and servers, you can [extend Configuration Manager to manage mobile devices](https://technet.microsoft.com/library/jj884158.aspx) by connecting Intune with Configuration Manager in a hybrid MDM deployment to manage mobile devices too.

Can anyone edit this content, or just MS?

Getting started with a paid subscription of Intune shares many of the same steps as starting with the [Intune evaluation guide](/intune/understand-explore/get-started-with-a-30-day-trial-of-microsoft-intune). However, after your evaluation, and when you are ready to start managing your mobile devices, you will need to address several additional requirements. These will vary depending on your current network infrastructure and business requirements including:

-   Synchronizing on-premises Active Directory accounts with Intune and Azure Active Directory

-   Updating public domain and DNS service records with your domain registrar

-   Customizing Intune features for production use

>[!TIP]
>If you purchase at least 150 licenses for Microsoft Intune in an eligible plan, you can use the "FastTrack Center Benefit," a service where Microsoft specialists work with you to get your environment ready for Intune. See [Microsoft Intune Service Benefit Description](https://technet.microsoft.com/library/mt228265.aspx).


## Before you begin
Starting with a paid subscription means that you're ready to deploy Intune and make changes to your existing network infrastructure. This could range from simply adding or updating your internal and external DNS records to synchronizing your existing Active Directory user accounts to Azure Active Directory. Whatever mix of Intune  mobile device management features you decide on, you'll need to  carefully plan how Intune will interact with your existing network components and services. Specifically, you should review:

-   **How you'll manage user identity**:  For most medium to large sized organizations, connecting your existing directory services to Intune via Azure Active Directory is the best and most convenient way to manage user identity with Intune. This is especially true if you already use other Microsoft cloud services, such as Office 365 or Exchange Online. Synchronizing your existing user accounts using [Microsoft Azure Active Directory Connect](https://www.microsoft.com/download/details.aspx?id=47594) is a quick and easy way to connect your on-premises Active Directory to Azure Active Directory and configure a single sign-on authentication experience for your users.

-   **How DNS will be affected**: If you want to use your own domain name instead of the default onmicrosoft.com domain you get when first signing up for Intune, some public DNS record updates will be needed. DNS record updates are required so that mobile devices can locate the Intune service and ensure the management service for your subscription works correctly to manage all devices in use by your organization.

## Have the following items handy
Ready to get started? You'll need the following items when starting to use your paid subscription to Intune:

### A device with a Silverlight-enabled web browser
You will need this to access the Intune administration console where you'll manage devices, apps, and policies. You will also need a web browser to access the web-based company portal when not accessing the company portal app from a mobile device. To make things easier, you can use the “privacy mode” setting on the same browser that you use for Intune administration (for example: in Internet Explorer, you can click **Tools** &gt; **InPrivate Browsing**).

>[!TIP]
>Because of this requirement, the Microsoft Edge browser is not supported for accessing the Intune administration console.


### Certificates for mobile devices
If you'll manage iOS or Windows Phone devices with Intune, you'll need certificates and accounts to retrieve those certificates. You won't need any additional certificates to manage Android devices.

- No certificate is required for **Windows Phone 8.1** users who install the company portal app from the Store. However, a [Symantec code signing certificate](https://products.websecurity.symantec.com/orders/enrollment/microsoftCert.do) is required for **Windows Phone 8.0** or to use Intune to deploy the company portal app to Windows Phone 8.1 devices.

>[!NOTE]
>This getting started walkthrough assumes your users get the company portal app from the Store on a Windows Phone 8.1 or later device. For information about Windows Phone 8.0 support, see [Set up Windows Phone 8.0 management with Microsoft Intune](/Intune/deploy-use/set-up-windows-phone-8.0-management-with-microsoft-intune).

- There are no certificate requirements for **Windows PCs** or **Windows RT devices** when enrolling Windows PCs as devices or [installing the Windows PC client for Microsoft Intune](/intune/deploy-use/install-the-windows-pc-client-with-microsoft-intune).

- For **iOS** or **Mac OS X** devices you will need to request an Apple Push Notification service certificate from Apple, as described in step 3 of [Set up iOS and Mac management with Microsoft Intune](/intune/deploy-use/set-up-ios-and-mac-management-with-microsoft-intune).

### Next steps
It's time to get started with your paid subscription!

>[!div class="step-by-step"]
[**Sign in to Intune** &rarr;](start-with-a-paid-subscription-to-microsoft-intune-step-1.md)
