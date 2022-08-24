# MySQL-performance-comarison-between-disable-and-enable-foreign_key_checks-and-unique_checks
# In the high traffic MySQL replication topoloty, always facing a painful problem: Replication Lag. 
# replica can't catch up the progress of source.
# Absolutely, change innodb_flush_at_trx_method and sync_logbin can improve the performance. 
# But these changes sacrifice data persistency, once corruption or abnormal shutdown, replica lost data.
# There is another way to improve the performance in replica, not sacrifice data persistency.
# Disable foreigh_key_checks and unique_checks in replica.
