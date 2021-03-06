# express-server-status
Get a quick overview of the status of an express server (uptime, version, stats)

A forked project from https://github.com/opencollective/express-server-status
## Installation

    npm install express-server-status-minus-git --save:
## Usage

    var serverStatus = require('express-server-status-minus-git');
    var express = require('express');
    var app = express();
    
    app.use('/status', serverStatus(app));
    
## Example
 
`curl localhost:3000/status`


    { 
      server: { 
        status: 'up',
        description: 'OpenCollective API',
        version: '0.0.5',
        uptime: 3,
        uptime_human: 'a few seconds ago',
        requests: { 
          total: 1, 
          last_minute: 0, 
          last_5mn_avg: 0, 
          last_15mn_avg: 0 
        } 
      },
      git: { branch: 'master', sha: '1f86caa' } 
    }