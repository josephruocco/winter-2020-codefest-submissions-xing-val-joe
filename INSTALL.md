## Schedule It!

The Scheduler  is a Python Flask application to scan your google calendars, find chunks
of free time, and allow you to schedule events in those times.

## Use a virtual environment
	    virtualenv -p python3 <name>
	    . <name>/bin/activate
	    
### Installing Dependencies

	    pip install flask requests python-dateutil rfc3339 
	    pip install git+https://github.com/mitsuhiko/flask-oauth
	   
The Scheduler is built on Python 3.5 and requires Flask and the
Google API.

### Running

#### Google Credentials

 You must fill the included JSON file with information from the  Google API Service account.
section to learn how. Save the JSON file in the *SAME* folder as `app.py` (i.e. the project root folder) as
`keys.json`. The name *MUST* be `keys.json`.

the Google Api Key and oauth credentials are made following simple instructions.

### Oauth client credentials
javascript origin:
    http://localhost:5000/

Redirect_URI
    http://localhost:5000/authorized

these details must be filled in *AS IS* or the api will throw an error.

### SECRET_KEY

 you must create a randomized secret key to generate a session.

     	  $ python3
	  > import os
	  > os.urandom(24)

copy the generated key into "" in the json file. Note: the key generated should *NOT* have any '\' characters, as the json file will not be able to handle it. replace these characters with an alphanumeric one.

#### Starting up the application

To run the application, simply start the server using:

```
$ python app.py
```

### Troubleshooting
- python app.py runs at https://localhost:5000/
- rfc3339  is a small library to format dates to rfc3339 strings (format for Google Calendar API requests), 
- flask-oauth is used in place of the old lib on pypi.
