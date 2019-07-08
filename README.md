# gcp-building-app
This effort is based on https://cloud.google.com/appengine/docs/standard/python3/building-app/.

# Issues
* The version of the javascript libraries described in the documentation does not work.
* Firebase initially prompts for email, user name, and password.  I had assumed
  that by specifying the gmail address, the credentials will be used from that.
  It appears as if the initial login is also doing some registration.
* It is not clear how one can add custom fields to the token that the flask back end
  receives.
* Flask token implementation is bound to GCP.  Not clear how this will integrate
  with other environments, both cloud and on-premise.  One may need separate
  token handling modules per target deployment platform.
* During registration app may need to capture specific fields in addition to user name,
  password, and email.  Not clear how this is achieved.
* How will a python client be able to access the API using Firebase?