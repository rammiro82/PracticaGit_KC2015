## Entrega Práctica Git ##
*Ramiro García Salazar*

____

1. ¿Qué comando utilizaste en el paso 11? ¿Por qué?
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/011.png)
	- reset --> Permite mover __HEAD__ del repositorio a donde se indique.
	- --hard --> Fuerza al realizar el reset, a deshacer los cambios del __working copy__ y el __stagin area__, se vacía también.
	- HEAD~1 --> Puesto que "sólo" queremos deshacer los cambios realizados en el último commit.

2. ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
	- git reflog --> para tener un histórico de todos los commit's por los que ha pasado el __HEAD__.
	- git reset --hard #HASH# --> Localizando el hash del último comit realizado.
3. El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/013.png)
	No causó ningun conflicto, puesto que:
	
		* cuando se crea la rama __htmlfy__, ésta sale del mismo nodo del que se encontraba la rama __master__.
		* Posteriormente, se modifica el fichero en la rama __htmlfy__.
		* Al hacer el merge, no hay cambios sobre el fichero de la rama __master__, con lo que dichas modificaciones no entran en _conflicto_.
4. El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/019.png)
	Si causa conflicto, porque se han modificado las mismas líneas en ramas distintas.
5. El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/021.png)
	No causa conflicto, porque las líneas con los cambios de la rama htmlfy no están modificadas en la rama master.
6. ¿Qué comando o comandos utilizaste en el paso 25?
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/025_1.png)
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/025_2.png)
7. El merge del paso 26, ¿Podría ser fast forward? ¿Por qué? 
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/026.png)
	Sí que podría haber sido fastforward, puesto que la rama __title__ se crea a partir de la rama __master__. Se modifica el documento en la rama __title__, pero en __master__ no se cambia.
8. ¿Qué comando o comandos utilizaste en el paso 27?
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/027.png)
9. ¿Qué comando o comandos utilizaste en el paso 28? 
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/028.png)
10. ¿Qué comando o comandos utilizaste en el paso 29? 
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/029.png)
11. ¿Qué comando o comandos utilizaste en el paso 30? 
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/030.png)
12. ¿Qué comando o comandos usaste en el paso 32?
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/032.png)
13. ¿Qué comando o comandos usaste en el punto 33?
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/033.png)

***

1. Crear un repositorio.
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/001.png)
2. Crear un archivo “poem.md” con el contenido:

	~~~
	Roses are red, 
	Violets are blue. 
	All of my base 
	are belong to you.
	~~~

	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/002.png)

3. Añadir poem.md al staging area
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/003.png)4. Mover lo que hay en el staging area al repositorio
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/004.png)5. Crear una rama llamada “htmlify”
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/005.png)6. Listar las ramas que hay en el repositorio
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/005.png)7. Moverse a la rama “htmlify”
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/006.png)8. Comprobar que se está en la rama correcta
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/008.png)9. Modificar en el archivo poem.md:

	~~~	La palabra “red” por “#ff0000” y la palabra “blue” por “#0000ff”.	Roses are #ff0000, 
	Violets are #0000ff. 
	All of my base	are belong to you.
	~~~

	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/009.png)10. Añadir los cambios al staging área y luego pasarlos al repositorio.
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/010.png)11. Deshacer el último commit (perdiendo los cambios realizados en el working copy).
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/011.png)

12. Rehacer el último commit (el que acabamos de deshacer).
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/012.png)13. Hacer un merge con ‘master’ (htmlify absorbe a master).
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/013.png)14. Volver a la rama master.
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/014.png)15. Crear una nueva rama llamada “matrix”.
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/015.png)16. Entrar en matrix (cambiar a la rama matrix).
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/016.png)17. Modificar en el archivo poem.md:

	~~~	La palabra “Red” por “Red pills” y la palabra “Violets” por “Blue pills”. 
	Red pills are red, 
	Blue pills are blue. 
	All of my base 
	are belong to you.
	~~~

	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/017.png)18. Hacer un commit.
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/018.png)19. Hacer un merge de “matrix” en “htmlify” (htmlify absorbe a matrix).
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/019_.png)20. Si hay conflictos, deberemos resolverlos quedándonos con el contenido de la rama “htmlify”.
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/020.png)21. Desde “master”, hacer un merge con “htmlify”.
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/021.png)22. Crear una rama “title” y cambiarse a esa rama
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/022.png)23. Añadir un título (a tu gusto) al archivo poem.md y hacer un commit.
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/023.png)24. Volver a la rama master.
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/024.png)25. Dibujar el diagrama.
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/025_1.png)
	
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/025_2.png)26. Hacer un merge “no fast-forward” de “title” en “master” (master absorbe a title).
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/026.png)

27. Deshacer el merge (sin perder los cambios del working copy.
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/027.png)28. Descartar los cambios.
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/028.png)29. Eliminar la rama “title”.
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/029.png)30. Rehacer el merge que hemos deshecho.
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/030.png)31. Volver a master y eliminar el resto de ramas.
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/031.png)32. Volver al commit inicial cuando se creó el poema.
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/032.png)33. Volver al estado final, cuando pusimos título al poema.
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/033.png)34. Crear los siguientes tags:

	~~~	inicial: en el primer commit 124177f	htmlified: modificación del paso 10 86faf9f	matrix: modificación del paso 17-18 97e71a2
	html_matrix: merge de html y matrix (paso 19) a7523eb
	title: modificación del paso 30 aa00924
	~~~

	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/034.png)35. Ir al tag matrix
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/035.png) 