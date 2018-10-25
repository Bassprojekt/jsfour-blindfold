# jsfour-blindfold
This script lets you use a blindfold on the nearest player.

### LICENSE
Please don't sell or reupload this resource

### INSTALLATION
* You need to have ESX installed
* Run the SQL-file
* Add the event to a menu or a button, example below

### Screenshot
![screenshot](https://i.gyazo.com/thumb/1200/ea01b13e36b33c3e38a9adceb9e88708-png.jpg)
![screenshot](https://i.gyazo.com/thumb/1200/622e916016a518ab3e1825fc1098b70e-png.jpg)

### Example
```
if data.current.value == 'blindfold' then
	local player, distance = ESX.Game.GetClosestPlayer()

	if distance ~= -1 and distance <= 3.0 then
	   ESX.TriggerServerCallback('jsfour-blindfold:itemCheck', function( hasItem )
	      TriggerServerEvent('jsfour-blindfold', GetPlayerServerId(player), hasItem)
	   end)
	else
	   ESX.ShowNotification('Ingen i närheten')
	end
end
```
