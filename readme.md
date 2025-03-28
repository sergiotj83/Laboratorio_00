# Laboratorio_00
Primer cambio en la rama development


1. Crear un repositorio en local

    Abre tu terminal y navega hasta el directorio donde deseas crear el repositorio.
       He abierto el terminal de Git directamente en el directorio.
    Crea una carpeta con el nombre del repositorio.
       mkdir Laboratorio_00
    Ingresa a la carpeta que acabas de crear.
       cd Laboratorio_00
    Inicializa el repositorio de Git.
       git init

2. Subir el repositorio a GitHub

    Crea un nuevo repositorio en GitHub.
       Entro en mi cuenta de GitHub, y marco la opción de "New" para crear un repositorio, marcando la opción de "Public" y sin añadir "Readme"
    Copia el URL del repositorio que acabas de crear en GitHub
    Conecta tu repositorio local con el repositorio en GitHub.
       git remote add origin git@github.com:sergiotj83/Laboratorio_00.git
    Verifica que la conexión se haya establecido correctamente.
        git remote -v
origin  git@github.com:sergiotj83/Laboratorio_00.git (fetch)
origin  git@github.com:sergiotj83/Laboratorio_00.git (push)


3. Hacer un commit y un push

    Crea un archivo en la carpeta del repositorio.
       echo "# Laboratorio_00" > readme.md
    Añade el archivo al staging.
       git add readme.md
    Crea un commit con un mensaje descriptivo.
       git commit -m "Primer commit"
    Sube los cambios al repositorio en GitHub.
       git push -u origin master

4. Crear una rama

    Crea una rama nueva llamada "development".
       git branch development
    Cambia a la nueva rama.
       git checkout development
    Realiza algunos cambios en el archivo que creaste.
       echo "Primer cambio en la rama development" >> readme.md
    Añade y haz un commit con los cambios en la rama "development".
       git add readme.md
       git commit -m "Primer commit de la rama development"
    Sube los cambios a Github.
       git push -u origin development

5. Hacer un merge

    Vuelve a la rama "main".
       git checkout master
    Haz un merge de la rama "development" a la rama "main".
       git merge development
    Si no hay conflictos, los cambios realizados en la rama "development" se incorporarán a la rama "main".
    Hax un push de los cambios al repositorio en GitHub.
       git push
