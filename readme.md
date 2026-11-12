# Curso de Introducción a GIT AF 47082 – GR 99733

- Introducción a GIT AF 47082 – GR 103068
- Duración: 16 horas
- Modalidad: On-line
- Fechas: M 10/11/2026 - J 12/11/2026
- Horario: 9:00 - 14:20
  - 9:00-11:30 (2h 30m)
  - Descanso 11:30-11:50 (20m)
  - 11:50-14:20 (2h 30m)

Formador: Alejandro Cerezo
<alce65@hotmail.es>

## Contenidos

- Conceptos básicos
    - `¿Qué es y que no es GIT?`
    - `Cómo usar correctamente GIT`
    - `Configuración imprescindible` 
- Fundamentos y arquitectura interna de GIT
    - `Diferencias entre el working directory, el stage y el repositorio`
    - `Qué es exactamente un commit`
    - `Tipos de referencias (HEAD, ramas y tags)` 
- Commits
    - `Cómo preparar selectivamente un commit`
    - `Cuando hacer un commit`
    - `Cómo deshacer commits`
    - `Buenas prácticas` 
- Como resolver los conflictos
    - `Qué es un conflicto, cómo reducir su frecuencia y cómo resolverlos`
- Branching
    - `Qué es exactamente una rama en GIT`
    - `Cómo trabajar con ramas y diferentes maneras de fusionarlas`
- Trabajando con repositorios remotos
    - `Cómo comunicar los repositorios locales con los remotos`
    - `Diferentes escenarios cuando trabajamos en equipo contra un repositorio remoto`
    - `Configuración básica `
- Pull Requests
    - `Por qué usar PR`
    - `Cómo hacer correctamente una PR`
    - `Cómo configurar el repositorio remoto si usamos “PR”`
- Modelos de branching
    - `Git Flow`

