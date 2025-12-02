# DynamoDBForge

---

## 🔥 Overview

**DynamoDBForge** is a high-performance, scalable, and fully managed NoSQL database repository built on AWS DynamoDB.
It focuses on speed, flexibility, and reliability for modern cloud applications.

This repository demonstrates **key DynamoDB concepts**, **best practices**, and **hands-on implementations** for real-world usage.

---

## 🚀 Features

* Fully managed NoSQL database on AWS
* Ultra-fast read/write operations
* Scalable and serverless
* Flexible schema design
* High availability and durability
* Ideal for real-time applications and analytics

---

## 🛠️ Core Concepts

1. **Tables** – Organize your data in DynamoDB tables with partition keys and optional sort keys.
2. **Items** – Individual records stored in tables (like rows in relational DBs).
3. **Attributes** – Fields within each item (like columns).
4. **Primary Keys** – Unique identifiers for each item.
5. **Secondary Indexes** – Query flexibility beyond the primary key.
6. **Provisioned & On-Demand Capacity** – Manage throughput and costs efficiently.
7. **Streams** – Capture table changes in real-time for event-driven applications.

---

## 📦 Step-by-Step Creation Guide

### 1. Create a DynamoDB Table

```bash
aws dynamodb create-table \
    --table-name DynamoDBForgeTable \
    --attribute-definitions AttributeName=ID,AttributeType=S \
    --key-schema AttributeName=ID,KeyType=HASH \
    --provisioned-throughput ReadCapacityUnits=5,WriteCapacityUnits=5
```

### 2. Insert Items

```bash
aws dynamodb put-item \
    --table-name DynamoDBForgeTable \
    --item '{"ID": {"S": "1"}, "Name": {"S": "Arkan"}, "Role": {"S": "Developer"}}'
```

### 3. Query Items

```bash
aws dynamodb get-item \
    --table-name DynamoDBForgeTable \
    --key '{"ID": {"S": "1"}}'
```

### 4. Update Items

```bash
aws dynamodb update-item \
    --table-name DynamoDBForgeTable \
    --key '{"ID": {"S": "1"}}' \
    --update-expression "SET Role = :r" \
    --expression-attribute-values '{":r": {"S": "Senior Developer"}}'
```

### 5. Delete Items

```bash
aws dynamodb delete-item \
    --table-name DynamoDBForgeTable \
    --key '{"ID": {"S": "1"}}'
```

---

## 📝 Best Practices

* Use **Partition Keys** wisely to distribute load evenly
* Avoid hot partitions
* Use **On-Demand Capacity** for unpredictable workloads
* Monitor table metrics with **CloudWatch**
* Enable **Streams** for real-time updates

---

## ⚡ Use Cases

* Real-time analytics
* E-commerce product catalogs
* IoT data storage
* Serverless applications
* Mobile and web apps

---

## 🔗 Resources

* [AWS DynamoDB Documentation](https://docs.aws.amazon.com/dynamodb/)
* [AWS SDKs](https://aws.amazon.com/tools/)
* [DynamoDB Best Practices](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/best-practices.html)

---

## 👤 Author Info

**Arkan Tandel**
**GitHub:** [arkantandel](https://github.com/arkantandel)
**LinkedIn:** [Arkan Tandel](https://www.linkedin.com/in/arkantandel)


