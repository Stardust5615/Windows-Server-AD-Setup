# Windows-Server-AD-Setup
This repository contains a step-by-step guide on setting up an Active Directory environment using Windows Server 2022 in a virtualized environment and adding common features in Active Directory

# Active Directory Lab Setup
This project documents my step-by-step setup of an Active Directory environment using Windows Server 2022 on KVM (Parrot OS).  
It includes domain setup, user and group management, and security policies.  

## Table of Contents  
- [Prerequisites](#prerequisites)  
- [Setting up the Virtual Machine](#setting-up-the-virtual-machine)
- [Adding features and configuring Active Directory](#Adding-features-and-configuring-Active-Directory)
- [Creating Users and Group Policies](#creating-users-and-group-policies)  
- [Troubleshooting](#troubleshooting)  
- [Screenshots](#screenshots)  




## Prerequisites  
- **Host OS**: Parrot OS  (Optional)
- **Hypervisor**: KVM  (Optional)
- **Guest OS**: Windows Server 2022  
- **ISO File**: Downloaded from Microsoft  





## Setting up the Virtual Machine  

1. Open **Virt-Manager** and create a new VM.  
2. Select **Local install media** and attach the Windows Server 2022 ISO.  
3. Allocate at least **4GB RAM** and **2+ CPU cores**.  
4. Configure storage (Recommended: 50GB+).  
5. Set the network to **"Virtual Network - default"**.  
![kvm](https://github.com/user-attachments/assets/3ab25c69-acdc-454d-9a7f-cafb5379d23f)



## Adding necessary features and configuring Active Directory  

1. Open **Add roles and features**.  
2. Select **DNS Server** and **Active Directory Domain Services** and press next.
3. Make sure **Group Policy Management** is selected then press next.
4. Select **Add a new Forest** then name the root domain whatever you want it to be then click next.
5. Create a password for **Directory Services Restore Mode Password** and confirm the password, then click next.
6. Click next until **Install** is available then click Install.
![7](https://github.com/user-attachments/assets/dea3c7db-51a4-46cb-ad1e-515e8466da39)
![6](https://github.com/user-attachments/assets/b9598551-39aa-4f4a-9390-4f225323c85e)
![5](https://github.com/user-attachments/assets/4422f958-650c-44b2-bcde-cab858d955aa)
![4](https://github.com/user-attachments/assets/10e80975-3e01-4217-a5b0-59e8f860d5f7)
![3](https://github.com/user-attachments/assets/ec13b905-cd30-49c4-94f0-f83775393539)
![2](https://github.com/user-attachments/assets/28e4c06d-ddf8-4cc3-9659-3d334e6d6f8f)
![1](https://github.com/user-attachments/assets/2ee246f6-04bf-4410-b1e4-3a032ed6fe0c)


## Creating Users in Active Directory  

1. Open **Active Directory Users and Computers**.  
2. Navigate to **Users** → Right-click → **New** → **User**.  
3. Enter user details (e.g., `JohnDoe`, `johndoe@mydomain.local`).  
4. Set an initial password and enable "User must change password at next login".  
![12](https://github.com/user-attachments/assets/f9ef6a97-fc75-4f95-ada0-c043e4905047)
![11](https://github.com/user-attachments/assets/f3fbcea7-cdb0-4ebe-904f-8397d33ed0de)
![10](https://github.com/user-attachments/assets/d688f615-c425-4a6b-ba4d-476309763e0a)
![9](https://github.com/user-attachments/assets/907c6d71-8067-453b-b33f-cf1e80828dd4)
![8](https://github.com/user-attachments/assets/d484d214-0659-4ac3-85ba-ce38c09b1eca)


## Setting Up Group Policies  

1. Open **Group Policy Management**.  
2. Right-click **Group Policy Objects** → **New**.  
3. Name it (e.g., `Password Policy`).  
4. Right-click the new policy → **Edit**.  
5. Navigate to **Computer Configuration** → **Windows Settings** → **Security Settings**.  
6. Configure settings (e.g., enforce password complexity).  
![21](https://github.com/user-attachments/assets/c5e4ab15-2d96-4acb-ba69-ea6c8c0f95d0)
![20](https://github.com/user-attachments/assets/f1a5c18b-397e-4d94-aaa0-115e15403d6f)
![19](https://github.com/user-attachments/assets/22c5ad5a-8d64-48d4-96fb-4a0d4a8844cf)
![18](https://github.com/user-attachments/assets/d068f0b2-748d-479d-8311-7fc9f5e4a2c1)
![17](https://github.com/user-attachments/assets/a83a739d-a4fb-42e4-b6cb-4d047c947439)
![16](https://github.com/user-attachments/assets/9d55e7a8-4734-463c-8a42-298116cf3060)
![15](https://github.com/user-attachments/assets/f8544b35-9387-4e1d-89b1-76bac90d6fd0)
![14](https://github.com/user-attachments/assets/7ea9b619-a87d-40e1-a63c-807a6a12f308)
![13](https://github.com/user-attachments/assets/7f05df3e-c0aa-4410-b50f-4b07c1cb5ef8)
