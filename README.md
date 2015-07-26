# hawk-auth

A simple Polymer element to provide log in and sign up forms. With a single tag
you will get an element containing a log in and sign up form, with material
design paper elements.

![hawk-auth example](http://i.imgur.com/xdXy35g.png)

## Installation

You can install the component by running:

    bower install --save hph/hawk-auth

## Usage

Add the tag to your project:

    <hawk-auth></hawk-auth>

You will get a container with a log in and a sign up form in two tabs. The
default configuration is to make `POST` requests with the provided `username`
and `password` values to `/login` and `/signup`, but these values can be
customized. For instance, the following element will use `email` instead of
`username`, use different paths and add an extra `password_confirmation` field
to the sign up form:

    <hawk-auth identifier="email" login-path="/users/sign_in" signup-path="/users">
      <paper-input-container class="signup">
        <label>Password confirmation</label>
        <input is="iron-input" name="password_confirmation" required>
      </paper-input-container>
    </hawk-auth>
