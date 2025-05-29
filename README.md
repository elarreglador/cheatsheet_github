## PLANTILLA COMITS

<table border="1">
  <tr>
    <td colspan="3"><b>COMMITS COMUNES</b></td>
  </tr>
  <tr>
    <td>🎉 Primer commit!</td>
    <td>🎉 Compila sin errores!!</td>
    <td>🐞 Bug corregido:</td>
  </tr>
  <tr>
    <td>💾 Almacenamiento:</td>
    <td>🔗 Navegación a pantallas:</td>
    <td>🔥 Borrado:</td>
  </tr>
  <tr>
    <td>🚀 Cambio mayor:</td>
    <td>✨ Cambio menor:</td>
    <td>🎨 Mejora estética:</td>
  </tr>
  <tr>
    <td>📜 Nueva(s) clase(s):</td>
    <td>⚙️ Nueva(s) función(es):</td>
    <td>🔗 Nuevo(s) API REST endpoint(s):</td>
  </tr>
  <tr>
    <td>💡 Nueva funcionalidad:</td>
    <td>🈯 Config. de proyecto:</td>
    <td>🧯 Gestión de excepciones:</td>
  </tr>
  <tr>
    <td>🔍 Tests de funcionamiento:</td>
    <td>📷 Multimedia:</td>
    <td>📱 pantalla/vista/pagina:</td>
  </tr>
  <tr>
      <td>🛡️ Seguridad:</td>
      <td>📡 Comunic.:</td>
      <td>〰️ Data flow:</td>
  </tr>
  <tr>
      <td>⚡Eventos:</td>
      <td></td>
      <td></td>
  </tr>
  <tr>
    <td colspan="3"><b>HERRAMIENTAS EXTERNAS</b></td>
  </tr>
    <tr>
      <td>🟠 Postman export:</td>
      <td>🔴 Node-red export:</td>
      <td></td>
  </tr>
  <tr>
    <td colspan="3"><b>ARCHIVOS</b></td>
  </tr>
  <tr>
    <td>🔤 Cambio de nombre:</td>
    <td>📂 Estructura de archivos: </td>
    <td></td>
  </tr>
  <tr>
    <td colspan="3"><b>DOCUMENTACION Y REVISION</b></td>
  </tr>
  <tr>
    <td>📚 Documentación:</td>
    <td>📐 Formato y limpieza del documento:</td>
    <td>📐 Formato y limpieza del código:</td>
  </tr>
  <tr>
    <td>📑 Recursos:</td>
    <td>🏗️ Arquitectura:</td>
    <td>📸 Screenshots:</td>
  </tr>
  <tr>
    <td>🔖 Nueva version:</td>
    <td></td>
  </tr>
</table>

### AGREGA ANOTACION DE VERSION AL ULTIMO COMMIT
```bash
VERSION="v0.1.0"; git tag -a $VERSION -m " $VERSION 🔖" && git push origin $VERSION
```

## VERSIONADO: vX.Y.Z🔖

Cada número tiene un propósito específico:

Major (X) – Cambios incompatibles: Se incrementa cuando haces cambios que rompen compatibilidad con versiones anteriores.

Minor (Y) – Nuevas funcionalidades compatibles: Se incrementa cuando agregas nuevas funciones o mejoras, pero sin romper lo que ya existía.

Patch (Z) – Corrección de errores o mejoras menores:Se incrementa cuando haces correcciones, mejoras internas o ajustes, pero sin agregar ni quitar funcionalidades públicas.

## CREAR RAMA PARA FUNCIONALIDAD / CERRAR RAMA PARA FUNCIONALIDAD

Crear nueva rama de tipo feature/XXX , hotfix/XXX , fix/XXX , etc...
```bash
echo " " >> ./README.md ; git add . ; git commit -m "(⎇) Previo feature/XXX" ; git push
git checkout -b feature/XXX
echo " " >> ./README.md ; git add . ; git commit -m "(⎇) Inicio feature/XXX" ; git push
```
al finalizar la tarea volvemos a integrar la rama
```bash
echo " " >> ./README.md ; git add . ; git commit -m "(⎇) Previo a merge de feature/XXX"
git checkout main #Regresamos a la rama main
git pull origin main #Actualizamos main
git merge feature/XXX
echo " " >> ./README.md ; git add . ; git commit -m "(⎇) Finalizado merge feature/XXX"
```
Opcionalmente podemos borrar la rama de feature en local y remoto
```bash
git branch -d feature/tu-nombre-de-rama
git push origin --delete feature/tu-nombre-de-rama
```

## DESHACER COMMIT CONSERVANDO CAMBIOS
```bash
git reset --soft HEAD~1  # Revierte el commit pero conserva los archivos
git push origin main --force # Reemplaza el commit remoto
git push origin feature/XXX --force-with-lease # Sincroniza rama remota con la local
```

