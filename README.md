Master Universitario en Desarrollo y Operaciones

##### Entornos de Integración y Entrega Continua

### Actividad grupal

# Pull requests en GitHub 


Integrantes:
- Jorge Luis Tinoco
- Jonathan Jordi
- Daniel Naupari
- Victor Maldonado

##### Objectivo:

El objetivo de esta actividad es aplicar el flujo de GitHub sobre el código del caso práctico. Para ello, uno de los miembros del equipo debe actuar como administrador del repositorio principal, mientras que los demás integrantes del grupo deberán
actuar como desarrolladores individuales, los cuales implementarán una funcionalidad diferente.



##### Uso de la aplicación

La aplicación (`main.py`) lee una lista de palabras desde un fichero de texto (una palabra por línea), opcionalmente elimina las duplicadas y las imprime ordenadas.

Requisitos: Python 3.

```bash
python3 main.py <fichero> <eliminar_duplicados> <orden>
```

| Argumento | Valores | Descripción |
|-----------|---------|-------------|
| `fichero` | ruta a un `.txt` | Fichero con las palabras, una por línea. Si no existe, se usa una lista por defecto. |
| `eliminar_duplicados` | `yes` / `no` | Si es `yes`, elimina las palabras repetidas antes de ordenar. |
| `orden` | `asc` / `desc` | Orden ascendente o descendente. |

##### Ejecución de prueba

Fichero de ejemplo `palabras.txt`:

```
manzana
pera
uva
manzana
banana
kiwi
pera
```

Orden ascendente eliminando duplicados:

```
$ python3 main.py palabras.txt yes asc
 Words of the file palabras.txt will be read
['banana', 'kiwi', 'manzana', 'pera', 'uva']
```

Orden descendente sin eliminar duplicados:

```
$ python3 main.py palabras.txt no desc
 Words of the file palabras.txt will be read
['uva', 'pera', 'pera', 'manzana', 'manzana', 'kiwi', 'banana']
```

Si el fichero no existe, se ordena la lista por defecto:

```
$ python3 main.py noexiste.txt no asc
 Words of the file noexiste.txt will be read
The file noexiste.txt does not exist
['gryffindor', 'hufflepuff', 'ravenclaw', 'slytherin']
```

Si no se indican los tres argumentos, se muestra la ayuda y el programa termina:

```
$ python3 main.py
The file must be indicated as the first argument
The second argument indicates if duplicates should be removed
```
