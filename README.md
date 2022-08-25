# MySQL-performance-comarison-between-disable-and-enable-foreign_key_checks-and-unique_checks
# In the high traffic MySQL replication topoloty, always facing a painful problem: Replication Lag. 
# replica can't catch up the progress of source.
# Absolutely, change innodb_flush_log_at_trx_commit and sync_binlog can significantly improve the performance. 
# But these changes sacrifice data persistency, once corruption or abnormal shutdown happened, replica lost data.
# There is another way to improve the performance in replica, not sacrifice data persistency.
# Disable foreigh_key_checks and unique_checks in replica.
# performace_schema.data_locks indicates the transaction does foreigh_key_checks and unique_checks, so when there are some constraints, it will nagetive affect the performance.
