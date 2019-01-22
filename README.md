En el ejercicio SQL INYECTION de DVWA, se tiene el código inicial(SQL-INYECTION-INICIAL.txt)


Dentro de User ID, permite realizar la consulta dando como resultado nombre y apellido del usuario:


![image](https://user-images.githubusercontent.com/46895869/51506909-94dbca00-1dbc-11e9-84ac-d30bc00020fb.png)

Luego de ello, unimos la consulta, dando en la parte inferior el HASH del password de dicho usuario:


1' OR 1=1 UNION SELECT user,password from users#


![image](https://user-images.githubusercontent.com/46895869/51506994-bb016a00-1dbc-11e9-96b7-e6d6dfc5caf9.png)


Para corregir, utilizamos mysqli_real_escape_string llamando a Mysql anteponiendo “\”. Además, utilizamos las opciones de entrada específicas:


![image](https://user-images.githubusercontent.com/46895869/51507034-e7b58180-1dbc-11e9-8146-5de69f496a34.png)


Da como resultado el ID seleccionado:



