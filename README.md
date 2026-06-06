# Purchase-Order-Detail-
Purchase Order Detail  : Develop an SAP ABAP report to display Purchase Order details along with Vendor, Material, and  Goods Receipt (GR) information.

Based on your uploaded **Purchase Order Details Report Requirement**, here is a professional GitHub README for your SAP ABAP project. The report displays Purchase Order, Vendor, Material, and Goods Receipt details using an ALV Grid. 

# 📦 SAP ABAP - Purchase Order Details Report

## 📖 Overview

This SAP ABAP report retrieves and displays Purchase Order details along with Vendor Information, Material Information, and Goods Receipt (GR) details in an ALV Grid Output.

The report allows users to enter a Purchase Order Number and view all related procurement and GR information in a single screen.


🎯 Objective

Develop an SAP ABAP ALV Report that:

* Displays Purchase Order Header and Item details
* Fetches Vendor information
* Retrieves Material descriptions
* Displays Goods Receipt details
* Calculates Remaining Quantity
* Presents data in an ALV Grid


 🖥️ Report Type

* Executable Program (SE38)
* ALV Grid Report
* Single Selection Parameter


📋 Selection Screen

| Parameter | Description           | Table-Field |
| --------- | --------------------- | ----------- |
| PO Number | Purchase Order Number | EKKO-EBELN  |



📊 Output Fields

| Field                 | Description              |
| --------------------- | ------------------------ |
| Purchase Order Number | PO Number                |
| Line Item             | PO Item                  |
| Vendor Number         | Vendor Code              |
| Vendor Name           | Vendor Name              |
| Material Number       | Material Code            |
| Material Description  | Material Description     |
| Ordered Quantity      | Ordered Quantity         |
| Price                 | Net Price                |
| Goods Receipt Number  | Material Document Number |
| Goods Receipt Year    | Material Document Year   |
| GR Quantity           | Goods Receipt Quantity   |
| Remaining Quantity    | Ordered Qty - GR Qty     |



🗄️ SAP Tables Used

| Table | Purpose                             |
| ----- | ----------------------------------- |
| EKKO  | Purchase Order Header               |
| EKPO  | Purchase Order Item                 |
| LFA1  | Vendor Master                       |
| MAKT  | Material Description                |
| MSEG  | Goods Receipt Details               |
| MKPF  | Material Document Header (Optional) |



⚙️ Business Logic

Step 1 : Read Purchase Order Header data from EKKO.
Step 2 : Fetch Purchase Order Item details from EKPO.
Step 3 : Get Vendor details from LFA1.
Step 4 : Fetch Material Description from MAKT.
Step 5 : Retrieve Goods Receipt details from MSEG:
Material Document Number (MBLNR)
Material Document Year (MJAHR)
GR Quantity (MENGE)

Step 6 : Calculate Remaining Quantity : Remaining Quantity = Ordered Quantity - GR Quantity
Step 7 : Display data using ALV Grid.


🧮 Quantity Calculation : lv_remaining_qty = ekpo-menge - mseg-menge.

📈 ALV Features

✔ Sort Data

✔ Filter Records

✔ Export to Excel

✔ Layout Variants

✔ Totals & Subtotals

✔ User-Friendly Display


🚀 Technologies Used

* SAP ABAP
* ALV Grid Display
* Internal Tables
* Open SQL
* Classical Report Programming



📂 Project Structure

ZPURCHASE_ORDER_DETAILS
│
├── Selection Screen
├── Data Fetch Logic
│   ├── EKKO
│   ├── EKPO
│   ├── LFA1
│   ├── MAKT
│   └── MSEG
│
├── Remaining Quantity Calculation
│
└── ALV Output

🎓 Learning Concepts Covered

* Data Dictionary Tables
* Internal Tables
* Work Areas
* Open SQL Joins
* FOR ALL ENTRIES
* ALV Grid Reports
* Selection Screen Programming
* Data Processing Logic

