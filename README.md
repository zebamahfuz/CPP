# Real Estate Django Web App

A real estate listings website built with `python` `django` `bootstrap`.

A simple, reponsive  website. Built with:

- Python 🐍
- Django 🎸
- Bootstrap 4 🌈
- Vanilla JS - ES6
- JQuery
## How to run this project (Ubuntu 18.04)

1. **Clone the project**

```sh
git clone https://github.com/zebamahfuz/CPP.git
```

2.  **Make sure you are in *CPP* folder**

   1. Install all dependencies

      ```sh
      pip install -r requirements.txt
      ```

3. **Install PostgreSQL in your Ubuntu 18.04**

   1. Enable PostgreSQL Apt Repository

      ```sh
      sudo apt-get install wget ca-certificates
      
      wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
      
      # Now add the repository to your system.
      
      sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt/ `lsb_release -cs`-pgdg main" >> /etc/apt/sources.list.d/pgdg.list'
      ```

   2. Install PostgreSQL on Ubuntu

      ```sh
      sudo apt-get update
      sudo apt-get install postgresql postgresql-contrib
      ```

   3. Connect to PostgreSQL

      ```sh
      sudo su - postgres
      psql
      ```

      Now you are logged in to PostgreSQL database server. To check login info use following command from the database command prompt.

      ```sh
      postgres-# \conninfo
      ```

   4. Create a database

      ```sh
      CREATE DATABASE real_estate;
      ```

   5. Create user 

      ```sh
      CREATE USER pks WITH PASSWORD 'abc123!';
      ```
   
4. **Run Migrations**

```sh
python manage.py makemigrations
python manage.py migrate
```

5. **Run Server**

```sh
python manage.py runserver 
```

And you are good to go. 


**To run with SQLite only**

Go inside the 'realestate' folder and open 'settings.py' file and replace

```sh
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'real_estate' ,
        'USER': 'pks',
        'PASSWORD': 'abc123!',
        'HOST':'localhost',
        
    }
}
```

To: 

```sh
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': os.path.join(BASE_DIR, 'db.sqlite3'),
    }
}

```

This is the default configuration of Django database.


**Backend**
![RDS Database ](realestate.chwlezgyi7rm.eu-west-1.rds.amazonaws.com:5432)
For Database I have used AWS RDS Postgres Database Name: realestate

- **Lambda API Endpoint**

![Lambda API Endpoint ](https://v4dmr8sz3i.execute-api.eu-west-1.amazonaws.com/default/zeba)

## Acknowledgments

Many thanks to [@bradtraversy](https://github.com/bradtraversy) for his awesome course.

##### References

1. https://www.traversymedia.com/
2. https://www.djangoproject.com/
