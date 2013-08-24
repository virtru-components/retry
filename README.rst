retry
=====

Retries an action until it succeeds or is told to stop retrying. 

Usage::
    
    var retry = require('retry');

    retry(function(again, stop) {
      ... some action ...

      if(successful) {
        stop();
      } else {
        // Will try again after a set timeout. This timeout will increase
        // exponentially
        again();
      }
    });
