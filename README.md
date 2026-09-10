# practica-1-hash-table
1. lenguaje utilizado; Phyton, JUpyter notebook
2. instrucciones para ejecutar el programa; "practica-1-hash-table\src/práctica_1_tabla_hash_myp_IMPLEMENTACIÓN.py"
3. explicación de cómo ejecutar los casos de prueba; "practica-1-hash-table\tests\práctica_1_tabla_hash_myp_PRUEBAS.py"
4. explicación de la función hash; Sea $K$ el conjunto de las *keys* posibles y sea $m$ el número de posiciones de la tabla o tamaño. Usaremos una función de dispersión $h$, también llamada función Hash, así sea $k\in K$, el valor $h(k)$ indicará su posición inicial o *cubeta*.
$$h:K→ \{0,1,\ldots,m-1\}$$
Considerando *keys* enteras, tendremos la función didáctica
$$h(k)=k mod(m)$$
Donde nuestro residuo estrá entre $\{0,1,\ldots,m-1\}$
5. explicación del manejo de colisiones; Podemos usar dos métodos:
*Hashing Cerrado:* Busca la siguiente posición disponible en el arreglo mediante sondeo lineal o cuadrático.
*Hashing Abierto:* Utiliza listas enlazadas para almacenar múltiples elementos en la misma posición del arreglo, también llamado Encadenamiento.
Usaremos la segunda opción.
6. explicación de qué ocurre cuando dos llaves producen el mismo hash; Cada posición funciona como una *"cubeta"* que contiene una colección de elemntos. Si varias *keys* tienen el mismo valor de dispersión $(j(k_1)=h(k_2)=h(k_3))$, entonces se almacenan juntas en la posición correspondiente:
$$T[h(k_1)]⟶ k_1 ⟶ k_2 ⟶ k_3$$
7. explicación de qué ocurre cuando varias llaves caen en la misma cubeta; Se "encadenan" es decir, se almacenan juntas en la misma cubeta
8. factor de carga final obtenido durante sus pruebas. 0.57
