# GarmentsPro – Database Overview

## 1. Purpose

This document is intended to describe the database structure supporting GarmentsPro, including the database platform, logical data areas, tables, keys, relationships, and reporting dependencies.

The supplied GarmentsPro project presentation demonstrates application interfaces and report options. It does not identify the database platform, database name, table names, column definitions, primary keys, foreign keys, stored procedures, views, or entity relationships.

For that reason, this document records the known scope and provides a structured format for completing the technical database documentation after the actual database and application configuration have been inspected. No database engine or schema details are assumed.

## 2. Database Platform

| Item | Verified Information |
|---|---|
| Database Management System | Microsoft SQL Server |
| Database Name | OrderStatus |
| Database Version | Microsoft SQL Server 2025 |
| Database Server / Deployment | Network Deployment |
| Connection Method | ODBC DSN-based connectivity |
| Data Access Components | Microsoft ADO Data Control (ADODC) and ODBC |

Complete this section only after checking the original application configuration, development project, and authorised database environment.

Do not publish production server names, IP addresses, usernames, passwords, connection strings, or other credentials in this public repository.

## 3. Logical Data Areas

The report titles in the presentation indicate that the application works with information in the following business areas. These are logical subject areas, not confirmed physical database tables.

| Logical Data Area | Information indicated by the presentation |
|---|---|
| Capacity and Booking | Monthly/weekly capacity, buyer summaries, booking and order reports |
| Buyer and Brand | Buyer-wise, brand-wise, and buyer-summary reporting |
| Sample Planning | Sample plan status, history, sample type, deadlines, and sending status |
| Export Orders | Order booking by month, season, buyer, merchandiser, style, and department |
| Order Allocation | Allocation plan status by date range, floor, and buyer |
| Order and Style | Order sheet details, style-wise orders, and order status |
| Yarn and Fabric | Yarn issue and fabric requirement status |
| Knitting | Knitting plan, production details, and production summary |
| Collar and Cuff | Collar and cuff production status |
| Dyeing and Testing | Dyeing plan, dyeing production, laboratory test, and dyeing delivery status |
| Accessories and CAD | Accessories status, trim card, and CAD status |
| Cutting and Sewing | Cutting production by order and size, sewing-line production, sewing status, and cut-to-slip reports |
| Shipment | Shipment information, shipment summary, and shipment details |
| Management Reporting | Capacity, booking, buyer summaries, dashboard, and sewing production chart |

These areas should be mapped to actual tables and views only after database inspection.

## 4. Table Inventory

The following inventory should be completed from the authorised database schema.

| Table Name | Business Purpose | Primary Key | Important Relationships |
|---|---|---|---|
| To be identified | To be documented | To be verified | To be verified |

For each confirmed table, document:

- Exact table name
- Business purpose
- Primary key
- Foreign keys
- Important columns and data types
- Nullability and default values where relevant
- Related tables
- Whether the table stores master, transaction, status, or reporting data

Do not create table names based only on report titles.

## 5. Relationship Documentation

The presentation does not provide an Entity Relationship Diagram (ERD) or key definitions.

After inspecting the database, document verified relationships such as:

- Buyer-related records and order records
- Order records and style information
- Order records and production follow-up records
- Order records and shipment records
- Planning records and their related business references

The actual relationship type, join columns, cardinality, and referential constraints must be confirmed from the schema. The examples above are areas to investigate, not confirmed database relationships.

## 6. Database Objects

Record the database objects found in the actual system.

| Object Type | Documentation Required |
|---|---|
| Tables | Table name, purpose, key columns |
| Views | View name, source tables, business purpose |
| Stored Procedures | Procedure name, parameters, purpose |
| Functions | Function name, return type, purpose |
| Triggers | Trigger name, target table, business rule |
| Indexes | Indexed columns and performance purpose |
| Constraints | Primary key, foreign key, unique, check, and default constraints |

If an object type is not used by the application, state that it is not used after verification.

## 7. Reporting Data Sources

The project presentation lists reports for capacity, sample planning, export order booking, allocation, production follow-up, sewing/cutting, shipment, and management reporting.

For each report, record the verified data source and calculation logic.

| Report / Report Group | Source Object(s) | Main Filters | Calculation / Business Rule |
|---|---|---|---|
| Capacity reports | To be verified | To be verified | To be verified |
| Sample planning reports | To be verified | To be verified | To be verified |
| Export order booking reports | To be verified | To be verified | To be verified |
| Order allocation reports | To be verified | To be verified | To be verified |
| Production follow-up reports | To be verified | To be verified | To be verified |
| Sewing and cutting reports | To be verified | To be verified | To be verified |
| Shipment reports | To be verified | To be verified | To be verified |
| MIS and dashboard reports | To be verified | To be verified | To be verified |

## 8. Entity Relationship Diagram

Add the verified database diagram to:

`Database/ERD/GarmentsPro-ERD.png`

If the diagram is maintained in an editable format, include the source file as well, provided it contains no confidential information.

Embed the diagram here after it has been prepared:

```markdown
![GarmentsPro Entity Relationship Diagram](../Database/ERD/GarmentsPro-ERD.png)
```

Do not publish an illustrative or guessed ERD as if it represented the actual database.

## 9. Data Security and Public Repository Guidelines

Before publishing database-related material:

- Remove server names, IP addresses, usernames, passwords, and connection strings.
- Do not upload production database backups.
- Do not publish real buyer, supplier, employee, order, or shipment data.
- Use anonymised sample records if examples are required.
- Review scripts for hard-coded credentials and confidential business rules.
- Confirm that the developer has permission to publish any schema or database script.

## 10. Technical Verification Checklist

Complete the following items after inspecting the original development and database environment:

- [ ] Identify the database platform and version.
- [ ] Identify the database name, without exposing production connection details.
- [ ] Export or document the table inventory.
- [ ] Identify primary and foreign keys.
- [ ] Document verified table relationships.
- [ ] Identify views, stored procedures, functions, and triggers.
- [ ] Identify indexes and important constraints.
- [ ] Map major reports to their source objects.
- [ ] Prepare and review the ERD.
- [ ] Remove confidential information before publication.

## 11. Related Documentation

- [Project Overview](Project-Overview.md)
- [Functional Modules](Functional-Modules.md)
- [Business Workflow](Business-Workflow.md)
- [User Guide](User-Guide.md)
