# Join / Leaving / Creating / Deleting
  How To Join / Leave Servers / Delete Servers With Requests
  
# Creating A Guild
```py
import requests

payload={
  'channels': "null"
  'icon': "null"
  'name': "Dropout's server"
  'region': "sydney"
}

r = requests.post('https://discordapp.com/api/v8/guilds', headers={'Authorization': "Token Here"}, data=payload)
if r.status_code == 201:
  print('Success')
else:
  print('Error')
```

# Deleteing A Guild
```py
import requests

r = requests.post('https://discordapp.com/api/v8/guilds/GUILD_ID_HERE/delete', headers={'Authorization': "Token Here"})
if r.status_code == 201:
    print('Success')
else:
    print('Error')
```    

# Joining A Guild
```py
import requests

r = requests.post('https://discordapp.com/api/v8/invites/discord-api', headers={'Authorization': "Token Here"})
if r.status_code == 200:
    print('Success')
else:
    print('Error')
```

# Leaving A Guild
```py
import requests

r = requests.delete('https://discordapp.com/api/v8/users/@me/guilds/GUILD_ID_HERE', headers={'Authorization': "Token Here"})
if r.status_code == 201:
    print('Success')
else:
    print('Error')
```    
