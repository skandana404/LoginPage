Create a Login Page using 
 [HTML, CSS, Flask for backend] 
# Prerequisites before starting 
Before running the app, make sure these are installed on your system: 
## 1. Install Required Python Applications
   
 1.1 Python (3.x) 
 
 Download from: https://www.python.org/downloads/ 
 
 During installation, make sure to check the box that says: "Add Python to PATH" 

 1.2 pip (Python package installer) 
 
 Usually comes with Python. Otherwise install it 
 
 To check if it's available using syntax: pip --version

 1.3 Install Flask 
 
 Open Command Prompt and run: pip install flask 
 
## 2. Install Text Editor / IDE
   
To write and edit your frontend files: VS Code  Recommended 

• Recommended VS Code Extensions (Optional but Helpful)  is HTML CSS 
Support  

 # Tech Stack

- **Frontend**: HTML, CSS
- **Backend**: Python (Flask)


# Set Up the Project and Run Code

1. Create a folder structure in VS Code as follows: 
• Folder Structure 
<pre> ``` login-app/ ├── app.py ├── templates/ │ └── login.html ├── static/ │ └── style.css ``` </pre>
 
 
2. Check whether the prerequisites are installed  
For Python versions: On Windows 
Method 1: Using Command Prompt (CMD) 
In the terminal, type: python --version or python -V, pip show flask 
Method 2: (Using VS Code Terminal) 
In VS Code, open the terminal (Ctrl + `) and run: python --version or py –version,  
pip show flask 
 
3. Run the Flask App 
• Open Command Prompt or VS Code Terminal. 
• Navigate to the project folder. eg:  cd path\to\your\project\login-app 
• Run the app: python app.py 
If everything is correct, you should see output like:  
* Running on http://127.0.0.1:5000/ 
 
4. Open in Browser 
Open your browser and go to: http://127.0.0.1:5000/ 
This will load the login page from the Flask server. 
 
5. Test Login 
Use the following dummy credentials to log in: 
• Username: admin 
• Password: password123 
 
 
# Flask (Python Backend) APIs and Methods 
 
Line	Type	                                            Purpose
Flask(__name__)	 ---------------------------------->  Initialization	Creates a Flask app instance

@app.route('/')	API Route	--------------------------> Defines API endpoint at / that accepts default GET requests

@app.route('/login', methods=['POST']) -------------> API Route	Defines API endpoint at /login that accepts POST requests

def home(): and def login(): -----------------------> Method	Python functions are called when the above API routes are hit

render_template('login.html')	----------------------> Flask Method	Renders an HTML file from the templates folder

request.form['username'] ---------------------------> Flask Method	Retrieves form data sent via POST request for username

request.form['password']	---------------------------> Flask Method	Retrieves form data sent via POST request for password

app.run(debug=True)	     ---------------------------> Flask Method	Starts the Flask development server with debug mode 
 
# Functionality 
 
1. Render Login Page 
o The application displays a styled login form when you visit the homepage 
 (/ route). 
2. Collect User Credentials 
o Accepts username and password inputs from the user using an HTML form. 
3. Handle POST Request 
o Submits the form data via HTTP POST to the /login route securely. 
4. Hardcoded Authentication Check 
o Validates user credentials against predefined values (admin / 
password123). 
 
5. Display Login Result 
o Shows a success message (Welcome, admin!) if credentials are correct. 
o Shows a failure message (Invalid username or password.) if credentials are 
incorrect. 
 
# Planned Features 
- User registration system
- Database-backed authentication
- Secure password hashing, prevents exposing actual passwords
- Session-based login and logout
 - Flash messages for user feedback
  - Forgot password and email verification 
 
# Workflow 
1. User opens the application 
The user navigates to http://127.0.0.1:5000/ in a web browser. This triggers the 
Flask app to render and display the login page (login.html). 
2. User enters login credentials 
The user provides a username and password in the form and clicks the "Login" 
button. 
3. Form submits a POST request 
The form sends a POST request to the /login route defined in the Flask backend 
(app.py). 
4. Backend receives and processes data 
Flask extracts the form data using request.form['username'] and 
request.form['password']. 
5. Credentials are validated 
The entered credentials are compared against hardcoded (or later, database
stored) credentials. 
6. Response is returned to the user 
o If credentials are valid, the user sees a welcome message. 
o If credentials are invalid, an error message is displayed. 
 
