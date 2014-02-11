Milkman - Easy django model object generation
=============================================

Quick Examples
--------------

	from milkman.dairy import milkman
	from myapp.models import Video, Editor

	#I just want a random video in the db to test with
	v = milkman.deliver(Video)

	#I want a video with a particular editor
	e = milkman.deliver(Editor)
	v = milkman.deliver(Video, editor=e)


Development
-----------
Install virtualenv and virtualenvwrapper

http://www.virtualenv.org/en/latest/index.html

http://pypi.python.org/pypi/virtualenvwrapper

    mkvirtualenv milkman
    pip install -r requirements.txt


Running Tests
-------------

    cd testapp
    ./manage.py test

In addition you can install [the tox testing tool](http://tox.testrun.org/) to quickly run the tests against multiple installed versions of Python and Django.

Once tox has been installed you can run tests from the source directory with `tox`. This will build virtual environments for the versions defined in the file tox.ini and then install and test the source in each.


Known Issues
------------
Several of the basic django model fields have generators, although most do not.  Let us know if there is a particular field to be implemented thats really bugging you, or just send a patch :)
