# Manual Migrations and Downgrades

## Learning Goals

- Use an external library to simplify tasks from ORM and Advanced ORM.
- Manage database tables and schemas without ever writing SQL through Alembic.
- Use SQLAlchemy to create, read, update and delete records in a SQL database.

***

## Key Vocab

- **Persist**: save a schema in a database.
- **Engine**: a Python object that translates SQL to Python and vice-versa.
- **Session**: a Python object that uses an engine to allow us to
  programmatically interact with a database.
- **Transaction**: a strategy for executing database statements such that
  the group succeeds or fails as a unit.
- **Migration**: the process of moving data from one or more databases to one
  or more target databases.

***

## Introduction

In the last lesson, we started working with Alembic to generate and carry out
migrations, or changes to the database schema. Alembic is a powerful tool when
used with the SQLAlchemy ORM, and it can generate migrations that account for
many of the common changes we might make to a database schema:

- Creating and dropping tables.
- Creating and dropping columns.
- Most indexing tasks.
- Renaming keys.

That being said, there are certain tasks that Alembic can help us with but
cannot carry out on its own:

- Table name changes.
- Column name changes.
- Adding, removing, or changing constraints without explicit names.
- Converting Python data types that are not supported by the database.

In this lesson, we will explore writing manual migrations and how to roll back,
or **downgrade**, migrations that were unnecessary or went awry.

***

## Instructions

If you have not already, run `pipenv install` to create your virtual
environment and `pipenv shell` to enter the virtual environment.

- Rename a column in the `Student` model.
- Manually generate a migration using Alembic.
- Upgrade your database schema with `alembic upgrade head`.

Once your database schema has been upgraded, commit and push your work using
`git` to submit.

***

## Conclusion

<!-- Managing migrations is an important skill for a full-stack developer to keep
in their toolbox. Alembic is a powerful tool for carrying out migrations and
can handle most tasks automatically. That being said, Alembic can't do
_everything_ on its own. In the next lesson, we will explore how to manually
configure migrations and downgrade to revert to an earlier state. -->

***

## Resources

- [SQLAlchemy ORM Documentation](https://docs.sqlalchemy.org/en/14/orm/)
- [SQLAlchemy ORM Column Elements and Expressions](https://docs.sqlalchemy.org/en/14/core/sqlelement.html)
- [Tutorial - Alembic](https://alembic.sqlalchemy.org/en/latest/tutorial.html)
