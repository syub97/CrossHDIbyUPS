# Cross HDI consume data - User User Provide Service
1. Create a tech user to be used in UPS,  this user may be granted with limited priviledge to only read specific data, or could be greanted bigger priviledge and then set required on grant service when used.
```
CREATE USER <username> PASSWORD <password> SET USERGROUP DEFAULT;
ALTER USER <username> DISABLE PASSWORD LIFETIME;
Grant CS1A_SCHEMA_1.”CS1XHDIO#” to <username> WITH ADMIN option;
Grant CS1A_SCHEMA_1.”CS1XHDIA” to <username> WITH ADMIN option;
```
2. Bind user provide service to target DB, same process as binding another HDI container.
3. create grants to grant authorization.   
SYNCS2ATAB.hdbgrants
4. create synonym   
SYNCS2ATAB.hdbsynonym
5. create synonymconfig when need use dynamic shcema, here only use static schema so synonymconfig is useless.
SYNCS2ATAB.hdbsynonymconfig​


