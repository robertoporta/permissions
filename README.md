# <p align="center">
<img width="759" height="472" alt="Folder" src="https://github.com/user-attachments/assets/0bdf2866-e1b4-4a83-a0f4-44cef3908b8e" />
</p>

<h1>Network File Shares and Setting Permissions</h1>
This is an example where I configure network file shares and manage user permissions in a Windows Server environment. This simple simulation shows how access control is applied to shared folders, allowing specific groups or users to read, write, or modify files based on their roles. It demonstrates how proper permission management helps maintain security and organized collaboration within an organization.
</p>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure
- Remote Desktop (RDP)
- Active Directory Domain Services (AD DS)
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)


<h2>Shared Folder Setup and Permission Configuration</h2>

<p>
<img width="1169" height="657" alt="Image" src="https://github.com/user-attachments/assets/f572db55-0b0a-49b2-b49a-d74fedffee08" />  
</p>
<p>
- To start, I create several folders in the Windows (C:) drive that represent different levels of access: read, write, and no access. These folders are used to demonstrate how file permissions work for different users in a network environment. I also create a dedicated marketing folder, which will be used by the users in the Marketers group later in the setup.
</p>
<br>

<p>
<img width="1167" height="657" alt="Image" src="https://github.com/user-attachments/assets/5379dfde-1179-44d6-84fb-c162e8705a7b" />  
</p>
<p>
- Next, I configure the read-access folder. When sharing it, I assign permissions to domain users, allowing them only read access. This means that users within the domain can open and view the files in the folder, but they cannot modify, delete, or create new files. This setting helps protect files that should be visible to everyone but not editable. 
</p>
<br>

<p>
<img width="1166" height="656" alt="Image" src="https://github.com/user-attachments/assets/f941f4c8-bdfa-4de8-8ed8-903006c155e9" />  
</p>
<p>
- I then create a new security group called Marketers within Active Directory Users and Computers. This group represents the marketing team and is used to manage access rights collectively instead of assigning permissions to individual users one by one.  
</p>
<br>

<p>
<img width="1170" height="656" alt="Image" src="https://github.com/user-attachments/assets/4a5425e0-989e-4952-a29c-eaf8ac4e1a2f" />  
</p>
<p>
- Back in the Windows (C:) drive, I configure the marketing folder’s permissions so that the Marketers group has read/write access. This allows users in that group to both open and modify files, meaning they can edit, add, and remove content as needed. This setup reflects how real departments within an organization need shared spaces for collaboration.  
</p>
<br>

<p>
<img width="1166" height="654" alt="Image" src="https://github.com/user-attachments/assets/ff278f41-a1df-4dd5-86e9-91818d5aff4f" />  
</p>
<p>
- Next, I assign one of the domain users to the Marketers group. By doing this, the user automatically inherits all permissions given to the group, in this case the ability to read and write in the Marketing folder. Group-based access control like this helps administrators manage permissions efficiently, especially in large organizations.  
</p>
<br>

<p>
<img width="1168" height="657" alt="Image" src="https://github.com/user-attachments/assets/9588cb51-ce32-4206-9383-04e8e87bdf48" />  
</p>
<p>
- I then log in as the user who was added to the Marketers group. From the user’s perspective, I can now access the shared Marketing folder, confirming that the group permissions are working correctly. The user can open and read files inside the folder without any restrictions. 
</p>
<br>

<p>
<img width="1171" height="656" alt="Image" src="https://github.com/user-attachments/assets/34e9700e-796f-4f8b-bd9b-c6c48242f066" />  
</p>
<p>
To complete the test, I create a new file within the Marketing folder while still logged in as the Marketers user. This confirms that write permissions are functioning properly, as the user is able to add and modify files in the shared folder. This demonstrates how permissions control user access and maintain security in a networked environment.  
</p>
<br>

<br>
