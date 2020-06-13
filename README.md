# http-localhost-8888-notebooks-PycharmProjects-George-20scheduler.ipynb

connfig import config


def create_tables():
    """ create tables in the PostgreSQL database"""
    commands = (
        """
        CREATE TABLE George Scheduler App (
            User_id SERIAL PRIMARY KEY,
            User_name VARCHAR(255) NOT NULL
        )
        """,
        
        
        
