# Social-Network

A Sample prototype of a basic social networking Web application.
```
Uses Django version 1.10
```

### Download and Setup python virtual environment

```
cd Social_main
pip install virtualenv
virtualenv venv
```

### Start the virtual environment

```
source ./venv/Scripts/activate
```

### Install Django and pillow to your virtual environment

```
pip install Django==1.10
pip install pillow
```

### Add the following snippet to venv/lib/site-packages/django/db/models/base.py

```
<!-- under # Create the class -->

new_attrs = {'__module__': module}
classcell = attrs.pop('__classcell__', None)
if classcell is not None:
new_attrs['__classcell__'] = classcell
new_class = super_new(cls, name, bases,new_attrs)
```
### Start the development server

```
python manage.py runserver
```

The development server starts on <B>localhost:8000</B>