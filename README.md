# Configuración en DBeaver

>[!NOTE]
>los Username se pueden modificar desde el ``docker-compose.yml``

**POSTGRES**: El password que pongas en ``DBeaver`` de ser igual al ``PG13_PASSWORD`` del ``.env``

**MYSQL**: El password que pongas en ``DBeaver`` de ser igual al ``MYSQL_PASSWORD`` del ``.env``. Adcional a esto en ``DBeaver`` debe ir a la pestaña **Driver properties** y modificar los siguiente:

| Nombre | Valor |
|--------|-------|
| allowPublicKeyRetrieval | TRUE |
| useSSL | FALSE |


**ORACLE 18C**: El password que pongas en ``DBeaver`` de ser igual al ``ORACLE_PASSWORD`` del ``.env``

## Comandos para acceder a los CLI de las bases de datos

**POSTGRES**: docker exec -it postgres13 psql -U admin -d testpostgres

**MYSQL**: docker exec -it mysql8 mysql -u admin -p

**ORACLE 18C**: docker exec -it oracle18 sqlplus system/oracle123@XEPDB1
