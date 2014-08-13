# O-Car-Go - Integrate branch

This integrate branch is to keep separate (initially) the transition from using Ocargo as a separate application to using it through a central Deploy application (see the [codeforlife-deploy](http://github.com/ocadotechnology/codeforlife-deploy/) repository).

## Previous README text:

O-Car-Go is a 'Coding For Life' project, aimed at teaching children programming concepts through a vehicle routing game. It is a Django based web application.

To run the app, you'll need the dependencies found in requirements.txt. If you've got pip installed, just run `pip install -r requirements.txt` at the top level of the project (you may need to prefix that with `sudo`). You may want to use a [virtualenv](http://virtualenv.readthedocs.org/en/latest/).

Run `python manage.py collectstatic` to gather static files into a place where the webserver can find them.

Run `python manage.py syncdb` to create the database schema and populate it with initial data. This defaults to sqlite, but can be altered in settings.py.

To start the development server, run `python manage.py runserver` with optional address:port, where `python manage.py runserver 0.0.0.0:8000` will start the development server accessible to any machine that can find your IP address on port 8000. By default with no arguments, `runserver` will be only accessible to localhost on port 8000.

When you pull changes, you may need to `collectstatic` again, and will need to wipe the database schema (delete sqlite file or `manage.py sqlclear`) and re-create it (`manage.py syncdb`) if there have been schema changes.

## Branches

Most of the work happens on "master", which gets deployed automatically to [dev](http://dev.numeric-incline-526.appspot.com).

Changes for the next deployment go on "staging", which gets deployed automatically to [test](http://testing.numeric-incline-526.appspot.com).

Production - tbd.

## Useful links:
- [Google Group Forum](https://groups.google.com/a/ocado.com/forum/#!forum/coding-for-life-dev-xd)
- [Google Group Email](mailto:coding-for-life-dev-xd@ocado.com)
- [Google Drive folder](https://drive.google.com/a/ocado.com/folderview?id=0BydFxJnM7i7yRUlfUkFJV1R4bU0&usp=sharing)
