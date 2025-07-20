# Employee_Onboarding
Automating Employee Onboarding with Power Automate
# 🎯 Employee Onboarding Automation using Power Automate

This project automates the employee onboarding process using **Power Automate**, **Microsoft Forms**, and **Entra ID (Azure AD)**. It streamlines user creation, access provisioning, and email notifications to deliver a seamless onboarding experience.

---
## 🚀 Flow Overview

This Power Automate flow is designed to automate the end-to-end process of onboarding new employees using Microsoft 365, Entra ID (Azure AD), and business system integrations. It reduces manual tasks, enforces consistent provisioning practices, and improves communication between departments (HR, IT, and Managers).

🎯 **Key Benefits**
Benefit	Description

✅ Time-Saving	Automates repetitive tasks like user creation, group assignment, license allocation, and email notifications.

✅ Error Reduction	Eliminates manual data entry errors by pulling structured data directly from Microsoft Forms.

✅ Scalable	Supports dynamic group and license assignment for any number of business units or job roles.

✅ Secure	Ensures best practices by integrating with Entra ID (Azure AD) for access control and provisioning.

✅ Consistent Communication	Automatically notifies managers and stakeholders with personalized onboarding info.

✅ Extensible	Includes logic to trigger business system configurations or helpdesk tickets (like ITSM or Ninja).

---

## 🛠️ Technologies & Connectors Used

- **Power Automate**
- **Microsoft Forms**
- **Entra ID (Azure Active Directory)**
- **Outlook (Email Notifications)**
- **Office 365 Users**
- **Custom Connectors / HTTP (for Helpdesk Ticketing)**

---

## 🔄 Flow Steps Breakdown

1. **Trigger on Form Submission**
   Uses Microsoft Forms to collect onboarding information (e.g., name, department, job role, manager).
   The flow is triggered when a response is submitted.

2. **Initialize Core User Details**
   Generate secure password for the new user.
   Set nickname and prepare group logic using variables and expressions.

3. **Get Group Membership Logic**
   Dynamically checks existing Microsoft 365 / Entra ID groups to:
   Distinguish distribution groups vs. security groups.
   Avoid dynamic groups (read-only).
   Filter and map applicable groups for the user.

4. **Create the User in Entra ID**
   Creates the user with key attributes including:
   Display Name, UPN, Department, Job Title.
   Initial password setup.

5. **Assign Organizational Attributes**
   Assigns:Manager (from Form)
   Licenses (via Graph API or built-in connector)
   Groups based on role/business unit

6. **Send Notifications**
   Sends an email to the manager/HR notifying that the user has been created successfully and is being provisioned.

7. **Add to Business Applications**
   Uses a Loop + Switch block to configure the user in appropriate business systems (e.g., Ninja, ERP, CRM).
   Optional: Generates a helpdesk ticket for manual configuration steps.

8. **Send Welcome Email to the Employee**

Final step: Sends a customized welcome email to the new user with relevant links, credentials, or onboarding documents and instructions on how to set up Microsoft authenticator.

---

## 📎 Screenshots

Flow diagram:  
<img width="1090" height="2184" alt="merged_power_automate_flow_v2" src="https://github.com/user-attachments/assets/49a8081c-62b5-40db-bedd-cb5e21e63f9e" />

---

## 📬 Future Enhancements

- Integrate with **SharePoint** to store onboarding documents.
- Use **Power Apps** to improve the input UI.
- Log each step to a **Dataverse** table or **Excel Online** for tracking.

---

## 📝 License

| Component                     | License Required                        |
| ----------------------------- | --------------------------------------- |
| Power Automate Flow           | Power Automate Per User / Per Flow Plan |
| Microsoft Forms               | Microsoft 365 License                   |
| Azure AD / Entra ID           | M365 E3/E5 or Azure AD Premium P1/P2    |
| Outlook (Send Email)          | Microsoft 365 License                   |
| Premium Connectors (HTTP, AD) | Power Automate Premium                  |

---

## 🙋‍♂️ Author

**Aniket Posture**  
https://www.linkedin.com/in/aniket-posture-b08175119/

