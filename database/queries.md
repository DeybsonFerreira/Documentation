# Queries

## Tabela Temporária

```sql
create table #People (PersonId uniqueidentifier)
insert into #People (PersonId) 
select PersonId from person where FullName like '%joão%' --outra tabela

select * from #People

drop table #People --Obs: sempre remover tabela temporária (fim)

```

## Declare Types

{% embed url="https://docs.microsoft.com/en-us/sql/t-sql/data-types/data-types-transact-sql?view=sql-server-ver15" %}



