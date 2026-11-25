# ConnectIoT Configuration


- Point the ConnectIoT **Http** transport to your local viewer endpoint (`http://localhost:8000/logs`).
- Send JSON payloads so `viewer.py` can parse fields and stream events.

Example `config.json` file for ConnectIoT:

```jsonc
  ...
	"logging": [
		{
			"id": "LocalWebLogViewer",
			"type": "Http",
			"options": {
				"host": "localhost",
				"port": 8000,
				"path": "/logs",
				"ssl": false,
				"timestampFormat": "HH:mm:ss.SSSSS",
				"format": "${log.timestamp} ${log.level}:${log.message}",
				"level": "debug",
				"isEnabled": true
			},
			"applications": [
				"*"
			]
		},		
		{
			"type": "Console",
			"options": {
      ...
	
