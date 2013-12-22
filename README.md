# Django Bootstrap Markdown Editor

## A beautiful Markdown editor with a side by side preview

An extension of the Django Textarea widget made for editing [Markdown](http://daringfireball.net/projects/markdown/) with a live preview.

![Example](http://thegoods.aj7may.com/content/images/2013/Dec/Screen_Shot_2013_12_21_at_2_39_47_PM.png)

### Install:
`> pip install django-bootstrap-markdown`

### Usage:

* Add `django-bootstrap-markdown` to the installed apps of your Django Project
* Instead of using the django `Textarea` widget use the `MarkdownInput`
* Be sure to include the form's required media in the template. _ie._ `{{ form.media }}`
* Also be sure to include [Twitter Bootstrap](http://getbootstrap.com/)

### Example:

_forms.py_

	from django import forms
	from django_bootstrap_markdown.widgets import MarkdownInput
    
    class PostForm(forms.Form):
    	title = forms.CharField()
    	markdown = forms.CharField( widget=MarkdownInput )