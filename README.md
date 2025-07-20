# Employee_Onboarding
Automating Employee Onboarding with Power Automate
# 🎯 Employee Onboarding Automation using Power Automate

This project automates the employee onboarding process using **Power Automate**, **Microsoft Forms**, and **Entra ID (Azure AD)**. It streamlines user creation, access provisioning, and email notifications to deliver a seamless onboarding experience.

---

## 🚀 Flow Overview

The Power Automate flow is triggered when a new employee response is submitted via a Microsoft Form. The automation then proceeds through several stages including account creation, group assignment, application provisioning, and sending emails.



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

### 1. **Trigger**: New form response submitted  
### 2. **Retrieve response details**
### 3. **Generate random password**
### 4. **Set mail nickname**
### 5. **Initialize distribution groups array**
### 6. **Get Manager details from form**
### 7. **Create user in Azure AD**
### 8. **Assign manager to user**
### 9. **Assign license**
### 10. **Notify HR Manager via email**
### 11. **Delay for processing**
### 12. **Update user details (Title, Dept, Mobile)**
### 13. **Get groups of a mirror user**
### 14. **Loop through groups and replicate memberships**
### 15. **Add user to Distribution Groups (if not already)**
### 16. **Parse business application access**
### 17. **Handle app-specific provisioning (Switch logic)**
### 18. **Create helpdesk ticket with user details**
### 19. **Wait until start date**
### 20. **Send welcome email with MFA setup instructions**

---

## 📎 Screenshots

Flow diagram:  
![Flow Diagram](flow-diagram/merged_flow.png)

---

## 📬 Future Enhancements

- Integrate with **SharePoint** to store onboarding documents.
- Use **Power Apps** to improve the input UI.
- Log each step to a **Dataverse** table or **Excel Online** for tracking.

---

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🙋‍♂️ Author

**Your Name**  
[LinkedIn](https://www.linkedin.com/in/your-profile)  
