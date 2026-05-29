# Práctica Taller Git — Práctica 2

> **Objetivo:** Trabajar con un proyecto HTML y un repositorio local, documentando cada paso con sus comandos y resultados.

---

## Parte 1 — Repositorio local con proyecto HTML

### 1. Crear la carpeta e inicializar el repositorio

Creamos la carpeta `practica-taller-git` y dentro inicializamos el repositorio Git con el siguiente comando:

```bash
git init
```

<img width="1295" height="166" alt="git init" src="https://github.com/user-attachments/assets/ad9701a0-cb42-4baa-b6d7-9d8edf60cedb" />

---

### 2. Crear el fichero index.html

Se crea un archivo HTML básico como punto de entrada del proyecto.

<img width="1417" height="329" alt="index.html creado" src="https://github.com/user-attachments/assets/5ae9568c-002e-43dc-9464-ba8c85981ab1" />

---

### 3. Comprobar que Git detectó el cambio

```bash
git status
```

Git muestra el archivo `index.html` como **untracked**, lo que indica que el archivo existe en el directorio de trabajo pero todavía no está siendo rastreado por el repositorio.

<img width="970" height="328" alt="git status - untracked" src="https://github.com/user-attachments/assets/8adf4e38-1e1f-4f74-874b-12d1dd481968" />

---

### 4. Añadir el fichero al área de staging

```bash
git add index.html
```

Este comando mueve `index.html` al área de staging, preparando el archivo para ser incluido en el próximo commit.

<img width="1069" height="94" alt="git add index.html" src="https://github.com/user-attachments/assets/a890041c-948d-4a0f-b205-220b743c5fe0" />

---

### 5. Confirmar los cambios

```bash
git commit -m "added index file"
```

Se guarda la primera instantánea del proyecto en el historial local del repositorio.

<img width="926" height="114" alt="primer commit" src="https://github.com/user-attachments/assets/39e38a2e-0f27-4b0d-bf99-a3fb10149e41" />

---

### 6. Añadir description.html y modificar index.html

Se crea el archivo `description.html` y se realizan modificaciones sobre `index.html` para ampliar el contenido del proyecto.

<img width="1476" height="889" alt="description.html y cambios en index" src="https://github.com/user-attachments/assets/984103e7-de68-4d28-8c5a-e94970746bb7" />

---

### 7. Comprobar los cambios detectados

#### git status

```bash
git status
```

- `description.html` aparece como **untracked**: archivo nuevo que Git no rastrea aún.
- `index.html` aparece como **modified**: archivo ya registrado en el repositorio que ha sido editado.

<img width="929" height="249" alt="git status con dos cambios" src="https://github.com/user-attachments/assets/7325159b-a97d-45fc-9258-20e858e3c506" />

#### git diff

```bash
git diff
```

Muestra el detalle línea a línea de las modificaciones realizadas. Las líneas precedidas por `-` en rojo corresponden al contenido eliminado, y las precedidas por `+` en verde al contenido añadido.

<img width="919" height="554" alt="git diff mostrando cambios" src="https://github.com/user-attachments/assets/543f8db3-6b27-4c76-b110-67864eb0e911" />

---

### 8. Crear el fichero TODO.txt

Se crea un archivo `TODO.txt` destinado a registrar tareas personales pendientes.

<img width="371" height="128" alt="TODO.txt creado" src="https://github.com/user-attachments/assets/83ee4a14-6f8c-4005-b814-819ff20019d8" />

Git detecta el nuevo archivo al ejecutar `git status`:

```bash
git status
```

<img width="857" height="262" alt="git status detecta TODO.txt" src="https://github.com/user-attachments/assets/fc65f387-842b-4d1b-9e58-04536d1f78bc" />

---

### 9. Ignorar el fichero TODO.txt con .gitignore

Dado que `TODO.txt` contiene anotaciones personales que no deben formar parte del proyecto, se crea un archivo `.gitignore` incluyendo dicho fichero para que Git lo excluya del seguimiento.

<img width="778" height="169" alt=".gitignore creado" src="https://github.com/user-attachments/assets/5779554f-99dc-4edc-8462-7ee78f7ec87f" />

Al volver a comprobar el estado del repositorio, `TODO.txt` ya no aparece como archivo detectado. En su lugar, Git muestra el nuevo `.gitignore` como archivo pendiente de añadir.

```bash
git status
```

<img width="784" height="233" alt="git status sin TODO.txt" src="https://github.com/user-attachments/assets/496297b0-8197-477c-887d-eda41272921e" />

---

### 10. Confirmar el .gitignore

```bash
git add .gitignore
git commit -m "add gitignore"
```

---

## Parte 2 — Fork del repositorio del profesor

### 1. Realizar el fork

Desde la plataforma GitHub se accede al repositorio del profesor en la siguiente dirección:
`https://github.com/lalobarri/git-practica-2`

Se pulsa el botón **Fork** en la parte superior derecha para generar una copia del repositorio en la cuenta personal.

<img width="1848" height="979" alt="fork del repositorio" src="https://github.com/user-attachments/assets/553d8909-ac85-49a6-ae58-90237e386203" />

---

### 2. Clonar el repositorio

En una carpeta distinta a `practica-taller-git`, se clona el repositorio forkeado con el siguiente comando:

```bash
git clone https://github.com/[tu-nombre-de-usuario]/git-practica-2.git
```

<img width="1071" height="208" alt="git clone" src="https://github.com/user-attachments/assets/66d921df-6602-4a3c-8ee5-913298ebd7cb" />

