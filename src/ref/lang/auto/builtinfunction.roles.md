# Roles

| Name | Description |
| :--- | :--- |
| [CheckRole](builtinfunction.roles.md#CheckRole)\(​RoleId, UserId\) | Returns true when the given user has the specific role. |
| [GetUserId](builtinfunction.roles.md#GetUserId)\(\) | Returns the identifier of the user that is currently authenticated with the server or 'NullIdentifier\(\)' if the user is not authenticated. |

## CheckRole { \#CheckRole }

Returns true when the given user has the specific role.

Available in:

* Server-side logic: Yes
* Client-side logic: No
* Database: Can be used with attributes in aggregates.
* Local Storage: Can be used with attributes in aggregates.

### Parameters

RoleId : Type: RoleId. Mandatory.  
The identifier of the role to be validated.

UserId : Type: UserId. Mandatory.  
The identifier of the user for which to validate if role is granted.

### Output

Type: Boolean

## GetUserId { \#GetUserId }

Returns the identifier of the user that is currently authenticated with the server or 'NullIdentifier\(\)' if the user is not authenticated.

Available in:

* Server-side logic: Yes
* Client-side logic: Yes
* Database: Function is evaluated before the aggregate is executed.
* Local Storage: Function is evaluated before the aggregate is executed.

### Output

Type: UserId

