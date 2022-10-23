![image](https://user-images.githubusercontent.com/115179685/197389784-85d16a09-5205-4a11-9093-92f8fd2e1b66.png)
![image](https://user-images.githubusercontent.com/115179685/197389815-441caa77-5dfc-447b-bcc2-164d42be6c24.png)


In this course, you'll learn HTML forms by building a signup page. You'll learn how to control what types of data people can type into your form, and some new CSS tools for styling your page.
    Forms are used to collect information from people who visit webpages.
**************************************************************
    - The vh unit stands for viewport height, and is relative to 1% of the height of the viewport
        1vh=1% (of total screen viewport).
    
    - It is time to spruce the project up with some CSS. Begin by giving the body a width of 100%, and a height of 100vh.

        margin: 0; allowed us to get rid of horizontal scroll-bar

    - rem unit, stands for root em, wich is relative to the font size of the html element.

HTML:

<fieldset></fieldset> Set a distinct section in the form tag.
__________________________________________________________
|_________________________________________________________|

<label></label> inline element by default, so that means they are all displayed side by side on the same line.

<input /> for best practices the label tag have to be linked within the input tag... using the "id" attribute. The id name will be the name the labels "for" attribute has.

    ex:
          <label for="first-name">Enter Your First Name: <input id="first-name" /></label>

    - The email type only allows emails with a @ and a . in the domain. The password type obscures the input, and warns if the site does not use HTTPS.


    - To make the form more interactive, add the required* attribute to the input elements in the first fieldset.
        ex: 
        <input id="first-name" type="text" required />

- minlength attribute:

    -   It's a custom password validation
    -   This attribute allowed to prevent inputs of less x    characters beign submitted, with value x...
    
        minlength="8"

        The above is a regular expression which matches eight or more lowercase letters.

        ex:
                <label for="new-password">Create a New Password: <input id="new-password" type="password" minlength="8" required />

- The attribute pattern define a regular expression that the password must match to be considered valid.

        pattern="[a-z0-5]{8,}"

        ex:
                <label for="new-password">Create a New Password: <input id="new-password" type="password" pattern="[a-z0-5]{8,}" required />

                ** notice that minlenght has been removed.



**    To relate the radio inputs, because we only want one radio input to be selectable at a time. 

    + Give' em the same name attribute
    + within a account-type value ...

    placing this account-type is not possible to select two or more radios at the same time

Follow accessibility best practices:
     by linking the input elements and the label elements in the second fieldset.

        ex:
            <fieldset>
                <label for="personal-account"><input id="personal-account"type="radio" name="account-type" /> Personal Account</label>
                <label for="business-account"><input id="business-account"type="radio" name="account-type" /> Business Account</label>
                <label for="terms-and-conditions"><input id="terms-and-conditions"type="checkbox" required /> I accept the terms and conditions</label>
            </fieldset>

# <input type="file"/> allows a user to upload a profile picture
        ex: 

    <fieldset>
    <label>Upload a profile picture: <input type="file" /></label>
    </fieldset>

    attribute min="" users under certain age should not register.
    attribute max="" users users probably will not register over a max age...
        ex: 13 an 100 (years).

Adding a dropdown to the form is easy with the select element. The select element is a container for a group of option elements, and the option element acts as a label for each dropdown option. Both elements require closing tags.

select tag, and optioni tag will do a dropdown to select among several otions and send it to server.
Submitting the form with an option selected would not send a useful value to the server. As such, each option needs to be given a value attribute. Without which, the text content of the option will be submitted to the server.

With form submissions, it is useful, and good practice, to provide each submittable element with a name attribute. This attribute is used to identify the element in the form submission.

check out vertical-align property...
