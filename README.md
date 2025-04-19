# Using-the-Autopsy-retrieve-the-deleted-files

# Name: SHAIK MOHAMMAD SHAHIL
# Reg No: 212223240044
## AIM:
To use Autopsy in Kali Linux to retrieve and analyze deleted files from a disk image.

## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## Virtual Disk Creation & File Recovery using Autopsy 


## Step 1: 
   Create a Virtual Hard Disk (VHD) 

### **1. Open Disk Management**  
- Press **Windows + X** → Click **Disk Management** 

 ![Screenshot 2025-03-20 134041](https://github.com/user-attachments/assets/6ebfb059-a30d-4b57-8a5e-cdb3889573f7)


### **2. Create a New VHD**  
- Click **Action** (top menu) → **Create VHD**.  

![image](https://github.com/user-attachments/assets/b7420503-9719-458a-bda2-97112f0eb95d)


### **3. Choose File Location & Size**  
- Click **Browse** and select where to save the VHD file (e.g, `C:\new VHD.vhd`)
- Set the **size** (e.g: `1GB`) 
- Choose **VHD (Fixed Size)** and Click **OK**

![image](https://github.com/user-attachments/assets/649300cc-e39c-4001-af6a-2aadc0b28dc9)


### **4. Initialize the Disk**  
- In **Disk Management**, find your new disk (marked as "Not Initialized").  

![image](https://github.com/user-attachments/assets/de065bb1-2aa7-45b3-bc62-f9e74010f35d)


- Right-click the disk → Click **Initialize Disk**.
![image](https://github.com/user-attachments/assets/571f382b-bbdc-4f99-8b5d-37af3fdbf4f0)



- Select **MBR (Master Boot Record)**. 

![image](https://github.com/user-attachments/assets/a5da8c50-590c-4c07-bec8-034336982215)


### **6. Create & Format the Partition**  
- Right-click the **Unallocated Space** → Click **New Simple Volume**.  
![image](https://github.com/user-attachments/assets/0b56e23c-f79d-4ef9-be83-c9bcbfc9ca22)
![image](https://github.com/user-attachments/assets/56becbba-aa9c-402f-ba75-1149c04ac322)
![image](https://github.com/user-attachments/assets/7efc0c69-7b38-4fdd-aedb-a434374800e8)



- Click **Next** → **Click on Mount in the following empty NTFS folder** → **Browse** → **Assign a drive letter (e.g., `C: or D:`)** → **New folder** → **OK**

![image](https://github.com/user-attachments/assets/8d90194f-b5de-4769-9040-8c9475daad97)
![image](https://github.com/user-attachments/assets/46a5a80f-4ac3-4b53-b6a2-d511c2d69400)
![image](https://github.com/user-attachments/assets/c8c75b26-10e8-4a75-a7a4-be737721d8f6)


- Click **next** → **Finish**. 

---

## **Step 2: Add & Delete Files for Recovery** 

### **1. Copy Files to the Virtual Disk**  
- Open **File Explorer** → Go to the new drive (`C: or D:`), where the folder created in the previous step
- Create a new folder (`TestFolder`) and copy **images or files** into it.  

### **2. Delete the Files**  
- Select any one or two images → Press **Delete**.  
- Empty the **Recycle Bin** to permanently delete them.  

---

## **Step 3: Recover Deleted Files Using Autopsy**  
### **1. Open Autopsy & Create a New Case** 

- Launch **Autopsy** and **Run as a administrator**  
- Click **Create New Case**.  

![image](https://github.com/user-attachments/assets/d9604c32-f599-47e7-bb37-b7d39b91882b)


- Enter a **Case Name** (e.g., `Autopsy1`).  
- Choose a **Case Folder** location.  
- Click **Next** → Click **Finish**.  

![image](https://github.com/user-attachments/assets/87478c5d-1660-4041-b8f1-e537bcd8cf21)


### **2. Add the Virtual Disk as an Evidence Source**  
- Click **Add Data Source**  → **Select Host**
![image](https://github.com/user-attachments/assets/2cb4fb14-cf0b-460f-ab7e-323badf6b047)



- Select **Local Disk** → **next** 
![image](https://github.com/user-attachments/assets/06ee3022-8273-4943-99d9-d008b3c3a62d)


- Select Disk → **Choose the VHD drive (`Drive1`)**

![image](https://github.com/user-attachments/assets/e91fd4b8-4e77-4d3f-a167-e2cea9e584e9)

- Click **Next** → Keep default settings → Click **Finish**.  
- Wait for Autopsy to process the disk.  

### **3. Recover Deleted Files**  
- Go to **File Views** (left panel).  
![image](https://github.com/user-attachments/assets/91214523-09bc-4b49-a4cc-37a055190b25)



- Click **Deleted Files** → Find your deleted images.  
- Right-click an image → Click **Extract File**.  

![image](https://github.com/user-attachments/assets/8cb20987-9d5b-4b72-8517-520231fcf3de)


- Select a folder to see the recovered files (e.g., `C:\image_recovery`).  

**Your deleted images are now recovered!**  

---

## **Step 4: Delete the Virtual Disk (Optional Cleanup)** 

### **1. Detach the VHD**  
- Open **Disk Management** (`Win + X` → Disk Management).  
- Find the **virtual disk** (`C: or D:`).  
- Right-click the disk (not the partition) → Click **Detach VHD**.  

### **2. Delete the VHD File**  
- Open **File Explorer**.  
- Go to the location where you saved the `.vhd` file (e.g., `C:\new VHD.vhd`).  
- **Delete** the `.vhd` file.  
- Empty the **Recycle Bin**.  

**Your virtual disk is completely removed!**  
# Output:
![424877318-71cd78ae-68f3-468d-8b9a-320d0884532c](https://github.com/user-attachments/assets/0ec4323c-e95b-45a2-86f5-f58d9b7e9b03)


## Recovered Images:



 ![Screenshot 2025-03-22 115222](https://github.com/user-attachments/assets/d7abdbd8-ce13-4d45-acff-af53a404459a)




## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
