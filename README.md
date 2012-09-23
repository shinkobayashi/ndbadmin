Admin panel for ndb.Model
=========================

This is live application to demonstrate admin UI.
I developed this admin panel for my own usage.

In this app Admin panel use twitter bootstrap CSS style.


Meta
====

All work is done inside your ndb.Model() model. Add Meta() class inside it,
where to be defined create/edit form fields and templates for list/new/edit/delete item(s).

Example:

	class Meta():
        def __init__(self):
            self.fields = [
                fields.TextField("name", "Name", required=True),
                fields.BigTextField("description", "Description")
            ]


Fields
======

Admin UI use HTML 5 fields types and validation.

Now CRUD has next types of fields available to use:

 * TextField - input type text
 * BigTextField - input type textarea
 * CheckboxField - checkbox
 * CheckboxListField - list/group of checkboxes (useful for repeated NDB properties)
 * GeoField - input text for geo "lat, lon" comma separated pair
 * KeyField - select with list of objects for foreign key relations
 * ChoiceField - select with list of strings for choise values list
 * IntegerField - input type number (with spinner in most browsers)
 * MoneyField - input type text, styled with twitter bootstrap CSS
 * DateField - input type date

Fields options:

 * field - model field name
 * label - string with label for html elementh
 * initial - initial value
 * required - false by default
 * query - in choise and key fields indicate a list of values/options


TODO
====

 * Tests
 * Better documentation
