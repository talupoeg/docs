# Interactivity with Javascript

Introduction to use javascript with web pages.

[![Eloquent Javascript](https://eloquentjavascript.net/img/cover.jpg "Eloquent Javascript")](https://eloquentjavascript.net/)

> Notes from the course

## Week IV

User input.

#### Forms

Forms add a new layer to the Request-Response Cycle.

- forms are used to pass data
- different input elements can be used
- forms usually exchange data with a server

This course covers only basic front-end web development. That is a client-side html, css and some js dynamic.

> Structure

A minimal semantic form structure is to have a `form`, `label` and `input` tags.

```html
<form id="myForm">
    <fieldset>
        <legend>Irrelevant information</legend>
        <label for="clientName">Name</label>
        <input type="text" id="clientName" name="whatever"><br />
        <label>E-mail: <input type="email" name="email" /></label><br />
        <label for="birth">Birth</label>
        <input type="date" id="birth" value="birth"><br />
        <button>Validate</button>
    </fieldset>
</form>
```

By linking `label` and `input` together by "clientName" with a `for` and `id` attribute it's easier to click on a label and it activates the input field.

> Input types

- textfield
- email
- password
- radiobutton
    - have the attribute `checked`
- checkbox
    - have the attribute `checked`
- submit
- more types include:
    - number
    - range
    - color
    - date
    - url

> Attributes

- name
    - almost all input types use this attribute
- id
    - used for labels
    - used by js scrips
- value
    - if button - text inside the button
    - if textfield - provides a default value
- placeholder
    - provides a suggestion

#### Simple validation

Before validation it's important to stop and plan on things needed to be validated.

> What to validate?

- the type of input
    - number instead of a string..
- the format of the input
    - is it a valid email address or URL?
    - does the phone number have spaces?
- the value of the input
    - is it required?
    - email values match?

> How to validate?

- one way is to use `HTML5 input types`
    - email, number, url..
- another is to use `HTML5 attributes`
    - required, placeholder, min, max
- better way or a mixture is to use `JS` function
    - custom code to validate user input
    - normally it's also done in server side

> HTML5 Input types

The input types require that the browser validates the format of the input. When supported it will halt the submit process if not valid input.

- the first non-valid input is put into focus
- if not supported the input type is just text

> Input validation

- `required` attribute is used for inputs that need to be filled
- `novalidate` are for developing purposes, so no validation
- pattern
    - works with input type text
    - requires the input have a specific form
    - used with regular expressions:
        - `[0-9]{5}` - numbers 0-9 and 5 total digits
        - `[0-9]{13-16}` - 0-9 and 13-16 digits
        - `[a-zA-Z]+` at least one alphabet char
    - best if used with placeholders
    - html5pattern.com

> Validate by limiting number digits

- `min`, `max`, `step` (increment of 1, 2, 5 etc.)
- `range` input type attribute also has a max, min






