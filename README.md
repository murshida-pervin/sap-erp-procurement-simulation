# SAP-inspired Procurement Simulation (Python + SQL)

📂 PROJECT STRUCTURE

sap-procurement-simulation/
│
├── README.md                     # Detailed documentation (template below)
├── requirements.txt              # Python packages
├── oop_showcase.py               # Standalone OOP demonstration (recruiters will read first)
│
├── procurement/
│   ├── __init__.py
│   ├── models.py                 # All OOP classes (Vendor, LineItem, Bundle, PurchaseOrder)
│   ├── database.py               # DB connection and CRUD (SQL + Python integration)
│   └── simulation.py             # Main script that runs the demo
│
├── sql/
│   ├── schema.sql                # CREATE TABLE statements
│   └── sample_queries.sql        # SELECT queries for reporting
│
├── tests/
│   ├── test_models.py            # Unit tests for OOP classes
│   └── test_database.py          # Test DB operations
│
└── docs/
    └── architecture.md           # Explanation of OOP + SQL design

## About this project

I built this project to apply for the **SAP ABAP Internship at Accenture Warsaw**.  
It demonstrates the primary requirements:

- **Strong object-oriented programming** (Python classes, encapsulation, inheritance, polymorphism, abstraction, composition)
- **Very good SQL knowledge** (schema design, CRUD, joins, aggregations)

### Why procurement?

I worked as a **Production Specialist at Swappie Estonia** (phone refurbishment). I saw how purchase orders, vendor ratings, and goods receipts drive operations. This simulation recreates that workflow using code – similar to how SAP’s MM module works.

## OOP Concepts shown

| Concept | Implementation |
|---------|----------------|
| Encapsulation | Vendor.__rating with property getter/setter, validation |
| Inheritance | LineItem and Bundle inherit from abstract Purchasable |
| Polymorphism | print_total() works for both LineItem and Bundle |
| Abstraction | Purchasable ABC forces get_total() method |
| Composition | PurchaseOrder contains a list of Purchasable objects |

## SQL Capabilities

- Tables: vendors, purchase_orders, po_line_items, goods_receipts
- Foreign key constraints, CHECK constraints
- Complex queries: vendor performance (LEFT JOIN + aggregation)
- Parameterized queries (safe from injection)

## How to run

bash
git clone https://github.com/yourusername/sap-erp-procurement-simulation.git
cd sap-procurement-simulation
pip install -r requirements.txt
python -m procurement.simulation