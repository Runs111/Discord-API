# Adding / Removing / Declining / Blocking
  Yeah Very Cwool Im Running Out Of Description TEXT
  
# Adding
```py
import requests

payload={
    'discriminator': '1337' # If Theres A 0 It Dosent Count As Somthing I Guess So If There Discrim Was 0001 You Would Use 1
    'username': "Dropout"
}

r = requests.post('https://discordapp.com/api/v8/users/@me/relationships', headers={'Authorization': "Token Here"}, data=payload)
if r.status_code == 204:
    print('Success')
else:
    print('Error')
```

# Removing
```py
import requests

r = requests.delete('https://discordapp.com/api/v8/users/@me/relationships/USER_ID_HERE', headers={'Authorization': "Token Here"})
if r.status_code == 204:
    print('Success')
else:
    print('Error')
```

# Declining
```py
import requests

r = requests.delete('https://discordapp.com/api/v8/users/@me/relationships/USER_ID_HERE', headers={'Authorization': "Token Here"})
if r.status_code == 204:
    print('Success')
else:
    print('Error')
```

# Blocking
```py
import requests

r = requests.put('https://discordapp.com/api/v8/users/@me/relationships/USER_ID_HERE', headers={'Authorization': "Token Here"}, data={'type': "2"})
if r.status_code == 204:
    print('Success')
else:
    print('Error')
```
