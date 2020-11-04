---
title: Microsoft Learn support - Troubleshooting known issues
description: Troubleshooting resources for Microsoft Learn.
author: Sadadow
ms.author: Saadad
ms.date: 11/01/2019
ms.topic: article
ms.prod: learning
featureFlags:
- show_feedback_report
# layout: ContentPage
---
# Troubleshooting known issues

We’re continually improving Microsoft Learn. But if you have a issue, one of these troubleshooting steps might help.

| Common issue or error message        | Recommended quick fix  |
| :-------------------------------------- |:-----------------------|
| "MSA account requires additional verification steps." |The Microsoft account that you use to sign into Microsoft Docs may need verification if you haven’t used that account for a while, or if your account requires email or phone verification. You will need to resolve your account login issue through https://support.microsoft.com to use it on Microsoft Docs. |
| "You have used all of your sandboxes for today." | You can activate up to 4 sandbox environments per day. Once you have used all your sandboxes for the day, you'll need to wait 24 hours before you can activate additional sandboxes. <!--Only successful sandbox activations are counted towards your daily limit, so clicking the "Activate Sandbox" button on a module to test if your 24 hours have elapsed will not reset or extend your 24 hours. Need to complete a module, but have used all of your sandboxes for the day? Many module exercises can be completed using your Azure subscription, but charges may apply, and you may need to modify the instructions to work with your subscription.--> |
|  "An unexpected error occurred" or "Hmm, something went wrong."       |  These errors appear when you're activating the sandbox.  Select the **Retry activating sandbox** button, or log out and log back into your user before trying again. |
| "Invitation redemption failed."   |   Navigate back to the unit page and accept the invitation again.  |
|Unable to start the Cloud Shell | You need to have third-party cookies enabled in your browser. Use the following steps for your browser to enable them. <br><br>**Edge** - go to **Settings** > **Privacy and Security** > **Cookies** > **Don't block cookies** <br>**Internet Explorer** - go to **Internet Options** > **Privacy** > **Advanced** > **Accept Third-party Cookies** <br>**Firefox** - go to **Tools** > **Options** > **Privacy** > **Accept Third-party Cookies** <br>**Chrome** - go to **Settings** > **Privacy and security** > **Content Setting** > **Cookies**, and turn off "Block third-party cookies."|
| "You're signed into the cloud shell with an account that's different from your docs account." | Select **Sign out** below the error message. If that still doesn't fix the issue, try clearing your browser’s cache/cookies, or log in with an incognito window.|
| "Cloud Shell exceeds the active user quota." | The Cloud Shells that we have available are currently all in use. Try refreshing the page, or returning 20 minutes later. |
| “AuthorizationFailed”,  “does not have authorization to perform action”, or “resource group not found” | Try the steps again by signing in through a new, private browser window. If that still doesn't fix the issue, try clearing your browser’s cache/cookies, or log in with an incognito window.|
| "Storage creation failed." |   If that still doesn't fix the issue, try clearing your browser’s cache/cookies, or log in with an incognito window.  |
| "You're unable to provision Azure resources." | For security reasons, users with .onmicrosoft.com addresses are prevented from opening the sandbox. You will not see this issue if you log in with your personal Microsoft account. |
| Azure Cloud Shell opens without bringing up the prompt. |   This is a known issue in Edge and Safari. For now, use Chrome for the best user experience.  |
| The resource group is in a deprovisioning state and can't perform this operation, or the resource group is deleted. |   There's a one-hour time limit for virtual machine sandboxes. <!--, and a four-hour time limit for other sandboxes. The whole module must be finished before it times out.--> Once the sandbox expires, you can activate a new sandbox and start the module over. |
| Progress isn't saving. | Progress can take a few seconds to register in our system, so it might look like it isn't registered right away. Try refreshing the page after a few seconds. <!--If the issue persists, please reach out to our team.--> |
| Completing a module or learning path doesn't grant you a badge/trophy. | This issue primarily occurs when using Internet Explorer to view profiles. Try again with a different browser. |<!--| Deployment failed or you get a "The template deployment failed because of policy violation" error. |   Please let us know by sending a message to our team. Include any relevant reproduction steps, error messages, and/or screenshots.|-->
| "No such file or directory" |   <!--Please check you are using the right commands.--> Confirm your location in the folder structure within the module is the correct location for your commands. |
| The sandbox for this module is temporarily disabled for maintenance. |  We're working on improvements to the modules. When this message is disabled, you can use the sandbox in this module again. |
| You can't register your account. | Open your browser in InPrivate/private browsing and try to register again. </br><ol><li>Open the Console in your browser, which is normally able to opened by pressing F12.</li><li>In the **Console** window, retry your registration.</li><li>If it continues to fail, take a screenshot of any error shown in the **Console** window.</li></ol> <!--2) Ask user for permission to capture a screen recording of the user’s entire registration flow.  You can record the screen in Teams.  This enables the Microsoft Learn team to see the problem visually.--> |
| You can't activate a Sandbox using your "onmicrosoft.com" account.| This is a known issue. Currently, onmicrosoft.com accounts cannot be used to activate a Learn sandbox. Please log in with another Microsoft account, such as an Outlook.com account, or create a new Microsoft account for free at [Outlook.com](https://outlook.live.com/owa/). <br> If you created your Learn profile using an onmicrosoft.com account, you can link a second Microsoft account in your profile. Navigate to your Learn profile, click "Settings" in the left-side navigation menu, scroll to "Account Management" to find the header "Linked accounts." Click "+ Add account," then follow the prompts to login with the additional Microsoft account. |
