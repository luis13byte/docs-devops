## Comandos útiles para GIT

Crear un repositorioo dentro de un nuevo directorio (especificando el nombre del proyecto)
~~~
git init [nombre de proyecto]
~~~

Establecer configuración especifica como usuario, email, etc.. (--global para todos los repos locales, --local para el repo actual)
~~~
git config --local user.email luis@github.com
git config --local user.name "Luis Acosta"
~~~

Muestra la lista de los archivos que se han cambiado junto con los archivos que están por ser preparados o confirmados.
~~~
git status
~~~

Navegar entre ramas, con "-b" creamos una rama nueva y automaticamente cambiamos a ella.
~~~
git checkout -b dev
git checkout main
~~~

Fusionar una rama con otra rama activa.
~~~
# Hacer cambios en dev y luego..
git checkout main
git merge dev
# Después de fusionar podriamos borrar dev
~~~

Resetear el index y el directorio de trabajo al último commit.
~~~
git reset - -hard HEAD
git reset [archivo]
~~~

3 comandos: Agregar archivos al "stage area" & crea una instantánea de cambios & envía las confirmaciones locales al repo remoto.
~~~
git add README-now.md
git commit -m "docs: new readme"
git push dev
~~~

Fusionar los cambios que se han hecho en el repo remoto con el repo local.
~~~
git pull
~~~
