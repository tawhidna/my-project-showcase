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

# OrderStatus Database Inventory

## 1. Overview

| Property | Value |
|---|---:|
| Database | `OrderStatus` |
| Schema | `dbo` |
| Base tables | 264 |
| Views | 250 |
| Total database objects listed | 514 |

> **Documentation status:** Generated from the supplied object inventory. The source contains schema, object names, and object types only. Business purposes, primary keys, and relationships have not been verified against database definitions. All such fields are therefore marked as unverified.

## 2. Table Inventory

| # | Table Name | 
|---:|---|---|---|---|
| 1 | `access_spe_currency` |
| 2 | `access_spe_item_cat` | 
| 3 | `access_spe_kpi_cat` |
| 4 | `access_spe_kpi_score` | 
| 5 | `access_spe_kpi_subcat` | 
| 6 | `access_spe_purchase_order` | 
| 7 | `access_spe_suppliers` | 
| 8 | `Accessories` | 
| 9 | `accessories_categories` |
| 10 | `accessories_delivery` |
| 11 | `accessories_delivery_items` |
| 12 | `accessories_items` | 
| 13 | `accessories_stock_in_out` | 
| 14 | `accessories_stock_receive` | 
| 15 | `accessories_stock_receive_items` |
| 16 | `accessories_stock_summary` | 
| 17 | `AccQ_MonthCap` | 
| 18 | `ActiveHDTools-W` |
| 19 | `ActivePrinter-W` | 
| 20 | `ActiveRTA-W` ||
| 21 | `ActiveScanner-W` |  
| 22 | `ActiveSwitch-W` |  
| 23 | `ActiveUser` |  
| 24 | `ActiveUserAC` |  
| 25 | `address_cities` |  
| 26 | `address_countries` |  
| 27 | `address_states` |  
| 28 | `auth_assignment` |  
| 29 | `auth_assignment-` |  
| 30 | `auth_item` |  
| 31 | `auth_item-` |  
| 32 | `auth_item_child` |  
| 33 | `auth_rule` |  
| 34 | `authorised_master` |  
| 35 | `BankMaster` |  
| 36 | `Buyer` |  
| 37 | `CadDetails` |  
| 38 | `calcalendar` |  
| 39 | `calcategory` |  
| 40 | `calfirstday` |  
| 41 | `calglobals` |  
| 42 | `calholidays` |  
| 43 | `callocale` |  
| 44 | `calperiod` |  
| 45 | `calusers` |  
| 46 | `calweekdays` |  
| 47 | `CancelOrder` |  
| 48 | `Capacity` |  
| 49 | `Capacity5` |  
| 50 | `CapacityAcc` |  
| 51 | `CapacityLing` |  
| 52 | `capallowpcmin` |  
| 53 | `Car` |  
| 54 | `Category` |  
| 55 | `CategoryCodeStyle` |  
| 56 | `CFParts-OLD` |  
| 57 | `CFProd-OLD` |  
| 58 | `CFReq-OLD` |  
| 59 | `chat` |  
| 60 | `City` |  
| 61 | `CollarCuffSize` |  
| 62 | `CollarKnPSize` |  
| 63 | `Company` |  
| 64 | `CompanyOrd` |  
| 65 | `companyS` |  
| 66 | `cost_accessories` |  
| 67 | `cost_accessories_qut_price` |  
| 68 | `cost_fabric` |  
| 69 | `cost_finish_process` |  
| 70 | `cost_finish_process_item` |  
| 71 | `cost_gmt_parts` |  
| 72 | `cost_order` |  
| 73 | `Country` |  
| 74 | `CuffKnPSize` |  
| 75 | `Currency` |  
| 76 | `CurrencyConversion` |  
| 77 | `CutSize` |  
| 78 | `DailyCurrencyRate` |  
| 79 | `DayAll` |  
| 80 | `DChemSales` |  
| 81 | `department--` |  
| 82 | `department-OLD` |  
| 83 | `Dept` |  
| 84 | `designation` |  
| 85 | `Dia` |  
| 86 | `DiaSize` |  
| 87 | `DigitalNote` |  
| 88 | `DrCr` |  
| 89 | `dtproperties` |  
| 90 | `DyeFollowUp` |  
| 91 | `DyeFollowUpInFo` |  
| 92 | `DyeMProfile` |  
| 93 | `DyeProPlan` |  
| 94 | `DyesChemStock` |  
| 95 | `DyeSupplier` |  
| 96 | `employee-` |  
| 97 | `ESMaster` |  
| 98 | `ExportQtyValue` |  
| 99 | `FAAcctDetail` |  
| 100 | `FAAcctMaster` |  
| 101 | `FabAdd` |  
| 102 | `FABalSummary` |  
| 103 | `FabReq` |  
| 104 | `Fabric` |  
| 105 | `FabricProd` |  
| 106 | `FabricProdReprocess` |  
| 107 | `Factory` |  
| 108 | `FactoryMerchandiser` |  
| 109 | `FAIntAccts` |  
| 110 | `FakeHis` |  
| 111 | `FATransHeader` |  
| 112 | `FAVoucherInfo` |  
| 113 | `fd_process_dt` |  
| 114 | `fd_process_item` |  
| 115 | `FDBLC` |  
| 116 | `FinancialYear` |  
| 117 | `FingerTemplate` |  
| 118 | `Floor` |  
| 119 | `FollowUpCompactor` |  
| 120 | `G_Fabric` |  
| 121 | `Gate_Pass` |  
| 122 | `gatepasstype` |  
| 123 | `GFabRcvd` |  
| 124 | `hourly_prod_line` |  
| 125 | `hourly_prod_sewing` |  
| 126 | `HwCD-W` |  
| 127 | `HWItem` |  
| 128 | `HWPurchase_W` |  
| 129 | `HWStock_W` |  
| 130 | `ImportLc` |  
| 131 | `Intercom-W` |  
| 132 | `intercom_parallel` |  
| 133 | `Issue` |  
| 134 | `Issue-2` |  
| 135 | `Issue-3` |  
| 136 | `Issue-4` |  
| 137 | `ITBackupList` |  
| 138 | `Item` |  
| 139 | `ItemCategory` |  
| 140 | `ItemMast` |  
| 141 | `kc_menu` |  
| 142 | `kc_set_building` |  
| 143 | `kc_set_company` |  
| 144 | `kc_set_department` |  
| 145 | `kc_set_designation` |  
| 146 | `kc_set_employee` |  
| 147 | `kc_set_factory` |  
| 148 | `kc_set_uom` |  
| 149 | `kc_user` |  
| 150 | `kc_user_logon` |  
| 151 | `KDData` |  
| 152 | `KDelSt` |  
| 153 | `knit_factory` |  
| 154 | `Knit_Supplier` |  
| 155 | `KnitFollowUp` |  
| 156 | `KnitMProfile` |  
| 157 | `KnitSubContact-OLD` |  
| 158 | `LC` |  
| 159 | `lc_amendment_cost` |  
| 160 | `lc_cost` |  
| 161 | `lc_openning_cost` |  
| 162 | `lc_org_cost` |  
| 163 | `lc_others_cost` |  
| 164 | `lc_supplier` |  
| 165 | `LCAmend` |  
| 166 | `LcName` |  
| 167 | `LG-Purchase` |  
| 168 | `LineMaster` |  
| 169 | `LineSewing` |  
| 170 | `LingQ_MonthCap-OLD` |  
| 171 | `Main` |  
| 172 | `Main1` |  
| 173 | `Main2` |  
| 174 | `MBreakdown` |  
| 175 | `MCPeriodMnt` |  
| 176 | `menu-OLD` |  
| 177 | `Merchan` |  
| 178 | `migration` |  
| 179 | `MonthlyMeeting` |  
| 180 | `MSpareItemMaster` |  
| 181 | `MSpareStock` |  
| 182 | `NeedleIN-OLD` |  
| 183 | `NeedleIssue-OLD` |  
| 184 | `NeedleMaster-OLD` |  
| 185 | `OKProduction` |  
| 186 | `OrderDetails` |  
| 187 | `OrdQty` |  
| 188 | `OrdSizeSeries` |  
| 189 | `Parts` |  
| 190 | `PartyPay` |  
| 191 | `PartyPay2` |  
| 192 | `PathAll` |  
| 193 | `PC_Description_W` |  
| 194 | `PCCheckList_W` |  
| 195 | `PODtl` |  
| 196 | `POHeader` |  
| 197 | `PrgKC_users` |  
| 198 | `PrgKCv104v105_settings` |  
| 199 | `process_problem_details` |  
| 200 | `ProdMonitoring` |  
| 201 | `ProdOperation` |  
| 202 | `Project1_settings` |  
| 203 | `purchase_requisitions` |  
| 204 | `purchase_requisitions_items` |  
| 205 | `Q_Month2` |  
| 206 | `Q_MonthCap` |  
| 207 | `Rcvd` |  
| 208 | `Rcvd-4` |  
| 209 | `Rcvd2` |  
| 210 | `RcvdOLD` |  
| 211 | `Reminder` |  
| 212 | `RouterInfo` |  
| 213 | `routerinfo_details` |  
| 214 | `rta_process_date` |  
| 215 | `Sample_Name` |  
| 216 | `SampleDetails` |  
| 217 | `Season` |  
| 218 | `SelectedCompany` |  
| 219 | `Sheet1` |  
| 220 | `SizeType` |  
| 221 | `Sketch` |  
| 222 | `SoftPass` |  
| 223 | `SP_Pass` |  
| 224 | `Store` |  
| 225 | `Store_lng` |  
| 226 | `store_requisitions` |  
| 227 | `store_requisitions_items` |  
| 228 | `Supplier` |  
| 229 | `Suppliers` |  
| 230 | `Support-History` |  
| 231 | `Support-IT_audit` |  
| 232 | `Support-IT_locking` |  
| 233 | `Support-IT_settings` |  
| 234 | `support-it_uggroups` |  
| 235 | `support-it_ugmembers` |  
| 236 | `support-it_ugrights` |  
| 237 | `support_history_location` |  
| 238 | `sysdiagrams` |  
| 239 | `TCard` |  
| 240 | `techlearnlink` |  
| 241 | `tmp_yarn` |  
| 242 | `tmp_yarn2` |  
| 243 | `TmpActive_IT` |  
| 244 | `TmpData` |  
| 245 | `TmpDCOpStock` |  
| 246 | `TmpLcDetails` |  
| 247 | `TmpLcDetails2` |  
| 248 | `TMPLineSewing` |  
| 249 | `TmpStock` |  
| 250 | `Unit` |  
| 251 | `unit_of_measurement` |  
| 252 | `UsedNetIP` |  
| 253 | `user-OLD` |  
| 254 | `user_logon-OLD` |  
| 255 | `UserPCInfo` |  
| 256 | `users-erp` |  
| 257 | `webreport_admin` |  
| 258 | `webreport_sql` |  
| 259 | `webreport_style` |  
| 260 | `webreports` |  
| 261 | `WetData` |  
| 262 | `y_count` |  
| 263 | `y_type` |  
| 264 | `YarnLcMonitor` |  

