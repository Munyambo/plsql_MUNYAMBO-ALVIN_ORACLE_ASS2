# plsql_Oracle_AssignmentII

# OVERVIEW OF TASKS

Task 1: Create a New Pluggable Database (PDB)
   - Created a PDB named following instuction : `am_plsql_27146`.
   - Created a user `alvin_plsqlauca_27146` with DBA privileges inside the new PDB.
   - Used a simple password for demonstration purposes.
     
Task 2: Create and Delete a PDB
   - Created another PDB named `am_to_delete_pdb_27146`.
   - Verified it opened successfully, then deleted it with:
     sql
     ( DROP PLUGGABLE DATABASE <am_plsql_27146> INCLUDING DATAFILES; )

Task 3: Oracle Enterprise Manager (OEM)
   - Configured OEM and logged in using C##ALVIN to verify PDBs.
   - Verified PDBs are visible on the OEM dashboard.
   - Captured screenshot showing created PDBs and my username.

# NOTES ON CHALLENGES

   I. OEM Login Issue
- Attempted to log into OEM with my custom PDB user, but received *“Invalid Database Credentials.”*
- PROBLEM:  OEM requires either SYS/SYSTEM or a Common user (C##) with DBA and monitoring privileges.
- SOLUTION:  Created a `C##` user (C##ALVIN) at the container level with necessary privileges and used it to log in.

 II. HTTP Access Issue
- OEM initially did not open at `https://localhost:5500/em`.
- PROBLEM:  Oracle Enterprise Manager service was not securely started or protected .
- SOLUTION: I changed the http and https port to 8080 and 8443 so that i can access the oem, and i accessed it but without being secured but it's fine because no one can access in that traffic. `https://localhost:8443/em`

  # CONCLUSION
 
- Successfully created and deleted PDBs.
- Configured OEM and resolved login and HTTP issues.
- OEM dashboard now shows my databases and username clearly.



     
