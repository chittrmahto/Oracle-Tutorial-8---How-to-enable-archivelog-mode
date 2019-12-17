# Oracle-Tutorial-8---How-to-enable-archivelog-mode
Oracle Tutorial 8 - How to enable archivelog mode


Steps: ---
Log in as user oracle and enter the following commands:
Open cmd in Windows.

$ export ORACLE_SID=orcl
(if your database is already orcl the no need to export.)
where orcl is the name of the database.

$ sqlplus /nolog
SQL> connect / as sysdba

Check the ARCHIVELOG mode.
SQL> archive log list;

So archivelog is Disabled here. lets flow the below command to enable archivelog mode.


To enable ARCHIVELOG mode status, enter the following SQL commands:

SQL> Shutdown
Database closed.
Database dismounted.
ORACLE instance shut down.

SQL> startup mount
ORACLE instance started.

Total System Global Area 3390558208 bytes
Fixed Size                  2180464 bytes
Variable Size            1996491408 bytes
Database Buffers         1375731712 bytes
Redo Buffers               16154624 bytes
Database mounted.

SQL> Alter database archivelog;
Database altered.

SQL> alter database open;

To check the ARCHIVELOG mode status, enter the following SQL command:
SQL> archive log list;

Database log mode              Archive Mode
Automatic archival             Enabled
Archive destination            USE_DB_RECOVERY_FILE_DEST
Oldest online log sequence     29
Next log sequence to archive   31
Current log sequence           31

So database arhivelog is enabled now.

Video URL : https://chittranjanmahto.blogspot.com/2019/09/oracle-tutorial-8-how-to-enable.html
