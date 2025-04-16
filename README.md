Local server setup

1) Use python 3.10
2) create a virtual env C:\Users\91998\AppData\Local\Programs\Python\Python313\python.exe -m venv .venv
3) install mcp package and uv
	python -m pip install --upgrade mcp[cli]
	pip install uv
4) use node version v22.14.0
5) mcp dev calc.py
6) in your local host it will run MCP inspector
	http://127.0.0.1:6274/#prompts
	
	select Transport Type as STDIO
	command as uv
	Arguments 
	run --with mcp mcp run calc.py

Integrating with cursor tool
1) Install cursor tool in your local machine
provide the mcp.json as follow
{
  "mcpServers": {
    "server-name": {
      "command": "C:\\Users\\91998\\AppData\\Local\\Programs\\Python\\Python313\\python.exe -m uv",
      "args": ["run --with mcp mcp run C:\\Users\\91998\\mcp\\calc.py"]
    }
  }
}
2) In chat verify the results of the prompt

	
	![image](https://github.com/user-attachments/assets/50040bcf-440b-4c1f-b3dd-bac964112d03)

	
