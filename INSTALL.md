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

 You must obtain a JSON file for a Google API Service account. See the links provided in the 'For Development'
section to learn how. Save the JSON file in the *SAME* folder as `app.py` (i.e. the project root folder) as
`gcreds.json`. The name *MUST* be `keys.json`.

#### Starting up the application

To run the application, simply start the server using:

```
$ python app.py
```

### Troubleshooting
- python app.py runs at https://localhost:5000/
- rfc3339  is a small library to format dates to rfc3339 strings (format for Google Calendar API requests), 
- flask-oauth is used in place of the old lib on pypi.
