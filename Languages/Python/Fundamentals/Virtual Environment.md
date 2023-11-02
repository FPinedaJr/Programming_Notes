create virtual environment
```
<python path> -m venv <venvName>
python -m venv .venv
```

activate virtual environment
```
venvName\Scripts\activate.bat
```

keep track of your dependencies: `requirements.txt`
dependencies only used for development: `requirements-dev.txt`
```requirements.txt
flask==1.0.0
requests             # default is the latest version
gunicorn
```

automatically install all dependencies
```
pip install -r requirements.txt
```



