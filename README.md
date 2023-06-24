## fs-water
FiveM Water Manager

```My Discord```
- [Discord](https://discord.gg/UFng7DWnWP)


## 
```
local value = 1.0 -- initial value

CreateThread(function()
    while true do
        Wait(0)
        Citizen.InvokeNative(0xC54A08C85AE4D410, value) -- set the value
    end
end)
```
```
RegisterCommand("setvalue", function(source, args)
    local newvalue = tonumber(args[1])
    if newvalue ~= nil and newvalue >= 0.0 and newvalue <= 3.0 then -- check if the new value is valid
        value = newvalue
        print("Value set to " .. newvalue)
    else
        print("Invalid value. Please enter a number between 0.0 and 3.0")
    end
end, false)
```
## fxmanifest.lua
```
fx_version 'cerulean'
game 'gta5'

client_scripts {
    'client.lua'
}
```
