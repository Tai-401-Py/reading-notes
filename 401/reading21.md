# [Django 3: The  MDN Docs](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Models)

## Django Models

Django web apps manage data through python objects reffered to as models. They define the structure of stored data, including field types and max size, default vals, help text documentation. 

The Definition of the model is independant of the database. 

---

### Getting started

Take a few minutes to think about the data that needs to be stored and the relation between the objects. 

For example, books. Title, Summary, Author, Language, ISBN, Genre. We also need to account for multiple authors with same names. So when designing the model, it makes sense to have a seperate model for every "object". In this case, Books, instances of books, and the authors.

### Model primer

Models are usually defined in a models.py they are implemented as a subclass and can include metadata, fields, and methods.

Fields: Any model can have an arbitray number of fields. These can be of any type. Each one represents a column of data on the final table. 

```py
my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')
```

* name - explanitory, used to refer to it in queries and templates
* models.CharField - Field wil contain alphanumeric.
* max_length - MAx char in feild
* help_text - Documentation goes here

[See here for a full list of field options](https://docs.djangoproject.com/en/4.0/ref/models/fields/#field-options)

**The order that fields are declared affect thier default order in the model.**

Minimally you need to call `__str__` Class method on every model to return a human readable string for each object

Another common method, is ti use `get_absolute_url()` if you use this Django will add a "View on site" button to the model's record editing admin site.

---

### Managing Models

Once defined, you can use them to CRUD the records.

Creating and Modification

Define the model of the instance and then `model_name.save()`

You can search for records that match certain criteria using the `objects` attribute of the model.

Using methods such as `all()` and `filter()` you can narrow down or grab as much data as you need. 

## [ADMIN DUTIES](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Admin_site)

Once you have models it's time to add data. 

The admin application can use the models you defined and build a site area that you can use the CRUD functions to test your model, and get a feel for if tyou have the 'correct' data. It's also useful for managing data. 

It's reccomeneded from the developers of Django that you use it only for internal data managment. This is due to the fact that not all users need to see the extranious data about the models themselves.

After registering the model to the admin application, you should create a new superuser for testing the views and templates. 