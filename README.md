
# Week 5 – Todo List Project Summary

## Overview
In Week 5, I continued developing the Todo List project with React, Vite, DynamoDB, and Material UI.  
The main focus was extending the project beyond creating and scanning todos — I implemented update and delete features, learned to clean up the UI with reusable components, and worked with new libraries.  

## Key Learnings

### 1. DynamoDB Integration
- Learned how to use `UpdateCommand` and `DeleteCommand` from `@aws-sdk/lib-dynamodb`.  
- Built helper functions in `dynamo.js`:  
  - `updateTodo(id, updates)` → modifies fields (e.g., toggle completed).  
  - `deleteTodo(id)` → removes a todo item completely.  
- Practiced writing `UpdateExpression`, `ExpressionAttributeNames`, and `ExpressionAttributeValues`.  

### 2. React State Updates
- Connected DynamoDB actions to local React state so the UI updates instantly.  
- Used `setTodos()` with mapping and filtering to reflect changes without reloading.  
- Learned about optimistic UI updates (update UI immediately after action).  

### 3. UI with Material UI and React Icons
- Installed and imported components correctly:  
  ```js
  import { Button, TextField, Checkbox, List } from "@mui/material";
  import { IoTrashOutline } from "react-icons/io5";
  import { HiOutlinePencilSquare } from "react-icons/hi2";