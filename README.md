# Proyecto con Django
![](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftse4.mm.bing.net%2Fth%3Fid%3DOIP.ZjJwpEXpj4Q9I-b5HjmytwHaEK%26pid%3DApi&f=1)
- ![](https://img.shields.io/badge/Python-3.10-green) 
- ![](https://img.shields.io/badge/Django-4.1.1-blue)

## Creamos la carpeta del proyecto
> mkdir django_proj

## Creamos el entorno virtual
> py -m venv venv

## Activamos el entorno virtual
> Windows:  .\venv\Scripts\activate <p>
> Unix:   source venv/bin/activate

## Instalamos Django
> pip3 install django<p>
> o<p>
> sudo pip3 install Django

## Inicializamos GIT
> git init

## Iniciamos Django
> django-admin startproject django_proj_app .

## Creamos el gitignore
> touch .gitingnore

## Ver el proyecto en local
> py manage.py runserver

### Si sale un error con el puerto (ubuntu)
> sudo fuser -k 8000/tcp

## Creamos una aplicación ubicados en la carpeta django_proj 
> py manage.py startapp polls

## Creamos las tablas de polls, se crean los modelos que escribimos (ORM)
> py manage.py makemigrations polls 

## Tomar los modelos que se crearon y ejecutarlos en SQL en la base de datos. 
> py manage.py migrate

## Acceder a la consola interactiva
> py manage.py shell 

## Empezar a trabajar con los modelos creados 
> from polls.models import Choice, Question

## Nos permite acceder a todos los objetos que se crearon a partir de una clase
#### Accedemos a todos los registros 
> Question.objects.all()

## Para crear objetos de tipo datetime
> from django.utils import timezone

## Creando un registro en la base de datos
> q = Question(question_text="un string ",pub_date=timezone.now())
> q.save()

## Accedemos al contenido creado
> q.question_text  <p>
> q.pub_date  <p>
> Question.objects.all()  <p>
> >>> <QuerySet [<Question: Question object (1)>]>

## Modificamos los modelos para objtener una mejor salida
　
```python
 """class Question(models.Model):
    question_text = models.CharField(max_length=200)
    pub_date = models.DateField("date published")"""

    def __str__(self):
        return self.question_text


"""class Choice(models.Model):
    question = models.ForeignKey(Question, on_delete=models.CASCADE)
    choice_text = models.CharField(max_length=200)
    votes = models.IntegerField(default=0)"""

    def __str__(self):
        return self.choice_text
```
## uso del doble __ con el método filter
> Model.objects.filter(condición)  <p>
> [Documentación](https://docs.djangoproject.com/en/4.1/topics/db/queries/#field-lookups-intro)  <p>
> __gt = Mayor que  <p>
> __gte = Mayor o igual que  <p>
> __lt = Menor que  <p>
> __lte = Menos o igual que  <p>
> __startswith = Empieza con  <p>
> __iexact: Un case-insenstive match.   <p>
> __contains: Contiene  <p>
> __icontains: Version case-insensitive de la anterior  <p>
> __istartswith = version case-insensitive de startswith  <p>
> __iendswith = version case-insensitive de endswith  <p>
> __endswith = Termina con  <p>

## Herramienta 'django-extensions'
```shell
pip install django-extensions 
```
> en el archivo settings
```python

INSTALLED_APPS = (
    ...
    'django_extensions',
    ...
)

```
```shell
python3 manage.py shell_plus
```

## ORM
> Un ORM (Object-Relational Mapping) es una técnica que nos permite crear una Base de Datos Orientada a Objectos (virtual), que opera sobre la Base de Datos Relacional (real).
Utilizando un ORM podemos operar sobre la base de datos aprovechando las características propias de la orientación a objetos, como herencia y polimorfismo.
También podemos acceder a los atributos de una Entidad de la misma forma que accedemos a los atributos de una Clase, realizar operaciones para obtener, crear, modificar y eliminar datos, todo desde el código de programación sin tener que escribir SQL. Esto además nos permite escribir el código una sola vez y garantizarnos que va a seguir funcionando incluso si en el futuro se cambia el motor de Base de Datos (por ejemplo, de MySQL a Microsoft SQL Server).

---
<div align="center">

## Acerca de mí! <img src="https://raw.githubusercontent.com/iampavangandhi/iampavangandhi/master/gifs/Hi.gif" width="30px"></h2>


Soy Ingeniera en sistemas, me gustan los entornos linux, machine learning y la ciberseguridad, constantemente estoy aprendiendo cosas nuevas. 



**🛠️Frecuentemente trabajo con:**

<code><a href="https://www.python.org/" target="_blank"><img height="50" src="https://www.vectorlogo.zone/logos/python/python-ar21.svg"></a></code>
<code><a href="https://flask.palletsprojects.com/en/1.1.x/" target="_blank"><img height="50" src="https://www.vectorlogo.zone/logos/pocoo_flask/pocoo_flask-ar21.svg"></a></code>
<code><a href="https://ubuntu.com/"><img height="50" src="https://www.vectorlogo.zone/logos/linux/linux-ar21.svg"></a></code>
<code><a href="https://git-scm.com//" target="_blank"><img height="50" src="https://www.vectorlogo.zone/logos/git-scm/git-scm-ar21.svg"></a></code>
<code><a href="https://www.djangoproject.com/"><img height="50" src="https://www.vectorlogo.zone/logos/djangoproject/djangoproject-ar21.svg"></a></code>
<code><a href="https://jupyter.org/"><img height="50" src="https://www.vectorlogo.zone/logos/jupyter/jupyter-ar21.svg"></a></code>



💚[AnabelBerumen](https://github.com/AnabelBerumen)💚
</div>  
