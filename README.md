# Comandos
## Comandos varios en consola

- `ls`: ver que hay en el directorio.
- `ls -lah`: muestra todo, hasta archivos ocultos (lista todo para lectura humana).
- `pwd`: ver la ruta de trabajo y saber donde estoy.
- `cd <carpeta_nombre>`: pasar a tal carpeta.
- `cd .`: directorio en el que estoy.
- `cd ..`: directorio padre.
- `cd /`: directorio raiz.
- `cd /<carpeta_nombre>/<carpeta_nombre>/`: ir directo a tal directorio (escribir en orden).
- `clear`: limpia pantalla.
- `mkdir <nombre_carpeta_nueva>`: crea un directorio.
- `cat <ruta>`: muestra lo que hay dentro del fichero en la ruta que le pasamos.
- `<donde> | grep <cadena>`: encuentra una cadena específica en un archivo.
- `sudo <etc>`: Hacer algo con permisos de administrador.
- `rm <nombre_de_lo_que_queremos_eliminar>`: Eliminar algo.



## Referencia de comandos git

- `git clone <url-del-repositorio>`: hace una copia del repositorio remoto en la máquina local.
- `git clone <url-del-repositorio> <destino>`: al igual que el anterio, pero permite crear la copia
  en una carpeta con el nombre que especificamos en `<destino>`



- `git log`: permite explorar el histórico de commits.
- `git log --oneline`: simplifica la salida del log poniendo solamente el hash y el mensaje del commit.

- `git fetch`: actualiza la información de las ramas y los commits disponibles en el repositorio remoto.
- `git add .`: agrega todos los cambios realizados en el repositorio y los prepara para un commit.
- `git commit -m "<escribir commit>"`: hace el commit con el texto que pongamos.
- `git pull`: sincroniza desde el repositorio remoto hacia la máquina local el contenido de los commits
  de la rama actual.
- `git push`: sincroniza desde la máquina local hacia el repositorio remoto el contenido de los commits
  de la rama actual.

- `git remote`: lista todos los espacios remotos a los que hace referencia el repositorio local (y, por tanto, puede
  sincronizar cambios con él).
- `git remote get-url origin`: 'origin' es el nombre del espacio remoto (en este caso Github) y con este comando
  podemos ver la URL a la que hace referencia. En el caso de este repo: <https://github.com/KeepCodingCeroXXII/romanos.git>

## Cómo crear un entorno virtual

Supongamos que quiero crear un entorno virtual con el nombre _env_.

```
# en windows
python -m venv env

# en mac/linux
python3 -m venv env
```

## Cómo activar el entorno virtual

```
# en windows
.\env\Scripts\activate

# en mac/linux
source ./env/bin/activate
```

## Gestor de paquetes: pip

- Instalar un paquete nuevo: `pip install <nombre-del-paquete>`
- Instala los paquetes escritos en un archivo txt `pip install -r <requirements.txt (nombre donde están los paquetes)>`
- Listar los paquetes instalados: `pip list`
- Listar paquetes en formato de dependencias: `pip freeze`
- Para guardarlo en el archivo de dependencias: `pip freeze > requirements.txt`

## Cómo desactivar el entorno virtual

```
deactivate
```

## Cómo eliminar un entorno virtual

Basta con eliminar el directorio.

`rm -rf env/`: Elimina el directorio env (entorno virtual creado con anterioridad) y todos sus archivos. Posicionarse
en el directorio donde esta creado env.

## Variables de entorno

- Linux / Mac: `export FLASK_APP=hola` `export FLASK_DEBUG=True`

- Windows: `set FLASK_APP=hola` `set FLASK_DEBUG=True`
