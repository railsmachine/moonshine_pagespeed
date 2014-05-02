# Moonshine_Pagespeed

### A plugin for Moonshine[http://github.com/railsmachine/moonshine]

A plugin for installing and configuring Google's mod_pagespeed[http://code.google.com/speed/page-speed/].

### Instructions

* Install the plugin
    script/plugin install git://github.com/railsmachine/moonshine_pagespeed.git
    
* Include the recipe in your Moonshine manifest
    recipe :pagespeed
    
* Configure it as desired

    configure(
      :pagespeed => {
        :enabled => true, # set to false to turn pagespeed off
        :cache_path => '/var/mod_pagespeed/cache/',
        :file_prefix => '/var/mod_pagespeed/files/',
        :enabled_filters => [], # enable filters
        :disabled_filters => [], # disable filters
        :extra_domains => [] # CDNs to allow resources from, etc
      }
    )
