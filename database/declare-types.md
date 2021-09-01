# Declare Types

{% embed url="https://docs.microsoft.com/en-us/sql/t-sql/data-types/data-types-transact-sql?view=sql-server-ver15" %}

```sql
DECLARE @Id uniqueidentifier='31D83745-2825-41D4-B82D-000E5DBA0976';
DECLARE @Name varchar(20)='Deybson Ferreira';
DECLARE @TodayDate Date='2021-09-01 00:00:00.000';
DECLARE @YEAR INT =2021



print(@Id) --result 31D83745-2825-41D4-B82D-000E5DBA0976
print(@Name) --result Deybson Ferreira
print(@TodayDate) --result 2021-09-01
print(@YEAR) --result 2021
```

