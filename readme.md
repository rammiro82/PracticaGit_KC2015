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


	~~~
	Roses are red, 
	Violets are blue. 
	All of my base 
	are belong to you.
	~~~

	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/002.png)

3. Añadir poem.md al staging area
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/003.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/004.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/005.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/005.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/006.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/008.png)

	~~~
	Violets are #0000ff. 
	All of my base
	~~~

	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/009.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/010.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/011.png)

12. Rehacer el último commit (el que acabamos de deshacer).
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/012.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/013.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/014.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/015.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/016.png)

	~~~
	Red pills are red, 
	Blue pills are blue. 
	All of my base 
	are belong to you.
	~~~

	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/017.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/018.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/019_.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/020.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/021.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/022.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/023.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/024.png)
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/025_1.png)
	
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/025_2.png)
	![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/026.png)

27. Deshacer el merge (sin perder los cambios del working copy.
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/027.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/028.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/029.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/030.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/031.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/032.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/033.png)

	~~~
	html_matrix: merge de html y matrix (paso 19) a7523eb
	title: modificación del paso 30 aa00924
	~~~

	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/034.png)
	 ![Sin titulo](https://raw.githubusercontent.com/rammiro82/KeepCoding/master/Git/img_temp/035.png) 