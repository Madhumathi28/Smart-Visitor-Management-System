# 📅 Day 5 – UI Policies

## Objective

The objective of Day 5 was to learn and implement **UI Policies** in ServiceNow to dynamically control the behavior of form fields based on user input without writing JavaScript.

---

# What is a UI Policy?

A **UI Policy** is a client-side configuration in ServiceNow that dynamically changes the behavior of fields on a form based on specified conditions.

Using UI Policies, developers can:
- Show or hide fields
- Make fields mandatory
- Make fields read-only

UI Policies improve the user experience by displaying only the relevant information on a form.

---

# Why Use UI Policies?

UI Policies help create dynamic and user-friendly forms by:

- Reducing unnecessary fields.
- Improving form usability.
- Enforcing business requirements.
- Eliminating the need for simple client-side scripting.

---

# UI Policy Components

## Condition

Defines **when** the UI Policy should execute.

Example:

```
Status = Rejected
```

---

## UI Policy Action

Defines **what** should happen when the condition is met.

Possible actions include:

- Visible
- Mandatory
- Read Only

---

## On Load

When enabled, the UI Policy is evaluated as soon as the form is loaded.

---

## Reverse if False

Automatically reverses the field action when the condition is no longer true.

Example:

- Status = Rejected → Remarks field is visible.
- Status changes to Pending → Remarks field is automatically hidden.

---

# UI Policies Implemented

## 1. Show Remarks when Status is Rejected

### Condition

```
Status = Rejected
```

### Action

```
Remarks → Visible = True
```

### Purpose

Displays the Remarks field only when the visitor's status is **Rejected**.

---

## 2. Hide Remarks when Status is Pending

### Condition

```
Status = Pending
```

### Action

```
Remarks → Visible = False
```

### Purpose

Keeps the form clean by hiding the Remarks field while the visitor request is still pending.

---

## 3. Make Check-out Time Editable when Status is Checked Out

### Condition

```
Status = Checked Out
```

### Action

```
Check-out Time → Read Only = False
```

### Purpose

Allows users to edit the Check-out Time only after the visitor has been checked out.

---

# Testing Performed

| Test Case | Expected Result | Status |
|------------|-----------------|--------|
| Status = Rejected | Remarks field becomes visible | ✅ Passed |
| Status = Pending | Remarks field is hidden | ✅ Passed |
| Status = Checked Out | Check-out Time becomes editable | ✅ Passed |

---

# Key Concepts Learned

- UI Policy
- UI Policy Action
- Conditions
- Visible
- Mandatory
- Read Only
- On Load
- Reverse if False

---

# Best Practices

- Use meaningful UI Policy names.
- Keep conditions simple and easy to understand.
- Use UI Policies instead of Client Scripts for simple field behavior.
- Test each UI Policy after implementation.
- Enable **Reverse if False** whenever the field should return to its default state.

---

# Real-World Examples

- Show Passport Number only for international visitors.
- Display Rejection Reason only when a request is rejected.
- Make Approval Comments mandatory after approval.
- Allow Check-out Time editing only when the visitor has checked out.

---

# Interview Questions

1. What is a UI Policy?
2. Why are UI Policies used in ServiceNow?
3. What is a UI Policy Action?
4. What is the purpose of the **On Load** option?
5. What does **Reverse if False** do?
6. What is the difference between a UI Policy and a Client Script?
7. What actions can a UI Policy perform?
8. Can a single UI Policy control multiple fields?
9. Explain one UI Policy you implemented in your project.
10. When would you use a UI Policy instead of a Client Script?

---

# Screenshots

Include the following screenshots:

1. UI Policies list showing all three UI Policies.
2. Show Remarks when Status is Rejected.
3. Hide Remarks when Status is Pending.
4. Make Check-out Time Editable when Status is Checked Out.
5. Preview showing the Remarks field appearing when Status is Rejected.

---

# Summary

On Day 5, I learned how to implement UI Policies in ServiceNow to dynamically control form behavior based on business conditions. I created three UI Policies in the Smart Visitor Management System application to manage field visibility and editability according to the visitor's status. These configurations improved the user experience without requiring client-side scripting.
