* If getting error that scripts not allowed
- Open admin powershell
- 'Set-ExecutionPolicy RemoteSigned' > Yes
- back to terminal in app directory
- .venv/Scripts/activate

* To run the server:

1) Set environment variables
    * In powershell
    - $env:FLASK_APP = "application.py"
    - $env:FLASK_ENV = "development"

2) 'flask run'

* To quit the server
- ctrl-c

* To set up a database
1) Enter python interactive mode
    - 'python' > should get >>>
2) 'from application import db'
    - 'application' is just the name of the main py file
3) 'db.create_all()'
4) Import your model
    - Ex: from application import Drink
5) Declare a row/object
    - Ex: drink = Drink(name="whatever", description="whatever")
    - can view the variable by typing it in (ex: drink)
6) db.session.add(variableName)

**Note: can do it inline > db.session.add(Drink(...))

7) db.session(commit)
8) Can check the db with Drink.query.all()
9) To exit the session (exit())