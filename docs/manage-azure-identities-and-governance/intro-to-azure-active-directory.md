# Introduction to Azure Active Directory

## What is Azure Active Directory?
Azure Active Directory (Azure AD) is a cloud-based identity and access management service. Azure AD enables your employees access external resources, such as Microsoft 365, the Azure portal, and thousands of other SaaS applications.

## Who uses Azure AD?
- IT admins use Azure AD to control access to apps and app resources, based on business requirements.
- App developers can use Azure AD as a standards-based authentication provider that helps them add single sign-on (SSO) to apps that works with a user's existing credentials.
- Microsoft 365, Office 365, Azure, or Dynamics CRM Online subscribers already use Azure AD as every Microsoft 365, Office 365, Azure, and Dynamics CRM Online tenant is automatically an Azure AD tenant.

## What are the Azure AD licenses?

Microsoft Online business services, such as Microsoft 365 or Microsoft Azure, use Azure AD for sign-in activities and to help protect your identities. If you subscribe to any Microsoft Online business service, you automatically get access to Azure AD free.

To enhance your Azure AD implementation, you can also add paid features by upgrading to Azure Active Directory Premium P1 or Premium P2 licenses. Azure AD paid licenses are built on top of your existing free directory.

- **Azure Active Directory Free**: Provides user and group management, on-premises directory synchronization, basic reports, self-service password change for cloud users, and single sign-on across Azure, Microsoft 365, and many popular SaaS apps.

- **Azure Active Directory Premium P1**: In addition to the Free features, P1 also lets your hybrid users access both on-premises and cloud resources. It also supports advanced administration, such as dynamic groups, self-service group management, Microsoft Identity Manager, and cloud write-back capabilities, which allow self-service password reset for your on-premises users.


- **Azure Active Directory Premium P2**: In addition to the Free and P1 features, P2 also offers Azure Active Directory Identity Protection to help provide risk-based Conditional Access to your apps and critical company data and Privileged Identity Management to help discover, restrict, and monitor administrators and their access to resources and to provide just-in-time access when needed.

- **"Pay as you go"** feature licenses. You can also get licenses for features such as, Azure Active Directory Business-to-Customer (B2C). B2C can help you provide identity and access management solutions for your customer-facing apps. 

## Create a new tenant in Azure Active Directory

- Sign in to your organization's Azure portal.

- From the Azure portal menu, select Azure Active Directory.

- On the overview page, select Manage tenants

- Select Create. ![image](https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/media/active-directory-access-create-new-tenant/azure-ad-portal.png)


- On the Basics tab, select the type of tenant you want to create, either Azure Active Directory or Azure Active Directory (B2C).

- Select Next: Configuration to move on to the Configuration tab.

- On the Configuration tab, enter the following information: ![image](https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/media/active-directory-access-create-new-tenant/azure-ad-create-new-tenant.png)


- Type your desired Organization name (for example Contoso Organization) into the Organization name box.

- Type your desired Initial domain name (for example Contosoorg) into the Initial domain name box.

- Select your desired Country/Region or leave the United States option in the Country or region box.

- Select Next: Review + Create. Review the information you entered and if the information is correct, select create.

Your new tenant is created with the domain contoso.onmicrosoft.com.

## Adding custom domain to Azure AD

- Sign in to the Azure portal using a Global administrator account for the directory.

- Search for and select Azure Active Directory from any page. Then select Custom domain names > Add custom domain. ![image](https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/media/add-custom-domain/add-custom-domain.png)

- In Custom domain name, enter your organization's new name, in this example, contoso.com. Select Add domain. ![image](https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/media/add-custom-domain/add-custom-domain-blade.png)

The unverified domain is added. The contoso.com page appears showing your DNS information. Save this information. You need it later to create a TXT record to configure DNS.

![image](https://learn.microsoft.com/en-us/azure/active-directory/fundamentals/media/add-custom-domain/contoso-blade-with-dns-info.png)


## What is identity and access management (IAM)?

Identity and access management ensures that the right people, machines, and software components get access to the right resources at the right time. First, the person, machine, or software component proves they're who or what they claim to be. Then, the person, machine, or software component is allowed or denied access to or use of certain resources.

Here are some fundamental concepts to help you understand identity and access management:

### Identity
A digital identity is a collection of unique identifiers or attributes that represent a human, software component, machine, asset, or resource in a computer system. An identifier can be:

- An email address
- Sign-in credentials (username/password)
- Bank account number
- Government issued ID
- MAC address or IP address
- Identities are used to authenticate and authorize access to resources, communicate with other humans, conduct transactions, and other purposes.

At a high level, there are three types of identities:

- Human identities represent people such as employees (internal workers and front line workers) and external users (customers, consultants, vendors, and partners).
- Workload identities represent software workloads such as an application, service, script, or container.
- Device identities represent devices such as desktop computers, mobile phones, IoT sensors, and IoT managed devices. Device identities are distinct from human identities.

### Authentication
Authentication is the process of challenging a person, software component, or hardware device for credentials in order to verify their identity, or prove they're who or what they claim to be. Authentication typically requires the use of credentials (like username and password, fingerprints, certificates, or one-time passcodes). Authentication is sometimes shortened to AuthN.

Multi-factor authentication (MFA) is a security measure that requires users to provide more than one piece of evidence to verify their identities, such as:

- Something they know, for example a password.
- Something they have, like a badge or security token.
- Something they are, like a biometric (fingerprint or face).

Single sign-on (SSO) allows users to authenticate their identity once and then later silently authenticate when accessing various resources that rely on the same identity. Once authenticated, the IAM system acts as the source of identity truth for the other resources available to the user. It removes the need for signing on to multiple, separate target systems.

### Authorization
Authorization validates that the user, machine, or software component has been granted access to certain resources. Authorization is sometimes shortened to AuthZ.


## What does IAM do?
IAM systems typically provide the following core functionality:

- **Identity management** - The process of creating, storing, and managing identity information. Identity providers (IdP) are software solutions that are used to track and manage user identities, as well as the permissions and access levels associated with those identities.

- **Identity federation** - You can allow users who already have passwords elsewhere (for example, in your enterprise network or with an internet or social identity provider) to get access to your system.

- **Provisioning and deprovisioning of users** - The process of creating and managing user accounts, which includes specifying which users have access to which resources, and assigning permissions and access levels.

- **Authentication of users** - Authenticate a user, machine, or software component by confirming that they're who or what they say they are. You can add multi-factor authentication (MFA) for individual users for extra security or single sign-on (SSO) to allow users to authenticate their identity with one portal instead of many different resources.

- **Authorization of users** - Authorization ensures a user is granted the exact level and type of access to a tool that they're entitled to. Users can also be portioned into groups or roles so large cohorts of users can be granted the same privileges.

- **Access control** - The process of determining who or what has access to which resources. This includes defining user roles and permissions, as well as setting up authentication and authorization mechanisms. Access controls regulate access to systems and data.

- **Reports and monitoring** - Generate reports after actions taken on the platform (like sign-in time, systems accessed, and type of authentication) to ensure compliance and assess security risks. Gain insights into the security and usage patterns of your environment.

