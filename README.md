# Lab-2-Domain-join-Windows-10-to-Active-Directory-
Connecting windows 10 to active directory

Goal- connect Windows 10 pro client to active directory Domain controller 
Steps performed

1. **Configured Domain Controller**
   - Installed *Active Directory Domain Services*.
   - Promoted server to domain controller for `solvexlab.local`.
   - Verified DNS and DHCP were functional.

2. **Prepared Windows 10 Client**
   - Installed **Windows 10 Pro** (Home edition cannot join domains).
   - Set a **static IP (192.168.1.20)** and pointed **DNS → 192.168.1.10**.
   - Verified network connectivity with:
     ```cmd
     ping lab-dc01
     ping lab-dc01.solvexlab.local
     ```

3. **Joined the Domain**
   - Opened `sysdm.cpl` → *Change Settings* → *Domain:* **solvexlab.local**
   - Authenticated using domain admin: `SOLVEXLAB\Administrator`
   - Restarted after “Welcome to the solvexlab.local domain!”

4. **Verified Success**
   - Logged into client as domain user: `SOLVEXLAB\user01`
   - Confirmed in **Active Directory Users and Computers** → *Computers* folder:
     ```
     CLIENT-01
     ```
   - Domain authentication and DNS resolution confirmed.<img width="1920" height="1009" alt="LAB server  Running  - Oracle VirtualBox 11_10_2025 10_27_34 PM" src="https://github.com/user-attachments/assets/4666d611-371e-4815-b447-ec5b31e4205c" />
<img width="1920" height="1009" alt="window lab 10 redu  Running  - Oracle VirtualBox 11_10_2025 10_05_03 PM" src="https://github.com/user-attachments/assets/4ba828c4-035c-4055-be06-270f6d258e86" />
<img width="1920" height="1009" alt="window lab 10 redu  Running  - Oracle VirtualBox 11_10_2025 10_03_50 PM" src="https://github.com/user-attachments/assets/110fd826-b3bf-440c-8ace-e7be22be94f4" />
