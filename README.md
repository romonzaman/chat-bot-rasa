### build

python 3.9

```
pip install rasa
```

### deploy

```
rasa run
```

### API

- request

> [POST] http://localhost:5005/webhooks/rest/webhook

```
{
  "sender": "1001",
  "message": "hi"
}
```

- response

```
[
    {
        "recipient_id": "1001",
        "text": "Great, carry on!"
    }
]
```
