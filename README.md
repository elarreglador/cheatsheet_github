![Banner](./assets/banner.png)

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
      <td>📡 Comunic.:</td>
      <td>🌐 Network:</td>
      <td>〰️ Data flow:</td>
  </tr>
  <tr>
      <td>⚡Eventos:</td>
      <td>🛡️ Seguridad:</td>
      <td></td>
  </tr>
  <tr>
    <td colspan="3"><b>HERRAMIENTAS EXTERNAS</b></td>
  </tr>
    <tr>
      <td>🟠 Postman export:</td>
      <td>🔴 Node-red export:</td>
      <td>📋 TODO:</td>
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

## GIT LOG PERSONALIZADO
```bash
nano ~/.bashrc

    # Git log personalizado
    alias git-log="git log --graph --all --decorate --pretty=format:'%C(auto)%h%Creset %C(green)[%an | %ad]%Creset %C(yellow)%d%Creset %s' --date=short"
    alias gitlog="git-log" # opcional: atajo más corto
    alias git='f() { if [ "$1" = "log" ]; then shift; git log --graph --all --decorate --pretty=format:"%C(auto)%h%Creset %C(green)[%an | %ad]%Creset %C(yellow)%d%Creset %s" --date=short "$@"; else command git "$@"; fi }; f'

source ~/.bashrc
```
El resultado se vera similar a esto:
```bash
*   beb4c62 [David Moreno | 2025-05-29]  ⚡Eventos: Se inician tareas de deteccion de eventos en room_logic_task
|\  
| * 81d2b9a [David Moreno | 2025-05-28]  (origin/feature/events, feature/events) ⚡Eventos: pantalla lvgl genera eventos en event_bus
| *   de6d7ca [David Moreno | 2025-05-27]  Merge branch 'feature/lvgl' into develop
| |\  
| | * b1a8f46 [David Moreno | 2025-05-26]  (origin/feature/lvgl, feature/lvgl) ✨ Cambio menor: Finalizado comportamiento esperado para botones y sliders
| | * a037753 [David Moreno | 2025-05-23]  🎨 Mejora estética: Aplicados colores diferentes a cada elemento
| * | 6855757 [David Moreno | 2025-05-27]  (origin/feature/mqtt, feature/mqtt) 📑 Recursos:     Disponemos de los valores recibidos en el JSON como variables locales
* | | bd64750 [David Moreno | 2025-05-28]  Importado event_bus de rama events
* | | b09486c [David Moreno | 2025-05-28]  📚 Documentación: Comentado codigo
|/ /  
* / 0fb4380 [Your Name | 2025-05-26]  Feat: mqtt basic helow world connection
|/  
* affd673 [David Moreno | 2025-05-22]  🎨 Mejora estética: Reorganizadas tarjetas a falta de centrado vertical
```

## CLONAR VERSION ESPECIFICA DEL REPOSITORIO 

La version se busca a partir del release/tag , en este caso release/v5.3
```
git clone --recursive https://github.com/espressif/esp-idf.git -b release/v5.3 esp-idf-5.3.0
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
git switch <rama>                                   # Cambia de rama
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

