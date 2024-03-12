# homebridge-nature-remo-air-purifier
 [Homebridge](https://github.com/homebridge/homebridge) plugin to send power on and off to an air purifier using [Nature Remo](https://nature.global/nature-remo/).

## Installation
```bash
npm install -g homebridge-nature-remo-air-purifier
```

## Example config.json
```json
  "accessories": [
    {
      "name": "[Name display in Home app]",
      "access_token": "[Your access_token]",
      "signal_ID_on": "[aaaaaaaa-aaaa-aaaa-aaaa-aaaaaaaaaaaa]",
      "signal_ID_off": "[bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb]",
      "accessory": "NatureRemoAirPurifier"
    }
  ]
```
- `name` can be set whatever you want
- To get `access_token`, visit https://home.nature.global/
- To get `signal_ID_on` and `signal_ID_off`, run `curl -X GET "https://api.nature.global/1/appliances" -H "Authorization: Bearer [access_token]"` and find `id` key
- `accessory` must be `NatureRemoAirPurifier`
