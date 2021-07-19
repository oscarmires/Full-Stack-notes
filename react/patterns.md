# Patterns 

## Stateless components inherit from statefull components
A parent component passes information down to a child component, which has no state.

### Child updates parent
1. Create handler function in parent
2. Bind handler function to parent
3. Pass function to child as prop
4. Child uses handler function to update parent

### Child updates sibling
1. Child allows for change using handler function
2. Parent passes new (changed) data to sibling
3. Sibiling reflects the change

---
