# User Management Screen
## Main Layout
| ID | Group Name | H-Align | V-Align | H-Size | V-Size |
| --- | --- | --- | --- | --- | --- |
| g1 | Action Bar | Stretch | Top | %100 | 64px
| g2 | Table View | Center | Top (After g1) | %100 | 
| g3 | Form View | Center | Top (After g1) | %100 |

### States
- s1 Shows only g2 table view and hides g3 form view
- s2 Shows both g2 and g3
- Default state of page is s1

| State ID | Element ID | Visiblity | H-Align | V-Align | H-Size | V-Size |
| --- | --- | --- | --- | --- | --- | --- |
| s1 | g2 | Visible | Center | Center | %100 | %100 |
| s1 | g3 | Hidden | - | - | - | - |
| s2 | g2 | Visible | Left (parent) | Center | %50 | %100 (After g1)
| s2 | g3 | Visible | Right (parent) | Center | %50 | %100 (After g1)

### 1.1 g1 Action Bar Visual Structure
| ID | Type | Label | H-Align | V-Align |
| --- | --- | --- | --- | --- |
| 1a | Button | +New User | Left | Center (Parent) |
| 1b | Checkbox | Hide Disabled User | Left (After 1a) | Center (Parent)
| 1c | Button | Save User | Right | Center (Parent) |

### 1.2 g1 Action Bar Functional Behaviours
| ID | Action On Clicked |
| --- | --- |
| 1a | Change state s1 to s2 |
| 1b | Filter g2 table view data to show only enabled users |
| 1c | Save user with filled g3 form datas |

### 2.1 g2 Table View Visual Structure
Fetchs data and shows columns below:
- ID
- User Name
- Email
- Enabled

### 2.2 g2 Table View Functional Behaviours
All column headers contains 'order by' and 'filter' buttons.
- Order By Button: Orders rows by related column's values
- Filter Button: Filters rows by searched value on column

### 3.1 g1 Form View Visual Structure
- Elements will be grouped by label - input pair
- Groups will be showed line by line
- Labels and inputs will share width %25 - %75 as constant size
- Labels left, inputs right aligned

| Label | Input Type | Value Constraint |
| --- | --- | --- |
| User Name | Text Box | - |
| Display Name | Text Box | - |
| Phone | Text Box | + (0-9) Digits |
| Email | Text Box | az..AZ @ . |
| User Roles | Combo Box | <ul><li>Guest</li><li>Admin</li><li>SuperAdmin</li></ul> |
| Enabled | Check Box | - |

- If all filled values are valid, then 1c button will be enabled, otherwise disabled
