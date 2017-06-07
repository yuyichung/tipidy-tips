# Oracle DB

* If you wish to gain access to a database instance via SQLDeveloper and don't know what to use for "Service Name", try to find "tnsnames.ora" on the database instance
* Script to check oracle status: /etc/init.d/oracle status
* Oracle command scripts: $ORACLE\_HOME/bin
* Command to control TNS listener: LSNRCTL start/stop/status
* How to get clean output from a prepared query made via sqlplus:
  1. SET PAGESIZE 0
  2. SET FEEDBACK OFF
  3. SET VERIFY OFF
  4. SET TRIMSPOOL ON
  5. SPOOL {name of output file}
     Final output will have no column name, no extra messages, just plain data
* dgmgrl: Used for DataGuard architecture. If the dgmgrl service is not running on the databases or the observer, there may be split brain
* Placeholders in .sql files: &{param number}. e.g. select \* from table where id = &1; &gt;&gt; sample.sql , sqlplus user/pass@database @sample.sql 1001 &gt;&gt; sample.sh
* Oracle Enterprise Management: [https://{ip}:1158/em](https://{ip}:1158/em)
* Oracle 11.1.0.6 installation in silent mode:
  * Create group oinstall
  * Create user oracle, add oracle to group oinstall
  * Create file /etc/oraInst.loc with the following content:
    * inventory_loc=/desired\_path_/oraInventory
      inst\_group=oinstall
  * Create directory /_desired\_path_/oraInventory, chown oracle:oinstall /desired\_path/\_oraInventory
  * Create the $ORACLE\_HOME directory and chown oracle:oinstall
  * Locate the downloaded files for installation, find the /database folder
  * Copy or edit one of the .response files in /database/response/ depending on the edition to install
  * Execute ./database/runInstaller -silent -responseFile "_path to response file_"



