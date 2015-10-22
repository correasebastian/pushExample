POST /api/v1/push HTTP/1.1
Host: push.ionic.io


/*this is the api secret key with 64 encode */
Authorization: Basic xxxxxxxx
X-Ionic-Application-Id: xxxxxxx


Content-Type: application/json
Cache-Control: no-cache

{
    "tokens": ["DEV-b5a92fe8-0b98-4ba1-bb8e-03db06d0eeaf"],
    "notification": {
        "alert": "mtricula del ABC",
        //probe con un payload para web pero no funciona, ahora puerbo con android
        "android": {
            "collapseKey": "foo",
            "delayWhileIdle": true,
            "timeToLive": 600,
            "payload": {
                "message": "matricula disponible",
                "title": "ABC",
                "key1": "value",
                "key2": "value",
                "$state": "tab.chat-detail",
                "$stateParams": "{\"idinspeccion\": \"2015-07-23T16:52:44.114Z\", \"placa\":\"FFF358\"}"
            }
        }
    }
}