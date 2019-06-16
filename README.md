# SQLSERVER
identified blocks tables on SQL Server 
select
  object_name(resource_associated_entity_id) as 'TableName' ,*
from
  sys.dm_tran_locks
where resource_type = 'OBJECT'
  and resource_database_id = DB_ID()
GO    
