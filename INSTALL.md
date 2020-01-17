#  Installation Instructions
three steps to get you up and running...
## 1. create a virtual environment
	    virtualenv -p python3 <name>
	    . <name>/bin activate
## 2. install pip requirements 
	

	    pip install flask requests python-dateutil rfc3339 
	    pip install git+https://github.com/mitsuhiko/flask-oauth
	    python app.py
## 3.  run

    python app.py

FYI:
- python app.py runs at https://localhost:5000/
- rfc3339  is a small library to format dates to rfc3339 strings (format for Google Calendar API requests), 
- flask-oauth is used in place of the old lib on pypi.

