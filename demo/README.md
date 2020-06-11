# Example of integration with MongoDB as default DB and a local SQLite as buffer

## How to use: 

```sh
# Customize the demo/settings.py
pip install -r requirements.txt
python manage.py migrate
python manage.py migrate --database=local_db
python runserver.py
```


## Comments

Putting everything in a single database makes the plotly app slower than wanted. (1s/change) 
You can do it by modifying the ../django_plotly_dash/migrations/0001 file and removing the altertable, adding the foreign key integration in the first step of database creation.


