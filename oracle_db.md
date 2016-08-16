# Oracle DB

- If you wish to gain access to a database instance via SQLDeveloper and don't know what to use for "Service Name", try to find "tnsnames.ora" on the database instance
- Script to check oracle status: /etc/init.d/oracle status
- Oracle command scripts: $ORACLE_HOME/bin
- Command to control TNS listener: LSNRCTL start/stop/status
- How to get clean output from a prepared query made via sqlplus:
    1. SET PAGESIZE 0
    2. SET FEEDBACK OFF
    3. SET VERIFY OFF
    4. SET TRIMSPOOL ON
    5. SPOOL {name of output file}
    Final output will have no column name, no extra messages, just plain data
- dgmgrl: Used for DataGuard architecture. If the dgmgrl service is not running on the databases or the observer, there may be split brain
- Placeholders in .sql files: &{param number}. e.g. select * from table where id = &1; >> sample.sql , sqlplus user/pass@database @sample.sql 1001 >> sample.sh