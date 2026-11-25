# ConnectIoT Configuration

## Http Transport

<<<<<<< HEAD
- Point the ConnectIoT **Http** transport to your local viewer endpoint (for example, http://localhost:8000/...).
- Send JSON payloads so viewer.py can parse fields and stream events over SSE.

Example config.json file for ConnectIoT:
  ...
	"logging": [
			{
=======
- Point the ConnectIoT **Http** transport to your local viewer endpoint (`http://localhost:8000/logs`).
- Send JSON payloads so `viewer.py` can parse fields and stream events.

Example `config.json` file for ConnectIoT:

```jsonc
  ...
	"logging": [
		{
>>>>>>> a72a061 (Refine ConnectIoT config example)
			"id": "LocalWebLogViewer",
			"type": "Http",
			"options": {
				"host": "localhost",
				"port": 8000,
				"path": "/logs",
				"ssl": false,
				"timestampFormat": "HH:mm:ss.SSSSS",
<<<<<<< HEAD
				"format": "${log.timestamp} ${log.level}: ${log.message}",
=======
				"format": "${log.timestamp} ${log.level}:${log.message}",
>>>>>>> a72a061 (Refine ConnectIoT config example)
				"level": "debug",
				"isEnabled": true
			},
			"applications": [
				"*"
			]
<<<<<<< HEAD
		},		
		{
			"type": "Console",
			"options": {
      ...
	
=======
		},
		{
			"type": "Console",
			"options": {
      ...
>>>>>>> a72a061 (Refine ConnectIoT config example)
