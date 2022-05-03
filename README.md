# microservices_python
**Tasks**
- Install Python
- Creating Python Virtual Environments
- Installing Python VS code extension
- Sample Flask application
- Jinja templating for dynamic web pages
- using pip to free python dependencies
- Building the docker image using dockerfile
- Writing Docker compose file
- Writing Kubernetes manifest files for the application
- Creating Helm chart

**Process of Creating an API**
- create virtual environment '''C:\Users\viswa\Downloads\microservices_python>python -m venv tutorial-env'''
- Activate virtual environment  '''C:\Users\viswa\Downloads\microservices_python>tutorial-env\Scripts\activate.bat'''     
- Install flask in the virtual env '''(tutorial-env) C:\Users\viswa\Downloads\microservices_python>pip install Flask'''
- Create SRC folder and app.py file in that, copy the minimal flash application in the app.py file
    *from flask import Flask*
    *app = Flask(__name__)*
    *@app.route("/")* ----> creates the endpoint "/"
    *def hello_world():*
        *return "<p>Hello, World!</p>"*
    *if __name__ == '__main__':*
        *app.run(host='0.0.0.0', port=5000)*
- run ''' (tutorial-env) C:\Users\viswa\Downloads\microservices_python\SRC>python app.py '''
- it will give the url & port on which it is running 
 ''' Running on http://192.168.1.36:5000 (Press CTRL+C to quit)'''
- check the URL on a web browser "http://192.168.1.36:5000"
- This is the first endpoint "/"( @app.route("/")) which displays Hello World

- create another end point "/health" to check if the container is alive or dead
    *@app.route("/health")*
        *def health():*
            *return jsonify(status="Up")*

- http://192.168.1.36:5000/health is the endpoint which give the output * { "status": "Up"}*

