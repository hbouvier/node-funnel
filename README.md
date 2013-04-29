# A funnel to queue requests based on a limited number of resources

When you have limitted resources (e.g. CPUs) to process multiple requests,
you can use a funnel to queue the request to be served by each resource when
they become available.

#LICENSE:

This module is licensed under the Apache License v2.0

# Installation

npm install node-funnel

# Include this as a module in your own project

    var Funnel = require('./funnel'),
        funnel = new Funnel();  // One executor per CPU
        
    funnel.queue($this, $this.generate, filename, text, voice, function(/*err, filename */) {
    });
    