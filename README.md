# Configuración en DBeaver

>[!NOTE]
>los Username se pueden modificar desde el ``docker-compose.yml``
>Ademas en todos las configuraciones de debe hacer **Test Connection** e instalar los driver que solicita ``DBeaver``

# **POSTGRES**

El password que pongas en ``DBeaver`` de ser igual al ``PG13_PASSWORD`` del ``.env``

<img width="857" height="699" alt="image" src="https://github.com/user-attachments/assets/769f71f5-0a96-47ba-84e6-d7eb6fdcf74b" />

----

#**MYSQL**

 El password que pongas en ``DBeaver`` de ser igual al ``MYSQL_PASSWORD`` del ``.env``. Adcional a esto en ``DBeaver`` debe ir a la pestaña **Driver properties** y modificar los siguiente:

| Nombre | Valor |
|--------|-------|
| allowPublicKeyRetrieval | TRUE |
| useSSL | FALSE |

<img width="856" height="693" alt="image" src="https://github.com/user-attachments/assets/08c2fc6e-ef26-46e5-984c-2a5e806943c2" />

----

# **ORACLE 18C**

El password que pongas en ``DBeaver`` de ser igual al ``ORACLE_PASSWORD`` del ``.env``

<img width="861" height="699" alt="image" src="https://github.com/user-attachments/assets/247363fd-04bf-4119-9f0c-c37ffa0185e2" />

## Comandos para acceder a los CLI de las bases de datos
| Base de datos | Comando |
| ---- | ---- |
| **POSTGRES** | docker exec -it postgres13 psql -U admin -d testpostgres |
| **MYSQL** | docker exec -it mysql8 mysql -u admin -p |
| **ORACLE 18C** | docker exec -it oracle18 sqlplus system/oracle123@XEPDB1 |
