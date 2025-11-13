# Működés:

## Szerver elindítása

1. virtuális környezethez a pipenvet használom, cmd-ben: **pip install pipenv**
2. használt csomagok(flask, wtforms stb.): **pipenv install**
3. belépés virtuális környezetbe: **pipenv shell**
4. szerver futtatása: **python run.py**

## Alternatív indítás az előbbi 4. lépés helyett, kb ugyanazt érjük el vele:

1. **set FLASK_APP=quizapp.py**
2. **flask run**

## Lokális DB elkészítése:

1. cmd-ben nyitunk egy python interpretert: **python**
2. **from quizapp import app, db**
3. **app.app_context().push()**
4. **db.drop_all()**
5. **db.create_all()**

## Tesztelni így lehet a db-t python interpreterből
1. python interpreter: **python**
2. **from quizapp import app,db**
3. **app.app_context().push()**
4. **from quizapp.models import User**
5. **user = User.query.first()**

# Saját feladataim a csapatprojektben:

A quiz modul backendjének fejlesztése: adatmodellek, API végpontok, blueprint integráció.

A quiz felhasználói felületének elkészítése és az ehhez tartozó frontend útvonalak implementálása.

Adatseedelés és tesztadatok létrehozása (seed_words.py, 45 szó easy/medium/hard kategóriákban).

A projekt dokumentációjának jelentős részének elkészítése és karbantartása: funkcionális specifikáció, követelményspecifikáció, rendszerterv, deploy/maintenance plan, ERD diagram.

Tesztesetek létrehozása és újraformázása a jobb átláthatóság érdekében.
