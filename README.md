# enigma_for_home_assistant



This is only the correction from KavajNaruj
https://github.com/KavajNaruj/homeassistant-enigma-player

-> Now my dreambox 800sev2 (newnigma) works with home assitant 0.56.1


Changes:

bouquets_xml = self.request_call('/web/bouquets')
to
bouquets_xml = self.request_call('/web/getservices')


NOTE:
The enigma.py must be in this directory:
/home/homeassistant/.homeassistant/custom_components/media_player/

-> if not exist, then make the directory with mkdir .......
-> I also changed the owner with chown " sudo chown -R homeassistant:homeassistant NEW_DIRECTORY"

You only have to do this, after creating the directories:
sudo chown -R homeassistant:homeassistant /home/homeassistant/.homeassistant/custom_components



HA Configuration (configuration.yaml):
**************************************

media_player:
  - platform: enigma
	host: IP_FROM_DREAMBOX



-> I don't have an authentifiocation on my dreambox


