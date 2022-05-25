# Django CRUD and other Forms

## Working with forms

An Html form is a group of widgets on a webpage which can be used to collect data. They are flexible because opf he different types they come in. 

When typically working with forms they can take a lot to get started and Django takes most of that work away, by providing a pre-existing framework. Then Django uses the information provided to create the forms you need. 

Some of the things Django does is.

1. Display the default form the first time a user requests it.
2. Recieve data submit request and bind it to the form
3. Clean and validate the form, by removing invalid characters that might send malicious content to the server. 
4. If there is invalid data, it will redoisplay the form, this time with user pop'd values and errors.
5. Preform required actions such as ssave data if everything is correct. 
6. Once finished automatically send user to another page if needed. 

## Forms

Form class is at the heart of Django's handling system for forms. It helps define the layout and widgets needed. 

The declaration syntax for a form is very similar to taht of a model. 

`from django import forms` 

then we set the form as a subclass of `forms.Form`.

There are lots of forms but not limited to....  

- BooleanField
- TypedChoiceField
- DateTimeField
- DurationField
- FilePathField
- IntegerField

to name a few

They also have some kwargs that accompany them.

- required: If True, the field may not be left blank or given a None value. Fields are required by default, so you would set required=False to allow blank values in the form.
- initial: The initial value for the field when the form is displayed.
- validators: A list of functions that will be called on the field when it is validated.
- localize: Enables the localization of form data input (see link for more information).
- disabled: The field is displayed but its value cannot be edited if this is True. The default is False.

For forms that use a POST request to sumbit information to a server, the most common pattern is to view to test agaionst a POST type to id form validation. 

if forms are not valid, you can always call the `render()` method again. 

Form tags are relitively simple you just simply pass the object through `{{ form.as_*}}`. For POST methods don't forget to use `{% csrf_token %}` to ensure resistance to csrf attacks. 