# GarmentsPro – Business Workflow

## 1. Purpose

This document describes the business workflow areas represented in the GarmentsPro project presentation. It explains how the application’s planning, order, production follow-up, sewing/cutting, shipment, and reporting views relate to the garment order lifecycle.

The presentation shows application screens and report options. It does not provide a complete formal process specification, transaction sequence, approval matrix, or system integration design. The workflow below is therefore a business-level representation of the areas evidenced by the presentation, not a claim that every step is automatically triggered by the software.

## 2. High-Level Workflow

The business areas can be viewed in the following broad sequence:

1. Capacity planning and review
2. Sample planning and follow-up
3. Export order booking
4. Order allocation planning
5. Order-wise production and process follow-up
6. Sewing and cutting status monitoring
7. Shipment information and status review
8. MIS reporting and management review

Some activities may run in parallel or be revisited as order information changes. The exact operational sequence should be confirmed with the business users.

## 3. Capacity Planning and Review

Capacity-related reports provide monthly and weekly views, buyer summaries, booking information, and a dashboard.

Typical review dimensions shown in the presentation include:

- Month and ship-date range
- Department
- Buyer and brand
- Country-wise breakdown for a listed H&M capacity report
- Merchandiser head
- Product
- Booking and order information

**Workflow purpose:** Review capacity and booking information to support planning and management discussions.

**Presentation evidence:** Monthly capacity, weekly capacity, buyer summaries, booking report, monthly booking and order report, dashboard, and sewing production chart.

## 4. Sample Planning and Follow-up

The sample planning report set provides status and history views for sample-related activities.

The presentation identifies reports by:

- Buyer
- Order number
- Style
- Sample type
- Merchandiser
- Cut plan
- Sewing start and finish dates
- Print and embroidery sent date
- Date range
- Sample deadline
- Sample sending status

**Workflow purpose:** Review sample plan progress and related dates, identify sample plans listed as not done, and examine historical or filtered sample status.

The presentation does not define sample approval stages, sample categories beyond the report filter, or the precise meaning of each status. Those details should be confirmed in the application.

## 5. Export Order Booking

The export order booking reports provide different views of booked orders.

The available report groupings shown include:

- Booking month, season, and buyer
- Ship-date range and buyer
- Ship-date range and buyer with location
- Month-wise view for all buyers
- Merchandiser
- Style
- Department
- Ship-date sorting for selected report types

**Workflow purpose:** Review booked export orders using business and time-based groupings.

The presentation establishes report availability but does not describe the order-entry procedure, booking approval process, or source of booking data.

## 6. Order Allocation Planning

The order allocation planning reports provide:

- Date-range and floor-wise order allocation plan status
- Date-range and buyer-wise order allocation plan status

**Workflow purpose:** Review order allocation planning from floor and buyer perspectives over a selected date range.

The allocation rules, capacity constraints, and planning calculations are not specified in the presentation.

## 7. Order-wise Production and Process Follow-up

The order-wise report list covers several process areas associated with garment manufacturing.

### 7.1 Order and General Follow-up

- Order-wise production status
- Order sheet details
- Buyer/season-wise order list
- Buyer/season/colour-wise order list
- Shipped and unshipped order lists

### 7.2 Material and Upstream Process Follow-up

- Yarn issued status
- Fabric requirement status
- Knitting plan status
- Knitting production details and summary
- Collar and cuff production status
- Dyeing plan status
- Dyeing production status
- Laboratory test status
- Dyeing delivery status
- Accessories status
- CAD status

### 7.3 Cutting and Sewing Follow-up

- Sewing-line production status
- Cutting production status by order and size
- Sewing status by date, floor, month, year, order, and line
- Cut-to-slip status by date and floor, and by month and year

**Workflow purpose:** Provide order-level report views across the production-related activities represented in the presentation.

The presentation does not define the detailed hand-off rules, quantity reconciliation rules, or whether these process records are entered directly in GarmentsPro or obtained from another source.

## 8. Sewing and Cutting Status Review

Sewing and cutting reports allow information to be reviewed using several operational dimensions.

| Report View | Purpose indicated by the report title |
|---|---|
| Date and floor-wise sewing status | Review sewing status by date and floor |
| Date and floor-wise cut-to-slip report | Review cut-to-slip information by date and floor |
| Month and year-wise sewing status | Review sewing status by reporting period |
| Month and year-wise cut-to-slip status | Review cut-to-slip status by reporting period |
| Order-wise sewing status | Review sewing status for an order |
| Line-wise sewing status | Review sewing status by line |

The report titles do not specify the exact measures, formulas, or status definitions displayed.

## 9. Shipment Information and Review

Shipment reports provide views by buyer, season, department, and ship-date range.

The presentation lists:

- Buyer and season-wise shipment information
- Buyer, season, and department-wise shipment information
- Ship-date range and buyer-wise shipment information
- Ship-date range and buyer-wise shipment summary status
- Ship-date range and buyer-wise shipment information details

**Workflow purpose:** Review shipment information and shipment status using the listed business filters.

The presentation does not specify carrier integration, shipping-document generation, customs processing, or shipment approval functionality. These should not be assumed to be application features without further verification.

## 10. MIS and Management Review

The reporting area brings together several management views, including:

- Monthly and weekly capacity
- Buyer and brand summaries
- Merchandiser-head summaries
- Booking reports
- Monthly booking and order reports
- Dashboard
- Sewing production chart

**Workflow purpose:** Support periodic operational review and provide management with structured views of capacity, booking, order, and production-related information.

The KPI definitions, dashboard refresh method, and calculation logic should be documented after reviewing the actual application and its data sources.

## 11. Workflow Summary

```text
Capacity Planning and Review
          |
          v
Sample Planning and Follow-up
          |
          v
Export Order Booking
          |
          v
Order Allocation Planning
          |
          v
Order-wise Production and Process Follow-up
          |
          v
Sewing and Cutting Status Review
          |
          v
Shipment Information and Status Review
          |
          v
MIS Reporting and Management Review
```

This diagram is a simplified business-level view of the functional areas shown in the presentation. It should not be interpreted as a strict software-enforced sequence. Sample planning, capacity review, and reporting may take place at different points and may be revisited during order execution.

## 12. Related Documentation

- [Project Overview](Project-Overview.md)
- [Functional Modules](Functional-Modules.md)
- [Database Overview](Database-Overview.md)
- [User Guide](User-Guide.md)
