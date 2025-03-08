# Few get starter UV commands

*1.* Download uv from official docs via powershell.

*2.* ```uv version``` -> to check version.

*3.*  ```uv help```  -> displays all uv commands.

*4.* ```uv init .``` -> converts project to uv in existing folder.
 
```uv init projectname``` -> makes project from scratch.

*5.* *pyproject.toml* file is very important in uv;
It defines everything section wise -> denoted with ```[]```.

*6.* ```uv run hello.py``` -> to run python file.
_this will create a *.venv* file_.

*7.* Connect your project with this *.venv* file  by clicking on python version at bottom of vscode then click on the recommended one.

*8.* Can change python version from *.python-version* file.
_but ensure to update version in *toml* file as well_

*9.* ```uv init --package projectname``` -> to make project following package rules.
_Will make src folder_



## After making project following package rules

*1.* There'll be 3 sections in *toml* file b/w ```[]``` 

Most important entry point here is ```[project.scripts]``` 
_Can make *custom commands*  from here_

*Default*
 ```projectname = "projectname:main"``` 
_file *path* on colon's left and *function name* on its right_
 ```uv run projectname``` -> to run script 

*Eg 2*
 ```karachi = "projectname.hello:myfunction"``` 

 ```uv run karachi``` -> to run the script