---

### 3. Crear y subir el archivo personal

Se crea un nuevo archivo con el nombre de usuario como identificador, se edita con el contenido deseado y se sube al repositorio remoto.

```bash
git add [tu-nombre-de-usuario].html
git commit -m "add personal page"
git push
```

<img width="1573" height="752" alt="archivo personal creado" src="https://github.com/user-attachments/assets/2e7b1748-543c-4438-98ff-4db3bb2c09e4" />

<img width="1058" height="384" alt="git push del archivo personal" src="https://github.com/user-attachments/assets/54426a7a-1429-4ea4-a6a8-410d2ceca7fe" />

---

### 4. Crear la rama develop

```bash
git checkout -b develop
```

<img width="952" height="51" alt="creación rama develop" src="https://github.com/user-attachments/assets/095be40a-0a58-41b0-8732-a51890cf1193" />

Se realizan cambios en el proyecto, se confirman y se suben a la rama remota:

```bash
git status
git add .
git commit -m "changes from develop branch"
git push origin develop
```

<img width="1077" height="612" alt="push de la rama develop" src="https://github.com/user-attachments/assets/9c641e79-6ce7-44b9-8c18-145a78d5b447" />

---

### 5. Pull Request y fusión

Desde GitHub se crea un **Pull Request** de la rama `develop` hacia `main`. Al no existir conflictos, se procede a fusionar ambas ramas directamente desde la plataforma.

<img width="1717" height="849" alt="creación del pull request" src="https://github.com/user-attachments/assets/f4a65731-d164-4a41-8221-46e7799091d4" />

<img width="1781" height="981" alt="fusión completada" src="https://github.com/user-attachments/assets/20b63053-85d6-4e36-9068-8995e0ae3412" />

---

## Parte 3 — Preguntas y respuestas

---

### Pregunta 1
**¿Qué sucede cuando hacemos un git add?**

> El archivo pasa del directorio de trabajo al área de staging. Git comienza a rastrear esos cambios y los deja preparados para ser incluidos en el próximo commit.

---

### Pregunta 2
**¿Qué sucede cuando hacemos un git commit? ¿Dónde está ese commit?**

> Git crea una instantánea permanente del estado actual de los archivos en staging y la registra en el historial del repositorio local. El commit existe únicamente en la máquina del desarrollador hasta que se sincronice con el repositorio remoto.

---

### Pregunta 3
**¿Por qué al hacer git commit todavía no está disponible ese commit en el repositorio remoto?**

> Porque `git commit` opera exclusivamente sobre el repositorio local. El repositorio remoto es independiente y no recibe cambios de forma automática; es necesario un paso adicional para sincronizarlos.

---

### Pregunta 4
**¿Qué hay que hacer para que veamos este commit en nuestro repositorio remoto de GitHub?**

> Ejecutar `git push`, que transfiere los commits locales al repositorio remoto, haciéndolos visibles en GitHub.

---

### Pregunta 5
**¿Qué diferencia hay entre hacer un fork o crear una nueva rama?**

> Un **fork** genera una copia completa e independiente de un repositorio ajeno dentro de la cuenta propia en GitHub, permitiendo trabajar sin afectar al original. Una **rama** es una línea de desarrollo paralela dentro del mismo repositorio, compartiendo su historial con el resto de ramas del proyecto.

---

### Pregunta 6
**¿Qué comando se utiliza para crear una nueva rama sin cambiarte a ella?**

> Se utiliza el siguiente comando:
> ```bash
> git branch nombre-de-la-rama
> ```

---

### Pregunta 7
**¿Cuál es la diferencia entre los comandos git switch y git checkout al trabajar con ramas?**

> Ambos permiten cambiar de rama. `git checkout` es el comando clásico y tiene un uso más amplio, ya que también permite restaurar archivos a estados anteriores. `git switch` fue introducido en Git 2.23 con el propósito exclusivo de cambiar entre ramas, ofreciendo una sintaxis más clara e intuitiva para esa tarea concreta.

---

### Pregunta 8
**¿Qué es una rama por defecto (como main o master) y por qué es importante?**

> Es la rama principal creada automáticamente al inicializar el repositorio. Representa el estado estable y oficial del proyecto, y es habitualmente la base desde la que se crean el resto de ramas de desarrollo.

---

### Pregunta 9
**¿Qué comando te permite ver la lista de todas las ramas locales de tu repositorio?**

> Se utiliza el siguiente comando:
> ```bash
> git branch
> ```

---

### Pregunta 10
**¿Qué es una rama (branch) y cuál es su beneficio principal al trabajar en un proyecto de software?**

> Una rama es una línea de desarrollo independiente dentro del mismo repositorio. Su principal beneficio es permitir trabajar en nuevas funcionalidades o correcciones de forma aislada, sin comprometer el código estable, y poder integrar los cambios de manera controlada una vez que estén listos mediante un merge.

---

### Pregunta 11
**¿Qué ha pasado con el contenido de la carpeta practica-taller-git? ¿Por qué no la podemos ver en nuestro repositorio remoto de GitHub?**

> La carpeta `practica-taller-git` existe únicamente de forma local, ya que nunca se vinculó a ningún repositorio remoto. Para que su contenido fuera visible en GitHub sería necesario crear un repositorio remoto y ejecutar `git push`. El repositorio clonado `git-practica-2` es completamente independiente de dicha carpeta.

---
