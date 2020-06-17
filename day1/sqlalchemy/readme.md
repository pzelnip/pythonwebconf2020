# SQL Alchemy TUtorial

<https://2020.pythonwebconf.com/tutorials/introduction-to-sqlalchemy>

<https://github.com/zzzeek/sqla_tutorial>

Mike Bayer (Red Hat)

## Abstract

In this tutorial, we present a "from the ground up" tour of SQLAlchemy, what the
general idea of it is, how it's organized, and what it looks like to use it.
This is the latest version of the "classic" SQLAlchemy tutorial  which has been
presented on many occasions since 2008, reworked for the current recommended
SQLAlchemy usage patterns with an emphasis on previewing the upcoming 1.4 and
2.0 releases of SQLAlchemy, which are poised to make major changes to many of
SQLAlchemy's central paradigms and capabilities. SQLAlchemy is presented in
terms of a four-layered model, which include "Engine and Connection Basics",
"Table Metadata", "SQL Expression Language", and "ORM Usage" which is broken
into two sections and API use is presented in terms of a console runner
application which participants can install locally and follow along.   The
tutorial will also present some of the newest in-development features of
SQLAlchemy 1.4 which have only just merged.

## Notes

Overview of SQLalchemy

Spent 15 mins getting into the Zoom call.

Spent a chunk of time going over low level details that seemed unimportant for a tutorial.

## Engine basics

went through `01_engine_usage.py`

So much content is the diffs between 1.4 & 2.0, very little explanation of basic
concepts in SQLAlchemy

6:41 still going through 01_engine_usage.py, just various examples of doing raw
SQL, no discussion of ORM yet.

Sounds like 1.4/2.0 is still in flight under heavy dev.

6:43 finished 01_engine, took some questions.

6:45 moved to next section, Table metadata, reflection, and DDL

## Metdata

02_metadata.py

Now starting to get into higher level constructs.
6:58 finished the metadata example, going very fast at this point.
Continued on metadata slides: basic types, create and drop,

Finished at 7:01 moved onto core sql expression language

## Core Sql Expression Language

slides then 03_sql_basic.py

7:19 finished code example

10-ish minute break

## SQL Advanced

03_sql_adv.py

Examples of doing joins, subqueries, etc

7:57 ended this section

## Level 4, ORM

Overview of ORMs, what they do, etc.

Flavours of ORMs:

* Active Record
* Data Mapper

04_orm_basic.py @ 8:05, stopped for bathroom break

Basic examples of creating Base and deriving from it to declare object/DB mappings
Queries, etc

8:37 moved onto 04_orm_advanced.py

8:50 to 8:53-ish frantic sprint to everything except what's new in 1.4/2.0.
Last few mins was what's new which if you ahven't done sqlalchemy is totally over your head
