# Goal
- Connect the on-prem Active Directory domain to the Microsoft 365 tenant using Azure AD Connect.

---

## Tenant 
- Logged into **Microsoft 365 Admin Center** and confirmed:
  - Tenant Name: `HomeLab`
  - Tenant ID: `06c7d7fd-c2dc-44d2-88cf-a8cf15007283`
  - Primary Domain: `TestHomeLabx.onmicrosoft.com`
  - License: **Microsoft Entra ID P1 (Trial)**

---

## Install and Run Azure AD Connect
- On `DC-1`, downloaded **Azure AD Connect** and launched the installer.
- Entered Microsoft 365 Global Admin credentials.
- Selected the on-premises domain: `Domainname.com`
- Selected specific OUs to sync: `OU=Computers`, `OU=Groups`, `OU=ServiceAccounts`, `OU=Users`
- Continued through prompts and confirmed installation succeeded.

  <img width="457" height="133" alt="bcfaad1c-d562-4cc8-9cb2-e6649057987a" src="https://github.com/user-attachments/assets/ecfb9e75-bf92-43c9-9a32-e15f5911129d" />

---

## Post-Sync Validation
- Checked **Microsoft Entra ID** and verified that synced **on-premises** users, devices, and groups appeared.
  
  <img width="740" height="118" alt="ff8a3244-e2c6-4109-9136-97605c7e7003" src="https://github.com/user-attachments/assets/5947fedb-b04d-46a6-9e37-174369caf701" />

- Confirmed synced user accounts could successfully log into Microsoft 365.
  
  <img width="295" height="129" alt="ac7e83c7-f848-4918-82fc-71f3b398c106" src="https://github.com/user-attachments/assets/268a8eb4-7756-4e1d-8465-e1f84b8c56ab" />

---

## Notes
- Azure AD Connect successfully established synchronization between the on-premises Domain Controller (`DC-1`) and Microsoft Entra ID. Entra ID.
- Environment is now ready for further hybrid cloud configuration and management.
