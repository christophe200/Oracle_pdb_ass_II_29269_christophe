 Oracle PDB Assignment II 

 Student Information
- **Name:** Christophe Rugayampunzi  
- **Student ID:** 29269  
- **Course:** Database Development with PL/SQL (INSY 8311)  
- **Instructor:** Eric Maniraguha  
- **Semester:** 2025/2026  
- **Assignment:** Pluggable Database (PDB) Practical Assessment  

---

 Repository Details
- **Repository Name:** oracle_pdb_ass_II_29269_christophe  
- **Visibility:** Public  

---

**Assignment Objective**
The objective of this assignment is to demonstrate practical understanding of Oracle Multitenant Architecture by performing operations related to Pluggable Databases (PDBs).  
The tasks involved creating, managing, and deleting PDBs, creating users inside a PDB, accessing Oracle Enterprise Manager (OEM), and documenting the work professionally using GitHub.

---

 **Oracle Environment Used**
- **Oracle Database Version:** Oracle 19c  
- **Architecture:** Multitenant Container Database (CDB & PDB)  
- **Tools Used:**
  - SQL*Plus / SQL Developer
  - Oracle Enterprise Manager (OEM)
  - GitHub for documentation and version control

---

**Task 1: Creation of a New Pluggable Database**
**Steps Performed**
1. Connected to the Container Database (CDB) as SYSDBA.
2. Created the pluggable database using the required naming format.
3. Opened the PDB in READ WRITE mode.
4. Saved the state so it opens automatically.
5. Switched session to the created PDB.
6. Created the required user inside the PDB.
7. Granted necessary privileges for future coursework.
![Image AET](https://github.com/christophe200/Oracle_pdb_ass_II_29269_christophe/blob/14303d245aafc783bed205e74f56be176df2927f/plsql/CREATING%20PDB.png)
**Verification**
- Verified PDB creation using `SHOW PDBS`
- Confirmed open mode of the PDB
- Verified user creation using `SELECT username FROM dba_users`

**Evidence**
Screenshots provided in the `screenshots/` folder:
- PDB creation command result
- PDB open state
- User creation with visible username
![Image AET](https://github.com/christophe200/Oracle_pdb_ass_II_29269_christophe/blob/18a203118ed1ba64d8bfa0a5dc9afd8160e2ec77/plsql/CREATING%20USER.png)
---

**Task 2: Create and Delete a Temporary PDB**

**Temporary PDB Naming**
- **Temporary PDB Name:** `ch_to_delete_pdb_29269`

**Steps Performed**
1. Created a temporary PDB successfully.
2. Verified its existence using `SHOW PDBS`.
3. Closed the PDB before deletion.
4. Dropped the PDB including its datafiles.
5. Confirmed that it no longer exists in the system.

**Verification**
- Creation confirmed by listing available PDBs.
- Deletion confirmed by absence from `SHOW PDBS` results.

**Evidence**
Screenshots included:
- Temporary PDB creation
- Temporary PDB deletion
- Confirmation that the PDB no longer exists
![Image AET](https://github.com/christophe200/Oracle_pdb_ass_II_29269_christophe/blob/ede1d043e4b31cfe4101e0a17ccb3d3dd09627c2/plsql/CREATING%20AND%20DELETING%20TEMP%20PDB.png)
---

 **Task 3: Oracle Enterprise Manager (OEM)**

**Configuration and Access**
Oracle Enterprise Manager was successfully accessed through the web interface.

**Dashboard Verification**
The OEM dashboard displayed:
- The Oracle database environment
- The created PDB: `ch_pdb_29269`
- System status and database components

A clear screenshot of the OEM dashboard is included in the `screenshots/` folder.

---

**Challenges Faced and Solutions**

**Challenges Encountered**
Yes, some minor issues were encountered during execution:
- Creating the user before switching to the correct PDB container
- PDB not automatically opening after creation

**Solutions Applied**
- Used the command:
  ```sql
  ALTER SESSION SET CONTAINER = ch_pdb_29269;
before creating the user.

Opened and saved the PDB state using:

ALTER PLUGGABLE DATABASE ch_pdb_29269 OPEN;
ALTER PLUGGABLE DATABASE ch_pdb_29269 SAVE STATE;
These steps resolved all issues successfully.

**Repository Structure**
oracle_pdb_ass_II_29269_christophe/
│── README.md
│── screenshots/
    ├── pdb_creation.png
    ├── pdb_open_state.png
    ├── user_creation.png
    ├── temp_pdb_creation.png
    ├── temp_pdb_deletion.png
    └── oem_dashboard.png
Submission Information
Repository Link: (Paste your GitHub repository URL here)

PDB Name Created: ch_pdb_29269

Issues Encountered: Yes (resolved successfully)

Integrity Statement
I declare that this assignment is my original work.
All commands were executed by me in my Oracle environment, and the screenshots provided are authentic evidence of my practical implementation.

Student Name: Christophe Rugayampunzi
Student ID: 29269
Date: February 2026
