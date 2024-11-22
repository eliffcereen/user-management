# User Management Screen - UI Specification

## Purpose
The **User Management Screen** allows administrators to manage users by adding, updating, and viewing user details. It provides functionality to filter, enable/disable users, and assign roles.

---

## General Requirements
1. **Responsive Design**: The screen should adapt to various screen sizes.
2. **Validation**:
   - All fields in the "New User" form must be validated.
   - Email must be in a valid format.
   - "Username" must be unique.
3. **Accessibility**: Buttons, inputs, and dropdowns must comply with accessibility standards (e.g., keyboard navigation, ARIA labels).

---

## UI Components

### **1. Toolbar**
- **+ New User Button**:
  - Opens the "New User" form.
- **Hide Disabled User Checkbox**:
  - Filters the list to exclude disabled users when checked.

### **2. User List**
- **Columns**:
  - **ID**: Unique identifier (numeric).
  - **User Name**: Displays the username.
  - **Email**: Displays the user's email address.
  - **Enabled**: Boolean status (true/false).
- **Sorting**:
  - Each column is sortable (ascending/descending).
- **Filtering**:
  - Filters are available for "User Name", "Email", and "Enabled".

### **3. New User Form**
- **Fields**:
  1. **Username**:
     - Text input.
     - Required.
  2. **Display Name**:
     - Text input.
  3. **Phone**:
     - Text input.
     - Optional.
  4. **Email**:
     - Text input.
     - Required.
     - Must follow email format validation.
  5. **User Roles**:
     - Dropdown with multiple options (Guest, Admin, SuperAdmin).
     - Required.
  6. **Enabled**:
     - Checkbox.
     - Default: Unchecked.
- **Save User Button**:
  - Saves user details.
  - Disabled until all required fields are filled and valid.

---

## Behavior and Interactions

1. **On Page Load**:
   - Display the user list.
   - Default: "Hide Disabled User" unchecked.

2. **+ New User Button**:
   - Clears the form.
   - Displays the "New User" panel.

3. **Save User Button**:
   - Validates the form.
   - Displays a confirmation message upon successful save.

4. **Sorting and Filtering**:
   - Updates the user list dynamically.

5. **Hide Disabled User Checkbox**:
   - Filters the list when toggled.

---

## Error Handling
1. If validation fails:
   - Highlight the incorrect field with a red border.
   - Display an error message (e.g., "Invalid email format").
2. If saving fails (e.g., duplicate username):
   - Display an error toast: "Save failed: Username already exists."

---

## Future Enhancements
1. Bulk user import/export functionality.
2. Role-based access control for UI elements.

---