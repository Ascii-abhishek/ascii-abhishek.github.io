# Venv Module

---

- Create new Virtual environment:<br>
    ``` Python -m venv project_name ```

- Create a virtual environment with access to all the global installed libraries also: ## Caution: removing a library here will remove the library globally too, but installing new one and then removing new ones wont affect the global list <br>
    ``` Python -m venv my_project --system-site-packages ```

- Activate newly created virtual environment: <br>
    ``` Project_name\Scripts\activate.bat```

- To save all the installed installed libraries into a requirement.txt file:<br>
    ``` Pip freeze > requirements.txt```

- To install all libraries listed in requirements.txt in new venv project:<br>
    ``` Pip install -r requirements.txt # filename can be anything```

- To deactivate environment: <br>
    ``` Deactivate ``` # it will only deactivate virtual environment, it will not delete the project directory and files created.

**Note:** It is best practice to make 'venv' directory in main project directory and never to put any project file or folder in venv directory, virtual environments must be considered as a use and throw elements. Also we should never commit 'venv' directory to source control also.
