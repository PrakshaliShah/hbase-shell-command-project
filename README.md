# 🧾 HBase Shell Command Project – Customer Data Modeling

This project uses **Apache HBase shell commands** to create, populate, and query a semi-structured customer database. We explore column-family-based modeling for names, addresses, demographics, and digital payment behavior.

---

## 🧱 Table Structure: `customer`

| Column Families       | Example Fields                              |
|-----------------------|---------------------------------------------|
| `Cust_Name`           | FirstName, LastName                         |
| `Address`             | Street, City, State, Zip                    |
| `Demographics`        | DOB, Gender                                 |
| `Payments`            | CreditCard, InternetBanking, MobileBanking  |

---

## 📁 Files Included

- `tutorial_a_shell_commands.txt` – Create table, list, describe, disable, drop  
- `tutorial_a_put_commands.txt` – Inserted sample rows using `put`  
- `tutorial_a_scan_commands.txt` – Basic `scan`, `scan with filter`, and version examples  
- `tutorial_b_shell_commands.txt` – Follow-up actions: new rows, deletes, metadata  
- `tutorial_b_customer_puts.txt` – Populated customer table with rich sample data

---

## ✍️ Sample Commands

```bash
create 'customer', 'Cust_Name', {NAME => 'Address', VERSIONS => 3}, 'Demographics', {NAME => 'Payments', VERSIONS => 3}
put 'customer', '171', 'Cust_Name:FirstName', 'Madelyn'
put 'customer', '171', 'Address:City', 'New York'
scan 'customer'
