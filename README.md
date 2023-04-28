# User Management Screen
## Main Layout
| ID | Group Name | H-Align | V-Align | H-Size | V-Size | Visiblity |
| --- | --- | --- | --- | --- | --- | --- |
| g1 | Action Bar | Stretch | Top | %100 | 64px | Visible |
| g2 | Table View | <ul><li>s1) Center</li><li>s2) Left</li></ul> | Top (After g1) | <ul><li>s1) %100</li><li>s2) %50</li></ul> | %100 | <ul><li>s1) Visible</li><li>s2) Visible</li></ul> |
| g3 | Form View | <ul><li>s1) Center</li><li>s2) Right</li></ul> | Top (After g1) | <ul><li>s1) %100</li><li>s2) %50</li></ul> | %100 | <ul><li>s1) Hidden</li><li>s2) Visible</li></ul>

### States
- Default page state is s1
- s1 Shows only g2 table view and hides g3 form view
- s2 Shows both g2 and g3 side by side



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
All column headers contains 'order by' and 'filter' right aligned buttons
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
