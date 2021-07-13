## Vagrant
Befehle:
|Name|Funktion|
|----|--------|
|``vagrant ssh``|Vagrant Server starten|

Im Vagrant Server:
./vagrant ist gemapptes Verzeichnis zum Projektverzeichnis

## Python

### Virtual environment
``python -m venv ~/env``
Erstellt neues Python environment in ~/env, damit sich die Umgebung nicht mit der lokalen Maschine synchronisiert
``source ~/env/bin/activate``
Umgebung aktivieren
``deactivate``
Umgebung deaktivieren

Alle benötigten packages sind in requirements.txt
Requirements installieren: ``pip install -r requirements.txt`` (In virtual environment)

Django-Projekt erstellen ``django-admin.py startproject profiles_project .``
App in Django-Projekt erstellen ``python manage.py startapp profiles_api``

App in Projekt enablen: settings.py in profiles_project bearbeiten