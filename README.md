node-nocache
============


## Introduction

An node `express` middleware which add no-cache related headers for all the express response to disable caches. 
It is useful for REST API response, add no-cache headers to avoid browsers cache request response.

The following headers are added to response header:

    Cache-Control: no-cache, no-store, must-revalidate
    Expires: -1
    Pragma: no-cache


## Install

    npm install node-nocache


## Usage

    let nocache = require('node-nocache');

    app.use(nocache());

or use you can only add no-cache header to specific requests with `router`

    router.all('*', require('node-nocache'));


