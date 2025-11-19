# 📘 Proyecto SDAW_9483 – Control de Versiones con Git y GitHub

**Autor:** Peñarrieta  
**Asignatura:** Entornos de Desarrollo (SDAW1)  
**Curso:** 2025/2026

---

## 📝 Descripción breve
Este repositorio contiene una pequeña aplicación web (HTML + JS) y un servidor Node.js básico. El objetivo de la práctica ha sido aprender a usar Git y GitHub en un flujo real: crear ramas, subir cambios, resolver conflictos y documentar todo el proceso.



---

## 📁 Estructura del proyecto

```
SDAW_9483/
│── index.html
│── script.js
│── server.js
│── package.json
│── README.md
│── .gitignore
```

---

## 🚀 Ejecutar el proyecto en local (Node.js)

1. Comprobar versión de Node:
```bash
node -v
```

2. Instalar dependencias (si procede):
```bash
npm install
```

3. Iniciar servidor:
```bash
npm start
```
o directamente:
```bash
node server.js
```

Abrir en el navegador: `http://localhost:3000`

---

## 🛠️ Comandos usados (con explicación breve)
A continuación se listan los comandos clave que utilicé y una frase que explica qué hace cada uno.

### Git — creación y control
```bash
git init -b main
```
Inicializa un repositorio Git y crea la rama principal llamada `main`.

```bash
git config user.name "Peñarrieta"
```
Configura el nombre de usuario que aparecerá en los commits.

```bash
git config user.email "joseiverp@gmail.com"
```
Configura el correo electrónico asociado a los commits (mi dirección real usada en esta práctica).

```bash
git add .
```
Añade todos los cambios al área de preparación (*staging*) para dejarlos listos para el commit.

```bash
git commit -m "mensaje"
```
Crea un commit con el mensaje indicado, guardando los cambios añadidos al staging.

```bash
git remote add origin https://github.com/joseiverp/SDAW_9483.git
```
Vincula el repositorio local con el remoto en GitHub.

```bash
git push -u origin main
```
Sube la rama `main` al remoto y establece el tracking entre `main` local y `origin/main`.

```bash
git checkout -b nombre_rama
```
Crea y cambia a una nueva rama (por ejemplo `rama1_Penarrieta`).

```bash
git checkout nombre_rama
```
Cambia a la rama indicada.

```bash
git branch
```
Muestra las ramas locales disponibles.

```bash
git log --oneline --graph --decorate -n 10
```
Muestra un historial compacto y visual de los últimos commits.

```bash
git pull origin main
```
Trae y fusiona en local los últimos cambios desde `origin/main` (recomendado antes de subir trabajo al main remoto).

```bash
git merge main
```
Fusiona la rama `main` dentro de la rama actual (útil para integrar cambios recientes de `main` y resolver conflictos localmente).

```bash
git push -u origin nombre_rama
```
Sube la rama especificada al remoto y configura el tracking.

### Node / servidor
```bash
npm install
```
Instala dependencias listadas en `package.json` (si existieran).

```bash
npm start
```
Ejecuta el script `start` definido en `package.json` (en este proyecto corre `node server.js`).

```bash
node server.js
```
Lanza directamente el servidor desde el fichero `server.js`.

---

## 🌿 Archivo `.gitignore`
Incluí `.gitignore` con al menos:
```
node_modules/
.env
.DS_Store
```
Esto evita subir dependencias y archivos temporales innecesarios al repositorio.

---

## 🌱 Ramas y cambios principales
- `main` — rama principal.
- `rama1_Penarrieta` — añadí la explicación de los comandos Git al README.
- `rama2_Penarrieta` — añadí la salida de `git log` y gestioné un conflicto en `README.md`.

---

## 🔀 Pull Requests y merges
Se crearon dos Pull Requests y se fusionaron en GitHub:

1. **PR #1**: `rama1_Penarrieta` → `main`  
   - Contenido: documentación sobre comandos en README.