Desarrollo del curso en la carpeta Oficial -> [repo](https://github.com/IconoTC/-Introducci-n-a-GIT-AF-47082-GR-99733)

## Desarrollo del curso

### Día 1 (Martes 10/11/2026)

- Presentación profesor / alumnos
- Introducción: Qué es un SCV y qué un SCV distribuido
- IDE / Editor de código: Visual Studio Code (VSC)
- Terminales
- Instalación de Git
  Configuración inicial
  - Nombre de usuario y correo electrónico
- Primeros pasos con Git
  - Primer repo (init), primer commit: .gitignore / readme.md

- [Descanso] 11:30 - 11:50


- Primeros pasos con Git (2)

  - Anatomía de un repositorio git: working directory, staging area (index o cache) y repositorio (.git)
  - Estados de un archivo: untracked (U), tracked (modified (M), staged (A), committed)
  - add/commit/reset y status/log/show - GitGraph
  - Mensajes de commit

- Anatomía de comandos típicos, referencias VS paths

  - HEAD, main, HEAD~1 y otras referencias útiles

- Integración con otras herramientas y entornos
  - Clientes gráficos
  - Entornos de desarrollo
  - Repositorios remotos: GitHub, GitLab, Bitbucket
    - remotes -> push / pull
    - Clonar un repositorio: clone

- Comprobar el repositorio.
  - git log
  - git show
  - git diff

- Aliases
  - Qué son
  - Cómo crearlos desde el CLI: `git config --global alias.ch checkout`
  - Crearlos editando el fichero de configuración: `git config --global -e` 

- Ficheros Markdown
  - Qué son
  - Sintaxis básica
  - Vista previa en VSC / GitHub / GitLab

<!-- (No incluido en el curso actual)

- Git internals (1/2 día)

  - Estructura de un repositorio git: .git
  - Objetos git: blobs, trees, commits (y tags)
    - Creación y lectura de objetos
    - Creación del árbol de objetos en un primer commit
    - Modificación del árbol de objetos en commits sucesivos
  - Referencias: HEAD, ramas (tags y remotes)
  - Taller: creación de un repositorio git "a mano" 
-->

- Estructura interna de Git (brevemente)
  - Objetos git: blobs, trees, commits (y tags)
  - Referencias: HEAD, ramas (tags y remotes)


- Herramientas para preparar un buen commit en cualquier situación

  - Operaciones en la Staging Area (Index)
    - Añadir ficheros
    - Eliminar de la Staging Area (Index)

### Día 2 (Miércoles 11/11/2026)
  
- Herramientas para preparar un buen commit en cualquier situación (2)
  
  - Eliminar ficheros: git rm
  - Cambiar nombre de ficheros: git mv
  <!-- - git blame -->
  - Recapitulando: Git básico

  - Reescribiendo la historia
    - Advertencia
    - git commit --amend
      - Ref logs
    - git checkout y git reset (introducción)
    - git checkout
      - Evolución de git checkout: Nuevos comandos git switch y git restore
        - git checkout / git restore a nivel de archivo (restore) 
  - git reset
    - opciones de git reset: --soft, --mixed y --hard
    - git reset a nivel de archivo
  - rebase interactivo
    - edit: modificando un commit
    - squash y fixup: fusionando commits
    - drop: eliminando un commit

- Otros comandos
  - git revert 

  <!-- 
  - git clean
  -->

- [Descanso] 11:30 - 11:50

- Trabajando en paralelo: ramas
    - Ramas: etiquetas
      - main y feature branches (feature/homepage, feature/login, feature/signup)
      - hotfixes (hotfix/login-error, hotfix/signup-error)
      - bugs (bug/login-error, bug/signup-error)
 
    - Operaciones con ramas
      - Crear y seleccionar
        - Crear desde referencia
      - Ver ramas
      - Borrar ramas
      - Mover y renombrar ramas
    - git stash

  - Combinación de ramas: Merge y Rebase
    - git merge
      - fast-forward
      - three-way (ort) merge
      - --no-ff (force a merge ort)
    - git rebase 
    - Resolución de conflictos


### Día 3 (Jueves 12/11/2026)

- Combinación de ramas (continuación)
  - git cherry-pick
  - patches (mención breve) 

- Etiquetas (tags)
  - Tags anotadas y tags ligeros
  - Crear, listar, eliminar 

- Repositorios remotos

  - Repositorios "bare"
  - Clonar repositorios: git clone
  - git remote
  - git push
    - push tags
  - git pull

    - git fetch
    - git merge / git rebase
    - Conflictos

  - Ramas remotas
    - Seguimiento de ramas remotas (tracking branches)
    - Subir ramas locales a ramas remotas: -u 
    - Crear ramas locales a partir de ramas remotas: fetch + checkout / switch -c
    - Eliminar ramas remotas git branch -d -r origin/feature/branch

  - Pull requests (GitHub) / Merge requests (GitLab)
    - Flujo de trabajo típico
    - Revisión de código 
  
- [Descanso] 11:20 - 11:40
- [Encuesta]

- Ramas remotas (continuación)


- Pull requests (GitHub) / Merge requests (GitLab)
    - Resolución de conflictos en remoto
    - Buenas prácticas:
      - Actualizar la rama con la rama main antes de hacer el merge
      - Resolución de conflictos en local
      - Eliminar la rama una vez hecho el merge

- Flujos de trabajo (workflows)
  - Git Flow
  - GitLab Flow
  - GitHub Flow
    - Ship-Show-Ask

- Buenas prácticas 

- Configuración avanzada de git
  - Hooks
  - Husky (Hooks en JS) 

- Forks

<!-- (No incluido en el curso actual, pero puede ser interesante para el alumno)

- Preparar un commit parcial: git add -p
- git notes -->

<!-- COMENTADO

- Sub-proyectos (submodules)

- WorkTrees

- GitHub (comentario general)
  - Hosting de Repositorios
    - repositorios públicos y privados; ramas y remotos: push y pull (v.s.)
    - forks
  - Colaboración
    - pull requests: revisión de código y comentarios (v.s.)
    - PR desde ramas y forks
    - Proyectos
      - Tableros (Boards)
      - issues y proyectos; milestones
    - Wikis
    - Gists
  - GitHub CLI
  - GitHub Pages
-->
