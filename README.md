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
        
        
        
        
        
        