2. **PR #2**: `rama2_Penarrieta` → `main`  
   - Contenido: salida de `git log` y resolución de conflicto manual en `README.md`.

Ambos PR fueron revisados y mergeados desde la interfaz de GitHub. Las ramas se conservaron (no se borraron).

---

## ⚠️ Resolución de conflicto (resumen)
Al fusionar `main` en `rama2_Penarrieta` apareció un conflicto en `README.md` porque ambas ramas modificaban la misma sección. Procedí así:

1. `git checkout rama2_Penarrieta`  
2. `git merge main` → conflicto detectado en `README.md`  
3. Edité `README.md` en VSCode, eliminando las marcas `<<<<<<<`, `=======`, `>>>>>>>` y manteniendo el contenido de ambas ramas.  
4. `git add README.md`  
5. `git commit -m "fix: resolver conflicto de merge entre main y rama2"`  
6. `git push origin rama2_Penarrieta`

Tras esto, el PR se actualizó y se pudo completar el merge en GitHub.

---

## 📌 Historial (ejemplo)
Salida relevante del historial:
```
*   69ae2b2 (HEAD -> main, origin/main) Merge pull request #2
|\  
| * 83f3a39 (rama2_Penarrieta) fix: resolver conflicto...
* | 6642e14 Merge pull request #1
|/  
* db644e8 primer commit - estructura inicial
```

---

## 🔗 Enlace al repositorio remoto
https://github.com/joseiverp/SDAW_9483

---

## 🧠 Conclusión personal
Esta práctica me ayudó a entender mejor el flujo real de trabajo con Git: crear ramas, hacer merges, resolver conflictos y mantener el repositorio remoto sincronizado. Además aprendí la importancia de documentar bien cada paso para que cualquiera pueda seguir el proceso.


## 📝 Reflexión personal sobre lo aprendido (rama3_Penarrieta)
En esta segunda parte he aprendido a trabajar con 2 remotos simultáneamente, manteniendo GitHub y GitLab conectados al mismo repositorio local. También he reforzado el uso de SSH.

## Información técnica añadida desde rama 3
A continuación se muestra la salida del comando:
`git log --oneline --graph --all`

>>
* b0ffab0 (HEAD -> rama3_Peñarrieta, origin/main, gitlab/main, main) actualizado
*   69ae2b2 Merge pull request #2 from joseiverp/rama2_Peñarrieta
|\
| *   83f3a39 (origin/rama2_Peñarrieta, rama2_Peñarrieta) fix: resolver conflicto de merge entre main y rama2
| |\
| |/
|/|
* |   6642e14 Merge pull request #1 from joseiverp/rama1_Peñarrieta
|\ \
| * | 0aba423 (origin/rama1_Peñarrieta, rama1_Peñarrieta) rama1: añadir explicación de comandos en README
|/ /
| * 5298068 docs rama2: añadir salida de git log en una línea
|/
* db644e8 primer commit - estructura inicial del proyecto SDAW_9483

---

# 🟩 Contenido añadido en la segunda parte de la tarea (rama 4)

## 📝 Resumen del procedimiento para conectar el repositorio local con GitLab
Para conectar mi repositorio local con un nuevo remoto en GitLab, primero configuré el acceso SSH y añadí la clave pública en mi cuenta. Después obtuve la URL SSH del proyecto vacío en GitLab. Desde mi repositorio local ejecuté el comando `git remote add gitlab <URL>` para añadir un segundo remoto sin eliminar el de GitHub. Verifiqué la configuración con `git remote -v` y finalmente subí los archivos con `git push gitlab main`, replicando el proyecto completo en GitLab.

## Información técnica añadida desde rama 4
- Añadir remoto: `git remote add gitlab git@gitlab.com:Joseip/sdaw_9483.git`
- Probar conexión SSH: `ssh -T git@gitlab.com`
- Ver remotos configurados: `git remote -v`
- Subir cambios al remoto GitLab: `git push gitlab main`
- Comprobar ramas y commits replicados en GitLab desde la interfaz web.
