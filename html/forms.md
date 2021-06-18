# Forms in HTML
## Regular expressions
Used to specify string patterns. Example:   
`[^]*\d{3}[^]*\d{3}-\d{4}`: phone number pattern
## Client-side Validation
Ex: make parts of a form required or require match with specific regex.
- Useful libraries: Parsley, Vanilla
### Some practices
* Add "required" attribute
* Set min and max
* Maxlength/minlength for text
* Use pattern="some-regular-expression"

## Back-end Validation
"a malicious user can simply turn off JavaScript on their browser, for example"

## HTTP
"Protocol of requests and responses"  
HTTP can also be considered a "command language" that both sides of a connection must use.  
Initial request -> client
Initial response -> server

Client sends **HTTP GET** through TCP connection.

Common HTTP Methods:
- GET
- PUT
- DELETE
- POST

| Element | Description | Attributes |
| ------- | ----------- | ---------- |
| `<form>` | general form container | action (where the information is sent), method (HTTP verb) |
| `<input>` | input field | type (ex. text, password, number, range, checkbox, radio, submit, placeholder...), name (to pair with input text), value (what is typed or prefilled in the field), step (increase/decrease arrows), list (to associate to datalist) |
| `<label>` | Display text | for (assigned with the id of input element) |
| `<select>` | Dropdown list | id, name (selection results in "select_id=option_value" |
| `<option>` | Option for dropdown list (either select or datalist) | value |
| `<datalist>` | Dropdown list within text input field | id |
| `<textarea>`| bigger text box | id, name, rows, cols |

## CSS
Can use `:valid` and `:invalid` pseudoclasses to enhance user experience during validation.
