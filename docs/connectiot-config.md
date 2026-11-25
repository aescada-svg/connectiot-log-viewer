# ConnectIoT Configuration

## Http Transport

- Point the ConnectIoT **Http** transport to your local viewer endpoint (for example, http://localhost:8000/...).
- Send JSON payloads so iewer.py can parse fields and stream events over SSE.
- Include managerId in payloads to group logs by manager; payloads missing managerId default to "Orphan".
