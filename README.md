## RASA

```
https://rasa.com/docs/rasa/command-line-interface/
```

### build

python 3.9

```
pip install rasa


rasa train

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

> Security Considerations

```
rasa run \
    --enable-api \
    --auth-token thisismysecret

```

```
curl -XGET localhost:5005/conversations/default/tracker?token=thisismysecret
```
