# http-localhost-8888-notebooks-PycharmProjects-George-20scheduler.ipynb

import psycopg2
from config import config

def create_tables():
    """ create tables in the PostgreSQL database"""
    commands = (
        """
        CREATE TABLE George Scheduler App (
            User_id Integer PRIMARY KEY,
            User_name VARCHAR(255) NOT NULL,
            Assigned_to CHAR (255) NOT NULL,
            Task _Description CHAR (255) NOT NULL,
            Deadline_date  (int) not null,
        )
        """,
        
rom . import db

class Wizard(UserMixin, db.Model):
    """
        Represents a wizard who can access special parts of the application.
    """
    __tablename__ = 'George Scheduler'
    User_id = db.Column(db.Integer, primary_key=True)
    Assigned_to = db.Column(db.String(64), unique=True, index=True)
    Task _Description CHAR (255) NOT NULL,
    Deadline_date  (int) not null,
     )"""
     '
    password_hash = db.Column(db.String(128))

    def __init__(self, wizard_name, password):
        self.wizard_name = wizard_name
        self.password = password
        
      
        
        def config(filename='database.ini', section='postgresql'):
    # create a parser
    parser = ConfigParser()
    # read config file
    parser.read(filename)

    # get section, default to postgresql
    db = {}
    if parser.has_section(section):
        params = parser.items(section)
        for param in params:
            db[param[0]] = param[1]
    else:
        raise Exception('Section {0} not found in the {1} file'.format(section, filename))

    return db
The following connect() function connects to the suppliers database and prints out the PostgreSQL database version.

#!/usr/bin/python
import psycopg2
from config import config

def connect():
    """ Connect to the PostgreSQL database server """
    conn = None
    try:
        # read connection parameters
        params = config()

        # connect to the PostgreSQL server
        print('Connecting to the PostgreSQL database...')
        conn = psycopg2.connect(**params)
		
        # create a cursor
        cur = conn.cursor()
        
	# execute a statement
        print('PostgreSQL database version:')
        cur.execute('SELECT version()')

        # display the PostgreSQL database server version
        db_version = cur.fetchone()
        print(db_version)
       
	    # close the communication with the PostgreSQL
        cur.close()
    except (Exception, psycopg2.DatabaseError) as error:
        print(error)
    finally:
        if conn is not None:
            conn.close()
            print('Database connection closed.')


if __name__ == '__main__':
    connect()
        
        
