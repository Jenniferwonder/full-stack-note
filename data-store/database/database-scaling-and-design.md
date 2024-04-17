---
title: Database Scaling and Design
type: 
tags:
  - Database
  - System
DateStarted: 2023-12-27
DateModified: 2024-04-17
status: 
---

## [Database](Database.md) Scaling and Design

Performance bottleneck  
Read heavy, around 95%+

### Basic Scaling Techniques

#### 1. Indexes

- Index based on column
- Speeds up read performanceWrites and updates become slightly slower
- More storage required

#### 2. Denormalization

- Go against a standard best practice with relational databases
- Add redundant data to tales to reduce joins
- Boosts read performance
- Slows dorn writes
- Risk inconsistent data across tables
- Code is harder to write

#### 3. Connection Pooling

- Allow multiple application threads to use same DB connectionSaves on overhead of independent DB connections

#### 4. Caching

#### 5. Vertical Scaling

- Get a bigger server, with fast processor or more memory

### Replication and Partitioning

#### 1. Read Replicas

- Create replica servers to handle reads
- Master server dedicated only to writes
- Have to handle making sure new data reaches replica

#### 2. Sharding

- Horizontal partitioning

#### 3. Vertical Partition

- Divide schema of DB into separate tables
- Generally divide by functionality
- Best when most data in row isn't need for most queries

### When to consider NoSQL

Know what you're gonna sacrifice

- Consistency > SQL
- Scale > NoSQL
