# SQL Direct

## Objetivo
Connect to this PostgreSQL server and find the flag!

Additional details will be available after launching your challenge instance.

## Solución
```
┌──(emgeek㉿EmGeek-Kali-PC)-[~/Documents/pruebasHacking]  
└─$ psql -h saturn.picoctf.net -p 52282 -U postgres pico  
Password for user postgres:    
psql (15.4 (Debian 15.4-3), server 15.2 (Debian 15.2-1.pgdg110+1))  
Type "help" for help.  
  
pico=# \c pico  
psql (15.4 (Debian 15.4-3), server 15.2 (Debian 15.2-1.pgdg110+1))  
You are now connected to database "pico" as user "postgres".  
pico=# \dt  
        List of relations  
Schema | Name  | Type  |  Owner      
--------+-------+-------+----------  
public | flags | table | postgres  
(1 row)  
  
pico=# SELECT * FROM flags  
pico-# SELECT * FROM flags;  
ERROR:  syntax error at or near "SELECT"  
LINE 2: SELECT * FROM flags;  
       ^  
pico=# select * from flags;  
id | firstname | lastname  |                address                    
----+-----------+-----------+----------------------------------------  
 1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}  
 2 | Leia      | Organa    | Alderaan  
 3 | Han       | Solo      | Corellia  
(3 rows)  
  
pico=#
```