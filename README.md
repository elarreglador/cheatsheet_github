## PLANTILLA COMITS

<table border="1">
  <tr>
    <td colspan="3"><b>COMMITS COMUNES</b></td>
  </tr>
  <tr>
    <td>🎉 Primer commit!</td>
    <td>📷 Multimedia:</td>
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
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td colspan="3"><b>ARCHIVOS</b></td>
  </tr>
  <tr>
    <td>🔤 Cambio de nombre:</td>
    <td>🟠 Postman export:</td>
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
</table>


## VERSIONADO: vX.Y.Z🔖

Cada número tiene un propósito específico:

Major (X) – Cambios incompatibles: Se incrementa cuando haces cambios que rompen compatibilidad con versiones anteriores.

Minor (Y) – Nuevas funcionalidades compatibles: Se incrementa cuando agregas nuevas funciones o mejoras, pero sin romper lo que ya existía.

Patch (Z) – Corrección de errores o mejoras menores:Se incrementa cuando haces correcciones, mejoras internas o ajustes, pero sin agregar ni quitar funcionalidades públicas.


### AGREGA ANOTACION DE VERSION AL ULTIMO COMMIT
```bash
VERSION="v0.1.0"; git tag -a $VERSION -m " $VERSION 🔖" && git push origin $VERSION
```

## Comandos Básicos git

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
git reset --hard HEAD                               # Revierte al último commit sin guardar
```

NUEVO REPOSITORIO
```bash
git init                                            # Genera directorio .git
git add . && git commit -m "🎉 Primer commit!"      # Prepara el primer commit
git branch -M main                                  # Renombra la rama actual a main
git remote add origin <RUTA_REPOSITORIO.git>        # Indica el origin del proyecto
git push -u origin main                             # Sube el commit
```

