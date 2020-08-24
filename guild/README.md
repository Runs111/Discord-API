# Join / Leaving / Creating / Deleting
  How To Join / Leave Servers / Delete Servers With Requests
  
# Creating A Guild
```py
import requests

payload={
  channels: null
  icon: null
  name: "Dropout's server"
  region: "sydney"
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

r = requests.post('https://discordapp.com/api/v8/guilds/747317738988372068/delete', headers={'Authorization': "Token Here"})
if r.status_code == 201:
    print('Success')
else:
    print('Error')
```    