## 3. View Inventory

| # | View Name |
|---:|---|---|---|
| 1 | `2019-09-17` |  
| 2 | `a1` |  
| 3 | `a2` |  
| 4 | `a3` |  
| 5 | `abc` |  
| 6 | `AccCost` |  
| 7 | `AccPos` |  
| 8 | `Accpos1` |  
| 9 | `activecostorder` |  
| 10 | `Balance` |  
| 11 | `Balance1` |  
| 12 | `Balance2` |  
| 13 | `BalanceInfo` |  
| 14 | `BodyGSM` |  
| 15 | `CapView1` |  
| 16 | `CapView2` |  
| 17 | `CapView3` |  
| 18 | `CapViewAcc1` |  
| 19 | `CapViewAcc2` |  
| 20 | `CapViewAcc3` |  
| 21 | `CapViewLing1` |  
| 22 | `CapViewLing2` |  
| 23 | `CapViewLing3` |  
| 24 | `CapViewWBuyer1` |  
| 25 | `CapViewWBuyer2` |  
| 26 | `CapViewWBuyer3` |  
| 27 | `CCFProd` |  
| 28 | `CF1` |  
| 29 | `CF2` |  
| 30 | `CFSum` |  
| 31 | `CheckValue` |  
| 32 | `Compare_Main_To_Capcity` |  
| 33 | `CompareConvFactor` |  
| 34 | `CompareDate` |  
| 35 | `CompareQty` |  
| 36 | `CompareRate` |  
| 37 | `Costing Chemicals` |  
| 38 | `Costing_Dyes` |  
| 39 | `Costing_Hyche` |  
| 40 | `CuttingOrd` |  
| 41 | `DC_Issue` |  
| 42 | `DC_Rcvd` |  
| 43 | `DChemSales2` |  
| 44 | `Dept_H&M` |  
| 45 | `DFolowQ` |  
| 46 | `DFStyle` |  
| 47 | `DPlanTotalKg` |  
| 48 | `DQTgt` |  
| 49 | `DReqKnit` |  
| 50 | `DrOpeningBal` |  
| 51 | `DyCmIssue` |  
| 52 | `DyCmRcvd` |  
| 53 | `DyeBooked` |  
| 54 | `DyeChmStock` |  
| 55 | `DyedTotalProd` |  
| 56 | `DyeFabTotalV` |  
| 57 | `DyeFollowupDel` |  
| 58 | `DyeFollowupView` |  
| 59 | `DyeProdMonthly` |  
| 60 | `DyePType` |  
| 61 | `DyM` |  
| 62 | `Eset` |  
| 63 | `FabalUpdate` |  
| 64 | `FabReqT` |  
| 65 | `FabReqView` |  
| 66 | `FabricProdYearly` |  
| 67 | `FabricRate` |  
| 68 | `FALedger` |  
| 69 | `FV` |  
| 70 | `G1Rec` |  
| 71 | `GFIssued` |  
| 72 | `GFRcvd` |  
| 73 | `GRec` |  
| 74 | `grey_finish_fabrics_delivery_information` |  
| 75 | `GreyKgs` |  
| 76 | `GSM` |  
| 77 | `HStockV` |  
| 78 | `HWIN` |  
| 79 | `HWOut` |  
| 80 | `In_Issue` |  
| 81 | `Insert_Costing` |  
| 82 | `kbentryTD` |  
| 83 | `kbentryTDO` |  
| 84 | `kcauto_user_details` |  
| 85 | `KcSoft` |  
| 86 | `KDeSt1` |  
| 87 | `KDView` |  
| 88 | `KnitBooked` |  
| 89 | `KnitedInside` |  
| 90 | `KnitedOutside` |  
| 91 | `KnitprodMonthly2` |  
| 92 | `KnitProMonthly` |  
| 93 | `KnitReqComp` |  
| 94 | `KnitReqComp1` |  
| 95 | `KnitTotalProd` |  
| 96 | `KnM` |  
| 97 | `KNMCV` |  
| 98 | `KNMCV1` |  
| 99 | `KnOrd` |  
| 100 | `KnSmSqty` |  
| 101 | `KV1` |  
| 102 | `KV2` |  
| 103 | `KVF1` |  
| 104 | `KVF1ColorLot` |  
| 105 | `LcUti` |  
| 106 | `LedgerAccInfo` |  
| 107 | `LedgerInfo1` |  
| 108 | `LineProd` |  
| 109 | `LineSewBuyer` |  
| 110 | `LineSewingSum` |  
| 111 | `LineWiseSewingYearlycompyanywise` |  
| 112 | `Lot_no` |  
| 113 | `LotProd` |  
| 114 | `Master` |  
| 115 | `MCBatch` |  
| 116 | `MCostDC` |  
| 117 | `McProd` |  
| 118 | `MVStock` |  
| 119 | `NeedleStock1` |  
| 120 | `NeedleStock2` |  
| 121 | `NewFifo` |  
| 122 | `OPrintEmb` |  
| 123 | `Order5` |  
| 124 | `Order6` |  
| 125 | `Order7` |  
| 126 | `OrderTD` |  
| 127 | `OrderUpdate` |  
| 128 | `OrdRate` |  
| 129 | `OverYarnIssue` |  
| 130 | `PartyOB` |  
| 131 | `PartyPay3` |  
| 132 | `Payable` |  
| 133 | `PayableInfo` |  
| 134 | `Payble2` |  
| 135 | `PCST` |  
| 136 | `PoAccView` |  
| 137 | `PoNo` |  
| 138 | `PosAcc` |  
| 139 | `PosAcc1` |  
| 140 | `PrintEmbQty` |  
| 141 | `PrLoss` |  
| 142 | `ProdSwQty` |  
| 143 | `ProPlanView` |  
| 144 | `Q_Balance` |  
| 145 | `Q_ColorD` |  
| 146 | `Q_DIssue` |  
| 147 | `Q_Dye` |  
| 148 | `Q_FabRcvd` |  
| 149 | `Q_GDay` |  
| 150 | `Q_Issue` |  
| 151 | `Q_Issued` |  
| 152 | `Q_LC_Prob` |  
| 153 | `Q_Order` |  
| 154 | `Q_OrdQty` |  
| 155 | `Q_Print_Emb` |  
| 156 | `Q_ProdHistory` |  
| 157 | `Q_ProdHistory2` |  
| 158 | `Q_ProdM0` |  
| 159 | `Q_ProdM1` |  
| 160 | `Q_ProdM3` |  
| 161 | `Q_ProdM4` |  
| 162 | `Q_ProdSh` |  
| 163 | `Q_Rcvd` |  
| 164 | `Q_Rep1` |  
| 165 | `Q_Rep2` |  
| 166 | `Q_Rep3` |  
| 167 | `Q_RepPrice` |  
| 168 | `Q_Stock` |  
| 169 | `Q_Stock2` |  
| 170 | `Q_YarnS` |  
| 171 | `Q_YarnS_Lng` |  
| 172 | `Q_YarnSR` |  
| 173 | `QFabDel` |  
| 174 | `QTotQty` |  
| 175 | `Query1` |  
| 176 | `Query_M` |  
| 177 | `Query_Y` |  
| 178 | `RcpLab` |  
| 179 | `Rep_Query` |  
| 180 | `Rep_Query1` |  
| 181 | `Rep_Query1_Lng` |  
| 182 | `Rep_Query1R` |  
| 183 | `Rep_Query2` |  
| 184 | `Rep_Query2_Lng` |  
| 185 | `RtOrdSh` |  
| 186 | `SampleKnit` |  
| 187 | `SD1` |  
| 188 | `SD2` |  
| 189 | `ShifInfoDelay` |  
| 190 | `ship_for_test` |  
| 191 | `Ship_Info` |  
| 192 | `Ship_Information` |  
| 193 | `Ship_Information1` |  
| 194 | `ShipInfo2` |  
| 195 | `ShipInfo3` |  
| 196 | `ShipInfoDelay` |  
| 197 | `ShippedQty` |  
| 198 | `ShiPView` |  
| 199 | `SketchCheck` |  
| 200 | `sketchView` |  
| 201 | `SqtyKnit` |  
| 202 | `SS` |  
| 203 | `Stock` |  
| 204 | `stock_group` |  
| 205 | `SubContractOrder` |  
| 206 | `SumCutSProd` |  
| 207 | `SumKnit4` |  
| 208 | `SummaryKnit` |  
| 209 | `SummaryKnit1` |  
| 210 | `SummaryKnit2` |  
| 211 | `SummaryKnit3` |  
| 212 | `TableRowCount` |  
| 213 | `TB1` |  
| 214 | `TB2` |  
| 215 | `TmpLC1` |  
| 216 | `TmpLc2` |  
| 217 | `TmpSizeSeries` |  
| 218 | `TodayProd` |  
| 219 | `Total_Issue_Qty` |  
| 220 | `Total_Rcvd_Qty` |  
| 221 | `TotalCuttingOrder` |  
| 222 | `TotKQty` |  
| 223 | `TotView` |  
| 224 | `TrialBalance` |  
| 225 | `TTView` |  
| 226 | `V_GRcvd` |  
| 227 | `V_Shdt` |  
| 228 | `V_Shdt1` |  
| 229 | `VGRcvd1` |  
| 230 | `VIEW3` |  
| 231 | `View_107` |  
| 232 | `VOrdSize` |  
| 233 | `VPay` |  
| 234 | `YarnIssue` |  
| 235 | `YCKDData` |  
| 236 | `YDOrder5` |  
| 237 | `YDRcvd` |  
| 238 | `YDVF1` |  
| 239 | `YLot` |  
| 240 | `YLotCqty` |  
| 241 | `YLotCqtyLNG` |  
| 242 | `YrnIss` |  
| 243 | `z-CapView1New` |  
| 244 | `z_ConfirmOrderqtykgsTD` |  
| 245 | `z_ConfirmOrderqtykgsTDO` |  
| 246 | `z_kcmarchantstatusTD` |  
| 247 | `z_OrderKgssumNTD` |  
| 248 | `z_OrderKgssumTD` |  
| 249 | `z_OrderqtySumTD` |  
| 250 | `zdashboardcap` |  

## 4. Documentation Notes

- Object names and types are based on the supplied workbook.
- All objects are listed under the `dbo` schema in the source extract.
- Confirm primary keys and foreign keys from SQL Server constraints.
- Confirm view dependencies from the SQL definitions; views may reference tables or other views.
- Assign business modules and business-purpose descriptions only after reviewing schema definitions and application workflows.

## 5. Recommended Next Steps

1. Export table columns, data types, nullability, identity properties, and defaults.
2. Extract primary keys, unique constraints, and foreign keys.
3. Extract view definitions and referenced objects.
4. Group tables and views into verified business modules.
5. Replace the unverified placeholders with reviewed documentation.

---

*Inventory totals: 264 base tables and 250 views.*


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
| Base tables | 264 |
| Views | 250 |
| Stored Procedures | 10 |
| Functions | 30 |
| Triggers | 10 |
| Indexes | 150 |
| Constraints | 300 |

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
