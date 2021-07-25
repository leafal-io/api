# Success (800)
A response with code **800** has encountered no errors in reading or applying your information.

# Error range (9xx)
A response that falls within the 9xx range encountered an error. There are a few universal error codes, as well as some path-specific ones.

## 901: No public key provided.
The request did not provide a public key in the form of a `Client-Id` header. 

### Possible solutions
- [Temporary] Before the 2022 leafal.io Web relaunch, this could be solved by adding `/index.php` to the end of the request path.

## 902: No application found.
There was no application found with the provided public key.

## 903: Username and/or password were empty.
**Specific to:** `/auth/token`.
The username and/or password fields were left empty, whether intentional or not. 
- [Temporary] In rare cases before the 2022 leafal.io Web relaunch, Error 903 can be resolved with the same solution at Error 901, by adding `/index.php` to the end of the request path.

## 904: User not found.
**Specific to:** `/auth/token`.
The API could not identify a user with the provided information.

## 905: Invalid password.
**Specific to:** `/auth/token`.
The provided password did not match the database records.
