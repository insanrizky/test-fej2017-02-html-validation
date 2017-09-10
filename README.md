# test-fej2017-02-html-validation
Test FEJ2017 - 02 HTML Validation

This repository has been built to answer the test from https://github.com/sbhalim/test-fej2017/blob/master/02-html-validation.md

---

Modify the following HTML to ensure the the form can be only submitted when 
the following predefined set of conditions are fulfilled:

* **Title** is optional;
* **Name** must be filled, contains only A-Z, a-z and space. Minimum length of is 10 characters;
* **Sex** is required;
* **Email** is required, and must be valid email addreess format;
* **Phone** is required. Phone can only contains optional `+` prefix and numbers. Maximum length is 20;
* **Address** is optional, and the max length is 200;
* **ZIP** code is required and can only contains `A-Z`, `0-9` and `-` (dash). Maximum length is 10.

Use of JavaScript is discouraged. HTML way is preferred.

```html
<!DOCTYPE html>
<html>
<head> 
    <style type="text/css">
        body {font-family: sans-serif; font-size: .90rem}
        label {margin: .25rem 1rem .25rem 0; width: 7rem; display: inline-block;}
        input[type=text] {margin: .25rem 0 .25rem 0; width: 15rem;}
        fieldset {border: none;}
        #validateButton {margin-left: 8.2rem;}
    </style>
</head>
<body>
    <form action="#" method="post">
        <fieldset> 
            <label for="titleInput">Title:</label>
            <select id="titleInput">
                <option>- Please Select - </option>
                <option>Mr.</option>
                <option>Ms.</option>
                <option>Mrs.</option>
            </select>
            <br />
            <label for="fullnameInput">Name:</label> <input id="fullnameInput" type="text" /><br />
            <label>Sex:</label>
            <label><input id="sexMaleRadio" name="sex" type="radio" value="f" />&nbsp;Female</label>
            &nbsp;
            <label><input id="sexMaleRadio" name="sex" type="radio" value="m" />&nbsp;Male</label>
            <br />
            <label for="emailInput">Email:</label> <input id="emailInput" type="text" required /><br />
            <label for="phoneInput">Phone:</label> <input id="phoneInput" type="text" /><br />
            <label for="addressInput">Address:</label> <input id="addressInput" type="text" /><br />
            <label for="zipcodeInput">ZIP Code:</label> <input id="zipcodeInput" type="text" /><br />
        </fieldset>
        <fieldset>
            <input type="submit" id="validateButton" value="Validate!" />
        </fieldset>
    </form>
</body>
</html>
```