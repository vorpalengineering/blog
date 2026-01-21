---
title: "Access Control Patterns in Solidity"
date: "2025-11-05"
description: "Implementing robust permission systems in your smart contracts."
---

Proper access control is fundamental to smart contract security. Here are the patterns we recommend.

## Common Patterns

### Ownable
Simple single-owner pattern. Good for small projects but limited flexibility.

### Role-Based Access Control (RBAC)
Assign roles to addresses with specific permissions. More flexible than Ownable.

```solidity
mapping(bytes32 => mapping(address => bool)) private _roles;

function hasRole(bytes32 role, address account) public view returns (bool) {
    return _roles[role][account];
}
```

### Multi-Signature
Require multiple approvals for sensitive operations. Essential for treasury management.

## Best Practices

- Use OpenZeppelin's AccessControl for battle-tested implementations
- Implement timelock for admin functions
- Log all permission changes with events
- Consider role hierarchies carefully