## AGREGAR CAMBIOS AL ULTIMO COMMIT
```bash
git add . ; git commit --amend --no-edit ; git push --force
```

## OPCIONES DEL TEXTO

**negrita**
```
**negrita**
```
*cursiva*
```
*cursiva*
```
***negrita cursiva***
```
***negrita cursiva***
```
~~tachado~~
```
~~tachado~~
```
`código en línea`
```
`código en línea`
```
> Esto es una cita
```
> Esto es una cita
```

[Texto del enlace](http://ejemplo.com)
```
[Texto del enlace](http://ejemplo.com)
```


## CAPTURAS DE PANTALLA EN README.md

<table>
  <tr>
    <td><img src="https://github.com/elarreglador/PMM_Room/blob/main/SCREENSHOTS/HomeScreen.png?raw=true" alt="HomeScreen" width="200" title="HomeScreen"></td>
    <td><img src="https://github.com/elarreglador/PMM_Room/blob/main/SCREENSHOTS/AuthorListViewScreen.png?raw=true" alt="AuthorListViewScreen" width="200" title="AuthorListViewScreen"></td>
    <td><img src="https://github.com/elarreglador/PMM_Room/blob/main/SCREENSHOTS/AuthorAddScreen.png?raw=true" alt="AuthorAddScreen" width="200" title="AuthorAddScreen"></td>
  </tr>
</table>

```
<table>
  <tr>
    <td><img src="https://github.com/elarreglador/PMM_Room/blob/main/SCREENSHOTS/HomeScreen.png?raw=true" alt="HomeScreen" width="200" title="HomeScreen"></td>
    <td><img src="https://github.com/elarreglador/PMM_Room/blob/main/SCREENSHOTS/AuthorListViewScreen.png?raw=true" alt="AuthorListViewScreen" width="200" title="AuthorListViewScreen"></td>
    <td><img src="https://github.com/elarreglador/PMM_Room/blob/main/SCREENSHOTS/AuthorAddScreen.png?raw=true" alt="AuthorAddScreen" width="200" title="AuthorAddScreen"></td>
  </tr>
</table>
```

## GIT LOG PERSONALIZADO
```bash
nano ~/.bashrc
   # Git log personalizado
   alias git-log="git log --graph --all --decorate --pretty=format:'%C(auto)%h%Creset [%an | %ad] %d %s' --date=short"
   alias gitlog="git-log"  # opcional: atajo más corto
   alias git='f() { if [ "$1" = "log" ]; then shift; git log --graph --all --decorate --pretty=format:"%C(auto)%h%Creset [%an | %ad] %d %s" --date=short "$@"; else command git "$@"; fi }; f'
source ~/.bashrc
```
El resultado se vera similar a esto:
```bash
*   aeb127e [David Moreno | 2025-04-11]  (HEAD -> main, origin/main) Merge commit '3732b92'
|\  
| * 3732b92 [David Moreno | 2025-04-11]  🏗️ Arquitectura: Retiro git de los components (vendorizado)
* | c7333bf [David Moreno | 2025-04-10]  Actualizar puntero de lvgl
|/  
* 79d83b2 [David Moreno | 2025-04-10]  Creo un reloj no sincronizado
* e8cf7fd [David Moreno | 2025-04-09]  Agregados estilos titulo2, texto1 y texto2
```

## COMANDOS BASICOS GIT

```bash
git init                                            # Inicializa un nuevo repositorio Git
git clone <url>                                     # Clona un repositorio remoto
git status                                          # Muestra el estado del repositorio
git add <archivo>                                   # Añade un archivo al área de staging
git commit -m "mensaje"                             # Crea un commit con mensaje
```

RAMAS

```bash
git branch                                          # Lista las ramas
git branch <nombre>                                 # Crea una nueva rama
git checkout <rama>                                 # Cambia de rama
git merge <rama>                                    # Fusiona una rama con la actual
```

REMOTO

```bash
git remote -v                                       # Lista los repositorios remotos
git push origin <rama>                              # Envía los cambios al remoto
git pull origin <rama>                              # Trae los últimos cambios del remoto
```

OTROS

```bash
git log --oneline --graph --decorate --all --color  # Historial de commits
git diff                                            # Muestra cambios sin commitear
git reset --hard && git clean -fdx                  # Revierte al último commit sin guardar
```

NUEVO REPOSITORIO
```bash
git init                                            # Genera directorio .git
git add . && git commit -m "🎉 Primer commit!"      # Prepara el primer commit
git branch -M main                                  # Renombra la rama actual a main
git remote add origin <RUTA_REPOSITORIO.git>        # Indica el origin del proyecto
git push -u origin main                             # Sube el commit
```

