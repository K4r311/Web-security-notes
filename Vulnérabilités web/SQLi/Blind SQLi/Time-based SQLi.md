
Ces  injections SQL utilisent le temps comme repère, tel leur nom indique. Les time-based SQLi utilisent la méthode SLEEP() de SQL pour avoir un écart entre les résultats positifs et cceux négatifs.
Par exemple:
```SQL
select * from 'target_table' where domain='target_user' UNION SELECT SLEEP(5),2;--' LIMIT 1
```
