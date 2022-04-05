# Graduation-proposal

> This Document will be submitted in partial fulfilment of the requirement for the "Introduction to Graduation Project"
> course, during the academic year 2021-2022 (2nd Semester).

## Abstract

The current scholarship system is outdated; in this day and age, everything is easy to use and manage through
technology, making it more secure, efficient, and fast at the same time. However, aside from the cost of paper, it is
neither secure nor efficient to use between universities; what if it is damaged or lost for some reason?

## Introduction

Our suggested approach ensures the security and effectiveness of the university scholarship system. In the existing
method, you are required to write everything by hand, including a lot of repetitive information, such as information
connected to the recipient university or the scholarship itself, such as ID and kind, which should be given by the
university's database system. The current system requires the grantee university to provide a specific paper for the
scholarship, which is inconvenient for something so important (this paper is the only paper for that scholarship), and
if it is damaged or lost for any reason, the grantee university must provide another paper for the same scholarship,
which is time-consuming for the recipient university or the scholarship recipient.

## Stockholders
>not added yet

## System Roles
1. System admin (**questionable**)
2. University admin (**questionable**)
3. University user

### System admin
This role represents the whole community of universities and his role is to modify 
universities e.g. remove university, add university.

### University admin
This role represents the president of the university, his role consist on 
adding other users to the university and restricting others from logging in 
to the system, and the other role for him is to accept for other universities 
as a part of the system that being added by the system admin.<br/>
And he must accept the scholarship that the user made from the university or reject it.


### University user
This role is the main role of the system, will be explained briefly in a moment.
This role has two primary set of rules:
1. Add a Scholarship.
2. Edit a scholarship.
3. View the received scholarships and add a candidate (student) to that
specific scholarship.
4. Remove an added candidate.
5. Add description to the candidate information.

### Scholarship
This entity is concerned with the scholarships that colleges can offer to other institutions in order to help students.
<br/>
Every scholarship have a set of strict rules:
1. When added (state:public/pending)
`as can be sent to anyone but a single one only
`
2. When sent can't be re-sent to anyone else, only if the university user rejected it.
3. When sent can't be edited by the source university. However, it can be duplicated as a new scholarship with a new ID and the same data.
4. When a candidate is attached to a scholarship, the university that owns the scholarship can deny or accept the candidate.
5. When a candidate is rejected, the scholarship is returned to the offered university with the same state and info before (not a new entity e.g. new ID).
6. When a 