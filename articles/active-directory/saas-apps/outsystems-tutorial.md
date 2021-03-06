---
title: 'Tutorial: Azure Active Directory integration with OutSystems Azure AD | Microsoft Docs'
description: Learn how to configure single sign-on between Azure Active Directory and OutSystems Azure AD.
services: active-directory
documentationCenter: na
author: jeevansd
manager: mtillman
ms.reviewer: celested

ms.assetid: cf6f99b7-0604-4db2-a72e-0d1a1d643a08
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: tutorial
ms.date: 07/18/2019
ms.author: jeedes

ms.collection: M365-identity-device-management
---

# Tutorial: Integrate OutSystems Azure AD with Azure Active Directory

In this tutorial, you'll learn how to integrate OutSystems Azure AD with Azure Active Directory (Azure AD). When you integrate OutSystems Azure AD with Azure AD, you can:

* Control in Azure AD who has access to OutSystems Azure AD.
* Enable your users to be automatically signed-in to OutSystems Azure AD with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

To learn more about SaaS app integration with Azure AD, see [What is application access and single sign-on with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-appssoaccess-whatis).

## Prerequisites

To get started, you need the following items:

* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* OutSystems Azure AD single sign-on (SSO) enabled subscription.

## Scenario description

In this tutorial, you configure and test Azure AD SSO in a test environment. OutSystems Azure AD supports **SP and IDP** initiated SSO and supports **Just In Time** user provisioning.

## Adding OutSystems Azure AD from the gallery

To configure the integration of OutSystems Azure AD into Azure AD, you need to add OutSystems Azure AD from the gallery to your list of managed SaaS apps.

1. Sign in to the [Azure portal](https://portal.azure.com) using either a work or school account, or a personal Microsoft account.
1. On the left navigation pane, select the **Azure Active Directory** service.
1. Navigate to **Enterprise Applications** and then select **All Applications**.
1. To add new application, select **New application**.
1. In the **Add from the gallery** section, type **OutSystems Azure AD** in the search box.
1. Select **OutSystems Azure AD** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

## Configure and test Azure AD single sign-on

Configure and test Azure AD SSO with OutSystems Azure AD using a test user called **B. Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user in OutSystems Azure AD.

To configure and test Azure AD SSO with OutSystems Azure AD, complete the following building blocks:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** to enable your users to use this feature.
2. **[Configure OutSystems Azure AD](#configure-outsystems-azure-ad)** to configure the SSO settings on application side.
3. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** to test Azure AD single sign-on with B. Simon.
4. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** to enable B. Simon to use Azure AD single sign-on.
5. **[Create OutSystems Azure AD test user](#create-outsystems-azure-ad-test-user)** to have a counterpart of B. Simon in OutSystems Azure AD that is linked to the Azure AD representation of user.
6. **[Test SSO](#test-sso)** to verify whether the configuration works.

### Configure Azure AD SSO

Follow these steps to enable Azure AD SSO in the Azure portal.

1. In the [Azure portal](https://portal.azure.com/), on the **OutSystems Azure AD** application integration page, find the **Manage** section and select **Single sign-on**.
1. On the **Select a Single sign-on method** page, select **SAML**.
1. On the **Set up Single Sign-On with SAML** page, click the edit/pen icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section, if you wish to configure the application in **IDP** initiated mode, perform the following steps:

    a. In the **Identifier** text box, type a URL using the following pattern:
    `http://<YOURBASEURL>/IdP`

    b. In the **Reply URL** text box, type a URL using the following pattern:
    `https://<YOURBASEURL>/IdP/SSO.aspx`

1. Click **Set additional URLs** and perform the following step if you wish to configure the application in **SP** initiated mode:

    In the **Sign-on URL** text box, type a URL using the following pattern:
    `https://<YOURBASEURL>`

	> [!NOTE]
	> These values are not real. Update these values with the actual Identifier, Reply URL and Sign-on URL. Contact [OutSystems Client support team](mailto:support@outsystems.com) to get these values. You can also refer to the patterns shown in the **Basic SAML Configuration** section in the Azure portal.

1. On the **Set up Single Sign-On with SAML** page, in the **SAML Signing Certificate** section, find **Federation Metadata XML** and select **Download** to download the certificate and save it on your computer.

   ![The Certificate download link](common/metadataxml.png)

1. On the **Set up OutSystems Azure AD** section, copy the appropriate URL(s) based on your requirement.

   ![Copy configuration URLs](common/copy-configuration-urls.png)

### Configure OutSystems Azure AD

To configure single sign-on on OutSystems side, you need to download the [IdP forge](https://www.outsystems.com/forge/component-overview/599/idp) component, configure it as mentioned in the [instructions](https://success.outsystems.com/Documentation/Development_FAQs/How_to_configure_OutSystems_to_use_identity_providers_using_SAML#Configure_your_application_to_use_IdP_connector). After installing the component and do the necessary code changes, configure Azure AD by downloading Federation Metadata XML from Azure portal and upload on OutSystems IdP component, according to the following [instructions](https://success.outsystems.com/Documentation/Development_FAQs/How_to_configure_OutSystems_to_use_identity_providers_using_SAML#Azure_AD_.2F_ADFS).

### Create an Azure AD test user

In this section, you'll create a test user in the Azure portal called B. Simon.

1. From the left pane in the Azure portal, select **Azure Active Directory**, select **Users**, and then select **All users**.
1. Select **New user** at the top of the screen.
1. In the **User** properties, follow these steps:
   1. In the **Name** field, enter `B. Simon`.  
   1. In the **User name** field, enter the username@companydomain.extension. For example, `BrittaSimon@contoso.com`.
   1. Select the **Show password** check box, and then write down the value that's displayed in the **Password** box.
   1. Click **Create**.

### Assign the Azure AD test user

In this section, you'll enable B. Simon to use Azure single sign-on by granting access to OutSystems Azure AD.

1. In the Azure portal, select **Enterprise Applications**, and then select **All applications**.
1. In the applications list, select **OutSystems Azure AD**.
1. In the app's overview page, find the **Manage** section and select **Users and groups**.

   ![The "Users and groups" link](common/users-groups-blade.png)

1. Select **Add user**, then select **Users and groups** in the **Add Assignment** dialog.

	![The Add User link](common/add-assign-user.png)

1. In the **Users and groups** dialog, select **B. Simon** from the Users list, then click the **Select** button at the bottom of the screen.
1. If you're expecting any role value in the SAML assertion, in the **Select Role** dialog, select the appropriate role for the user from the list and then click the **Select** button at the bottom of the screen.
1. In the **Add Assignment** dialog, click the **Assign** button.

### Create OutSystems Azure AD test user

In this section, a user called B.Simon is created in OutSystems. OutSystems supports just-in-time user provisioning, which is enabled by default. There is no action item for you in this section. If a user doesn't already exist in OutSystems, a new one is created after authentication.

### Test SSO

When you select the OutSystems Azure AD tile in the Access Panel, you should be automatically signed in to the OutSystems Azure AD for which you set up SSO. For more information about the Access Panel, see [Introduction to the Access Panel](https://docs.microsoft.com/azure/active-directory/active-directory-saas-access-panel-introduction).

## Additional resources

- [List of Tutorials on How to Integrate SaaS Apps with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-saas-tutorial-list)

- [What is application access and single sign-on with Azure Active Directory?](https://docs.microsoft.com/azure/active-directory/active-directory-appssoaccess-whatis)

- [What is Conditional Access in Azure Active Directory?](https://docs.microsoft.com/azure/active-directory/conditional-access/overview)
