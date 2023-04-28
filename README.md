# UI-Specification-Doc

> User Management Screen

# Display Descriptions
# Main Layout
| ID | Element Group | H-Align | V-Align | H-Size | V-Size |
| --- | --- | --- | --- | --- | --- |
| g1 | Action Bar | Stretch | Top | %100 | 64px
| g2 | Table View | Center | Center | %100 | 
| g3 | Form View | Show file differences that haven't been staged |

States
Default state of page is s1
| State ID | Element ID | Visiblity | H-Align | V-Align | H-Size | V-Size |
| --- | --- | --- | --- | --- | --- | --- |
| s1 | g2 | Visible | Center | Center | %100 | %100 |
| s1 | g3 | Hidden | - | - | - | - |
| s2 | g2 | Visible | Left (parent) | Center | %50 | %100 (After g1)
| s2 | g3 | Visible | Right (parent) | Center | %50 | %100 (After g1)

1.1 Action Bar Visual Structure
| ID | Type | Label | H-Align | V-Align |
| --- | --- | --- | --- | --- |
| 1a | Button | +New User | Left | Center (Parent) |
| 1b | Checkbox | Hide Disabled User | Left (After 1a) | Center (Parent)
| 1c | Button | Save User | Right | Center (Parent) |

1.2 Action Bar Functional Behaviours
| ID | Action On Clicked |
| --- | --- |
| 1a | <ul><li>Change state s1 to s2</li><li>v2 and v3 shares %50-%50 width of page when v3 visible</li></ul> |

The background color is `#ffffff`
