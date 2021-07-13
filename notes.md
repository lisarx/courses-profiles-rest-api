## Vagrant
Befehle:
|Name|Funktion|
|----|--------|
|``vagrant ssh``|Vagrant Server starten|

Im Vagrant Server:
./vagrant ist gemapptes Verzeichnis zum Projektverzeichnis

## Virtual environment
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

Entwicklungsserver starten python ``manage.py runserver 0.0.0.0:8000``

Jetzt sieht man auf localhost:8000 die Seite, dass das Django Projekt erfolgreich erstellt wurde

## Django Models
- Models: Daten Beschreibung der Daten, die wir für die Anwendung brauchen.
- Django erstellt und konfiguriert dadurch unsere Datenbank.
- Jedes Model in Django bezieht sich auf eine bestimmte Datenbanktabelle.
- Dadurch müssen wir nie direkt SQL Statements schreiben, sondern alles läuft über Django.
- Models werden in models.py definiert (in App Ordner)

## Unsere Models im Projekt:
### UserProfile
- ``email = models.EmailField(max_length=255, unique=True)`` Sagt, dass wir eine email Spalte wollen, die ein EmailField ist mit maximal 255 Zeichen und keine Emails doppelt eingetragen werden dürfen (Keine zwei Accounts pro Mailadresse erlaubt)
- ``name = models.CharField(max_length=255)`` Definiert ein Textfeld, das name heißt
- ``is_active = models.BooleanField(default=True)`` Booleanfeld - ist das Profil aktiviert, oder nicht?


## Python allgemein
"""asd""" ist ein Docstring
class MyClass(ParentClass) -> Vererbung
zwischen zwei Klassendefinitionen immer zwei leere Zeilen

## Good to know!
Bei E-Mail Adressen ist IDR der erste Teil vor dem @ Case sensitive -> Ich kann lrex@protonmail.com != Lrex@protonmail.com
und der hintere Teil Case insensitive -> lrex@protonMail.com == lrex@protonmail.com
-> Deswegen immer hinteren Teil der Mail als Kleinbuchstaben speichern, um nicht die Konten lrex@protonmail.com UND lrex@protonMail.com zu erlauben