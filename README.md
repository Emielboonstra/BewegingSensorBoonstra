# BewegingSensorBoonstra
Beweging sensor Boonstra



Dit in de esphome cofig(API_key veranderen):


substitutions:
  name:  bewegingsensor-boonstra
  friendly_name: Bewegingsensor Boonstra
  
packages:
  Boonstra.Bewegingsensor: github://EmielBoonstra/BewegingSensorBoonstra/bewegingsensor-boonstra-ha.yaml@main
  
esphome:
  name: ${name}
  name_add_mac_suffix: false
  friendly_name: ${friendly_name}
  
# Enable Home Assistant API
api:
  encryption:
    key: {{API_KEY}}

wifi:
  ssid: !secret wifi_ssid
  password: !secret wifi_password
