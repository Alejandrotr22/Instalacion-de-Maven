# Instalacion-de-Maven


Este repositorio está destinado a la instalación de Maven en Kubuntu


## Introducción
**¿Qué es Maven?**

Maven es una herramienta muy útil que soluciona la dura vida de un programador de java, facilitando la creación de estructuras de directorios y la instalación de librerías necesarias para el desarrollo.  
<div align="center">
<img width="40%" src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/52/Apache_Maven_logo.svg/1280px-Apache_Maven_logo.svg.png">
</div>

## Requisitos
Para la instalación de este programa es necesario:
  - versión del JDK igual o superior a la versión 1.7.

## Pasos

### **1.Actualización de repositorios y descarga**

El primer paso es actualizar los repositorios con el comando: 
```
sudo apt update
```
y después instalar la versión predefinida del Maven con el comando 
```
sudo apt install maven
```
<div align="center">
<img width="100%" src="http://drive.google.com/uc?export=view&id=1KWHHW3jeFLg8XmXJBwSa5dAXXjBktVC_">
</div>

<div align="center">
<img width="100%" src="http://drive.google.com/uc?export=view&id=1QtdAvfg-WXXtuUhRbnaIYjOwifhBPloV">
</div>

### 2.Actualizar la version de Maven

Tras la instalación de la versión estándar de Maven, podemos comprobar con 
```
maven -version
```
Que tenemos la versión 3.6.3 de esta misma, ahora necesitamos actualizarla a la 3.8.2, para ello necesitamos utilizar este comando

```
wget https://www.apache.org/dist/maven/maven-3/3.8.2/binaries/apache-maven-3.8.2-bin.tar.gz -P /tmp
```

<div align="center">
<img width="100%" src="http://drive.google.com/uc?export=view&id=1L6J4dckP3L71fYW33aRHhB23gqcQjepA">
</div>


Lo siguiente que necesitamos hacer es extraer los archivos descargados en una carpeta específica con el siguiente comando
```
sudo tar xf /tmp/apache-maven-*.tar.gz -C /opt
```

Después utilizamos este comando para tener el control sobre las versiones de Maven
```
sudo ln -s /opt/apache-maven-3.8.2 /opt/maven
```
<div align="center">
<img width="100%" src="http://drive.google.com/uc?export=view&id=1jaqbx5mlwaWOJVhr0piJMcD-nwbMIsG7">
</div>

### 3.Variables de entorno

Después de extraer el archivo descargado en la carpeta /opt, necesitamos declarar la variables de entorno con
```
sudo nano /etc/profile.d/maven.sh
```

y dentro del directorio escribimos teniendo en cuenta la versión del java correspondiente:

<div align="center">
<img width="50%" src="http://drive.google.com/uc?export=view&id=1lUZflsjEd8iMHqDNI8xn0Btwr0eckGLB">
</div>
Guardando el archivo como: /etc/profile.d/maven.sh

### 4.Últimos pasos

Necesitamos que este script sea ejecutado con chmod con el comando
```
sudo chmod +x /etc/profile.d/maven.sh.
```

Por último cargamos la variables de entorno 
```
source /etc/profile.d/maven.sh
```
<div align="center">
<img width="100%" src="http://drive.google.com/uc?export=view&id=1B2tFu3ahaflBZpIvI7ljObias2-69ZPS">
</div>

### 5.Comprobamos la versión instalada

Ahora con el comando
```
mvn -version
```
Deber aparecer esta versión.

<div align="center">
<img width="100%" src="http://drive.google.com/uc?export=view&id=1wa6iieOGoH3kuV8YuPyD5gIqGLdb0xeB">
</div>

### Conclusión

*Siguiendo estos pasos podrá instalar en su sistema operativo Linux el programa Maven, solo falta entrar en la documentación acerca de Maven y aprender a utilizarlo.*





