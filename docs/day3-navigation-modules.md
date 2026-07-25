# Day 3 - Application Navigation

## Objective

Configure application navigation so users can access the Smart Visitor Management System through the ServiceNow navigation menu.

---

## Tasks Completed

- Created an Application Menu for the Smart Visitor Management System.
- Created the Visitors module.
- Created the Register Visitor module.
- Linked the Visitors module to the Visitor table.
- Configured the module path.
- Verified the module configuration.

---

## Concepts Learned

### Application Menu

An Application Menu is the main entry point for an application in the ServiceNow navigation pane. It groups related modules together.

Example:

Smart Visitor Management System
- Visitors
- Register Visitor
- Reports
- Dashboard

---

### Module

A Module is a navigation item inside an Application Menu.

Modules allow users to:

- Open a table
- Open a filtered list
- Open a URL
- Launch a script

---

### Module Configuration

Module Name: Visitors

Table:
Visitor

Path:
visitor

Application:
Smart Visitor Management System

---

## Learning Outcome

After completing Day 3, I understand:

- What an Application Menu is.
- What a Module is.
- How Modules connect users to tables.
- How navigation is organized in ServiceNow.

---

## Challenges Faced

The newer ServiceNow Studio interface behaved differently from older tutorials.

Although the Application Menu and Modules were created successfully, the navigation menu did not immediately display them. The issue appeared to be related to the Studio/Build Agent experience rather than the module configuration itself.

---

## Best Practices Learned

- Use meaningful module names.
- Keep related modules under one Application Menu.
- Use consistent naming conventions.
- Verify module configuration before troubleshooting navigation issues.
- Avoid creating duplicate modules while debugging.

---

## Status

✅ Completed
