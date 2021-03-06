Google Analytics Server Side Changelog
======================================

Version 0.7.0 Beta
------------------

- Convert into a small framework under GASS PHP 5.2 virtual namespace (for backwards compatability)
- Add in autoloader for new GASS virtual namespace
- GASS_Http singleton so can be used anywhere in framework without passing options around
- GASS_Http uses adapters, defaults to Stream, can also use cURL, ability for developer to write own adapters
- GASS_BotInfo which detects if user-agent is a bot or not separated out as not required
- GASS_BotInfo uses adapters, php's BrowserCap is default, but original UserAgentString.info is also available, developer can write own adapters

Version 0.6.4 Beta
------------------

- Ensure bots.csv is not empty when received from url and ensure lines in csv aren't empty before dealing with them

Version 0.6.3 Beta
------------------

- Ensure set cookie headers are only sent out once

Version 0.6.2 Beta
------------------

- Add in check to ensure cURL extension has been installed when the class is instantiated

Version 0.6.1 Beta
------------------

- Allow setting/getting of any class level variable with a publicly available get/set method via getOption/setOption methods

Version 0.6.0 Beta
------------------

- Ability to ignore logging statistics for web trawling bots and spiders and caching of the bots list
- Auto-setting of latest GA version number from ga.js
- Auto-setting of accepted language from headers
- Ability to pass options to curl
- Remove auto-setting of charset from headers, default to UTF-8 (response should define this, not request headers)
- Try manually reporting IP address to GA as done in the GA mobile code
- str_getcsv is not available in PHP before PHP 5.3 so added in a crude implementation so it works in lower than 5.3

Version 0.5.5 Beta
------------------

- Set Document-Referer by default and check url format
- Add extra Exceptions thrown in required circumstances
- Ensure explode on cookies only returns no of parts required
- Add Traffic source string with utmz cookie
- Update PHPDoc in code
- Update Readme with extra info & to correct markdown format


Version 0.5.0 Beta
------------------

- Initial Release
- Provides basic PageView and Event functionality, setting cookies in correct format