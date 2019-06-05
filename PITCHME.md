---?color=#111D39
## CockroachDB: Reads and Writes
@snap[south]
Will Cross, Director of Training
@snapend
---?color=#111D39
@snap[north-west]
### Agenda
@snapend

@ol
- How is data stored in CockroachDB?
- How do reads & writes happen locally?
- How is data replicated/distributed?
- How do reads & writes happen in a cluster?
- How does CockroachDB tolerate failures?
- How does CockroachDB guarantee consistency?
@olend
---
@snap[north span-100]
### How is Data Stored in CockroachDB?
@snapend

@ul[west span-70]
- *Bad question!*
- Better:
  - How are tables stored in CockroachDB?
  - How are indexes stored?
@ulend

@snap[east span-30]
![Dunce Cap](https://static.tvtropes.org/pmwiki/pub/images/dunce_hat.jpg)
@snapend

---
@snap[north span-100]
### How are Indexes Stored in CockroachDB
@snapend
@ul[west span-70]
- Indexes are _also_ in RocksDB
  - Key is the index key\* used to look up data
  - Value is the primary key of the table row that is pointed to\*\*
  - *Ordered by index key*
@ulend

```SQL
> SELECT * FROM animals;  -- primary key is id, we index common_name
                                   
  id |        species         | common_name |                                description
+----+------------------------+-------------+---------------------------------------------------------------------------+
   1 | Felis catus            | cat         | Small semi-domesticated predator known for its soft fur and sharp claws
   2 | Canis lupus familiaris | dog         | Domesticated predator known for its loyalty and intelligence
   3 | Ursus maritimus        | polar bear  | Large wild predator with white fur that lives mostly in the Arctic Circle
```
---


@snap[north span-100]
## What's Write the Docs?
@snapend

@snap[east span-70]
“**Write the Docs** is a global community of people who care about documentation.

The Write the Docs conference includes Writing Day, traditional conference-style talks, an Unconference, and a job fair.”
@snapend

---

## What's Writing Day?

“This event is to get a bunch of interesting people in a room together and have them work towards shared goals.”

The vibe was like a Fixit Day.

---

## Prepping for Writing Day

@ul

- Worked with Lucia to create usability testing for our docs search
- Groomed our GitHub issues
- Added our project description to the [official Writing Day page](https://www.writethedocs.org/conf/portland/2019/writing-day/#write-cockroachdb-docs)
    - Amruta led this effort last year, so thank you for your pre-work!
- Publicized our project on Write the Docs Slack

@ulend

---

## This is a new slide

Blah!

---

## This is another slide

- Blah
- Blah
- Blah
