# Django Bootstrap Markdown Editor

## A beautiful Markdown editor with a side by side preview

[![Build Status](http://img.shields.io/travis/aj-may/django-bootstrap-markdown.svg)](https://travis-ci.org/aj-may/django-bootstrap-markdown)
[![Coverage Status](http://img.shields.io/coveralls/aj-may/django-bootstrap-markdown/master.svg)](https://coveralls.io/r/aj-may/django-bootstrap-markdown)
[![Code Climate](http://img.shields.io/codeclimate/github/aj-may/django-bootstrap-markdown.svg)](https://codeclimate.com/github/aj-may/django-bootstrap-markdown)
[![License](http://img.shields.io/pypi/l/django-bootstrap-markdown.svg)](https://github.com/aj-may/django-bootstrap-markdown/blob/master/LICENSE.md)
[![Version](http://img.shields.io/pypi/v/django-bootstrap-markdown.svg)](https://pypi.python.org/pypi/django-bootstrap-markdown)
[![PyPI Downloads](http://img.shields.io/pypi/dm/django-bootstrap-markdown.svg)](https://pypi.python.org/pypi/django-bootstrap-markdown)
[![GitTip](http://img.shields.io/gittip/aj_may.svg)](https://www.gittip.com/aj_may/)

An extension of the Django Textarea widget made for editing [Markdown](http://daringfireball.net/projects/markdown/) with a live preview.

![Example](http://thegoods.aj7may.com/content/images/2013/Dec/Screen_Shot_2013_12_21_at_2_39_47_PM.png)

### Install:
`> pip install django-bootstrap-markdown`

### Usage:

* Add `django-bootstrap-markdown` to the installed apps of your Django Project
* Instead of using the django `Textarea` widget use the `MarkdownInput`
* Be sure to include the form's required media in the template. _ie._ `{{ form.media }}`
* Also be sure to include [Twitter Bootstrap](http://getbootstrap.com/)
* Include the markdown urls:

_urls.py_

	urlpatterns = patterns('',
	    ...
	    url(r'^markdown/', include('django_bootstrap_markdown.urls')),
	    ...
	)

### Example:

_forms.py_

	from django import forms
	from django_bootstrap_markdown.widgets import MarkdownInput
    
    class PostForm(forms.Form):
    	title = forms.CharField()
    	markdown = forms.CharField( widget=MarkdownInput )
