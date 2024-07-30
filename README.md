# NodeRedLearn

[
    {
        "id": "97ea30bf766d6072",
        "type": "tab",
        "label": "Flow 4",
        "disabled": false,
        "info": "",
        "env": []
    },
    {
        "id": "e99c621dfb0b2f24",
        "type": "http in",
        "z": "97ea30bf766d6072",
        "name": "",
        "url": "/Testing",
        "method": "get",
        "upload": false,
        "swaggerDoc": "",
        "x": 570,
        "y": 240,
        "wires": [
            [
                "3bdea5616ff12e17"
            ]
        ]
    },
    {
        "id": "4b216c56974038cd",
        "type": "http response",
        "z": "97ea30bf766d6072",
        "name": "",
        "statusCode": "200",
        "headers": {},
        "x": 900,
        "y": 240,
        "wires": []
    },
    {
        "id": "baf37b3de8487183",
        "type": "inject",
        "z": "97ea30bf766d6072",
        "name": "make request",
        "props": [
            {
                "p": "payload"
            },
            {
                "p": "topic",
                "vt": "str"
            }
        ],
        "repeat": "",
        "crontab": "",
        "once": false,
        "onceDelay": "",
        "topic": "",
        "payload": "",
        "payloadType": "date",
        "x": 530,
        "y": 300,
        "wires": [
            [
                "b0a3748f8e5c118b"
            ]
        ]
    },
    {
        "id": "b0a3748f8e5c118b",
        "type": "http request",
        "z": "97ea30bf766d6072",
        "name": "Testing",
        "method": "GET",
        "ret": "obj",
        "paytoqs": "ignore",
        "url": "http://host.docker.internal:1881/Testing",
        "tls": "",
        "persist": true,
        "proxy": "",
        "insecureHTTPParser": false,
        "authType": "",
        "senderr": false,
        "headers": [
            {
                "keyType": "Content-Type",
                "keyValue": "",
                "valueType": "application/json",
                "valueValue": ""
            }
        ],
        "x": 684.5,
        "y": 300,
        "wires": [
            [
                "cd4ed740ade71696"
            ]
        ]
    },
    {
        "id": "cd4ed740ade71696",
        "type": "debug",
        "z": "97ea30bf766d6072",
        "name": "",
        "active": true,
        "tosidebar": true,
        "console": false,
        "tostatus": false,
        "complete": "true",
        "targetType": "full",
        "statusVal": "",
        "statusType": "auto",
        "x": 870,
        "y": 300,
        "wires": []
    },
    {
        "id": "3bdea5616ff12e17",
        "type": "function",
        "z": "97ea30bf766d6072",
        "name": "function 3",
        "func": "msg.payload = \"Tests\"\nreturn msg;",
        "outputs": 1,
        "timeout": 0,
        "noerr": 0,
        "initialize": "",
        "finalize": "",
        "libs": [],
        "x": 740,
        "y": 240,
        "wires": [
            [
                "4b216c56974038cd"
            ]
        ]
    }
]
