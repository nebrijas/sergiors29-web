# Actividad Dirigida 2

La segunda actividad dirigida del módulo de Periodismo de Datos II constaba de tres etapas. En la primera se debía convertir el repositorio en una web servida desde GitHub. En este sentido, se utilizó una funcionalidad de Github que además de funcionar como servidor de git, también serviría como servidor web.

De acuerdo con lo solicitado en clases para el desarrollo de ésta actividad dirigida, se cumplió con los siguientes pasos:


## Primera parte.

Para convertir el repositorio en una web, se ingresó a la configuración desde [https://github.com/nebrijas/sergiors29-web/settings/pages](https://github.com/nebrijas/sergiors29-web/settings/pages). Esta fue la forma para activar la opción `pages`. Una vez dentro, en la parte de `fuente` o `source`, seleccioné la opción `main` y en folder coloqué `root`.

Después de realizar estos pasos, a los pocos segundos se generó nuestra página web donde se puede ver el contenido del archivo __README.md__, en la direccion [https://nebrijas.github.io/sergiors29-web/](https://nebrijas.github.io/sergiors29-web/).


## Segunda parte.

La siguiente parte de la asignación se realizó con el uso de la herramienta __git bash.__ Desde ahí, la tarea principal era clonar el repositorio remote y realizar una copia en local, configurar git, crear un archivo _ad1.md_ a partir del _README.md_ y editarlos para que el contenido correspondiera con su nombre.

1. Con el uso de __git bash__ coloqué `pwd` para imprimir el directorio de trabajo en el que me encontraba.
2. Posteriormente utilicé `git clone`, seguido de la dirección del repositorio [https://github.com/nebrijas/sergiors29-web](https://github.com/nebrijas/sergiors29-web) para modificarlo y clonar la carpeta.
3. El siguiente paso fue escribir _sergiors29-web/_ y _enter_ para cambiarlo por el del fichero o carpeta.
4. En la siguiente fase se usó el comando `ls` para visualizar o enumerar los archivos dentro del directorio de trabajo.
5. Como parte del proceso se introdujo `git config` + _user.name_ + _usuario_ de __github__ y _enter_, como parte de las tareas de configuración del __git.__ Lo mismo se hizo para con _user.email_, añadiendo la cuenta de correo electrónico usada para la creación de cuenta en __Github__ y _enter_.
6. Después de estos pasos, hubo que acceder desde el navegador a [https://github.com/settings/tokens](https://github.com/settings/tokens) para generar un token, al cual se denominó __perdatos2__ configurado para expirar en 60 días. Una vez generado el nuevo token, se copió y se colocó entre comillas (" "), precedido por el comando `echo`, para crear el nuevo archivo.
7. En la parte final de la actividad, se usó `nano` para ubicar archivo a modificar, se utilizó la tecla `control` + `X` para guardar los cambios, se confirmó el nombre del archivo y _enter_. Se añadió comentario sobre lo realizado con `git commit -m` y luego `git push` para actualizar y comprobar que los cambios se reflejen en el repositorio.


Finalmente se actualizó el repositorio remoto desde el local y se comprobó que los cambios se hubiesen producido en remoto.


## Tercera parte.

Previamente, se había creado el archivo _ad2.md_, desde la web. Con el uso de la terminal de __git bash__ se hicieron las correspondientes actualizaciones sobre los pasos realizados en cuanto al desarrollo de esta actividad, a manera de ejercicio de programación literaria, que es lo que se refleja en este documento.

Para la escritura se tomaron en cuenta los mecanismos de redacción para __Markdown__ para plasmar los componentes de este ejercicio. Para ello usé el comando `nano` para llamar al archive _ad2.md_, desde donde pude realizar las respectivas modificaciones, luego `Control`+`X` para salir, cuando me pedía salvar las modificaciones le di a la tecla `Y` y `enter` para confirmar el nombre del archivo (ad2.md).

Con `git status` me informaba que se debía actualizar la modificación del archivo _ad2.md_, lo cual hice con el uso de `git add` _ad2.md_ (nombre del archivo), posteriormente utilicé `git commit -m` para añadir comentarios sobre las últimas actualizaciones al escrito. Volví a utilizar `git status` para verificar que todo estuviese en orden antes de actualizar el repositorio con `git push` y comprobar que los cambios apareciesen en remoto.

Fue el mismo procedimiento realizado cada vez que ingresaba para actualizar el texto del ejercicio.

