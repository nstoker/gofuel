# Notes

A single page application will be served, that talks to an api. Step one is going to be the api. Probably.

## Users

### Signup

Requires user email address.

Creates a record in users table with a unique registration_token and the timestamp created. An email to the user will be sent containing the registration token.

The user will have a short period to register (4 hours?). Some sort of timeout mechanism is needed to delete records that have not been authenticated.

### Authentication

Requires email address and the registration token. If successful, then the user will be prompted to select a password.

### Signin

Requires email address and password. The password will be encrypted before sending (TODO) to the server.

If the email and password hash match, then the user will be signed in.

Otherwise a generic 'the email and password were not recognised.

The sign in page will have a forgotton password link.

### Password reset

The page will request the email address. On selection, a message along the lines of 'check your email account for a password reset link'. The reset link has a limited lifetime.
