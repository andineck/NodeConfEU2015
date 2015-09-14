# NodeConfEU 2015
> Waterford, Ireland

__Personal Notes__ from @andineck


I attended most of the talks, but missed a few.
No claim for correctness or completeness.


# linux foundation (node), open source
> @DivaDanese
  Danese Cooper

- give more value than you take
- be generous
- open source people are better


# tigital transformation
> @rjrodger
  Richard Rodger

- deads reckogning, rope with knots throwing out, cumulative error
- john harrison, solved time on ship problem, got 20'000 Pound from british goverment
- created a technical superior solution to a technical need
- same worked out with node
- when introduced, people think the solution does not work good enough
- why is node effective, rapid innovation delivering, delivering early value
- development speed, how long does it take to deliver a CEO initiative
- technical debt, traditional platforms mean lots of complex buggy code
- with node, there is less less technical debt, fewer bugs, easier to change.
- number of bugs is linear with the lines of code (~0.4 bugs for 1000 LOC)
- ceremonial overhead with teams
- small pieces, loosely coupled, deep open source nature
- microservices, small, agile, adaptable, modern enterprise architecture
- example: london school of marketing

# docker
> @anaptfox
  Taron Foxworth

- container bound with data
- when the container is gone, the data is gone too
- backups when the server is gone
- mongodump -> dat, version controlled decentralized data
- module -> sync

# ida business development in ireland

# groupon
> clovis chapman

- in the beginning simple solution, simple website
- massive growth from 40'k to 40'M

1. ngingx, ruby , db
2. solution: cdn, apache, ruby, backend services, db
3. replacement of ruby with java
4. node.js, breaking down monolith
5. cdn, nginx/GROUT, several apps for different routes | API, services

- reasons for node, highly concurrency, frontend and backend, rapid development, npm modules
- stack: coffeescript, express, connect, mustache, own libraries
- frontend composed over 100 node apps

# atlassian
> @RedWolves
  Ralph Whitbeck

- 100 M paid out to developers for plugins, 50'000 customers
- first: open(ish) source where customers could download jira and install on their own server
- version 1: jira, confluence own plugin architecture
- version 2: plugins OSGI plugins
- version 3: atlassian connect, web api's for cloud integration
- open technology stack, RESTful API, useful for node.js plugin development
- insert web content
- webhooks
- add-ons as micro services
- market place vs. add-on descriptor (JSON file)
- <-- API Request
- --> webhooks
- at the end, the user does not see, what comes from atlassian and what is a plugin
- atlassian connect is only available for cloud plugins, not self installed server

plugin development
1. download sdk
2. connect > developing localy
3. develop node app, in html :aui, localhost:port/jira/atlassian-connect/all.js for CORS
4. run jira locally, admin > manage add-ons install ad-on


# hacking the chipson
> @noopkat
  Suz Hinton

- nodebots javascript
- libc, avr-gcc, avrdude
- code->programmer->chip
- replacing avrdude with node.js alternative. avrgirl
- meow.noopkat.com

# tessel
> @selkeymoonbeam
  Kelsey Breseman
  technicalhumans

- from a company to
- a distributed development team with volunteers

# airplay with node
> @wa7son
  Thomas Watson

- airport epress with jack (airtunes RAOP) -> airplay (AirTunes2)
- ServiveDiscovery, Bonjour, Zeroconf, -> Multicast DNS
- ->photos, video, screen mirroring
- encrypted, James got the private RSA Key
- 2011 reverse engineering protocol
RAOP: RTSP:5000, Audio Data:6000, RTP Control:6001 (ish), Timing:6002 (ish)
AirPlay:7000, NTP:7011 (screen mirroring)
- did analyzing via wireshark with a a special capability
- netcat
- watson , protodrop

# alarm system,
> @mhdawson1
  Michael Dawson
  IBM

- node & mqtt (mosquito), for messaging
- 433 Mhz, 2262 protocol

# the internet going forward
> @nexxylove
  Emily Rose

- cyborg
- 2013 51% of internet traffic from non human traffic
- 50'000'000'000 devices by 2020 (estimate by cisco)
- the most successful technology gets out of the way and helps us live our lives (amber case)
- implementations are more valuable than standards

# rust
> @slsoftworks
  Istvan Szmozsanszky
  flaki

- javascript is huge
- node-ffi
- you can program hw in javascript, but at the end, it mitght run on something else like LUA (on tessel)
- node MCU, JerryScript
- why rust, program language is a tool
- RUST, new low level language, compiled language, into machine code, has a complainer
- RUST, for speed, low level consumtion, no garbage collector, reliable
- node-ffi node binding
- check fizbuzz


# node.js at netflix
> ?

- whole website in node.js
- bunyan stream json and analyze json properties
- bunyan extendable with serializers
- node-vasync
- restify, great logs with latency and time spent on function level
- scoped child loggers
- DTrace
- analytics with unix tools, observable REST applications

# nodebots
> @nodebotanist
  Kassandra Perch

- I am a direct product of the comunity I was raised in
- treat everyone like you treat your best friend, and chances are, you are right
- there is absolutely nothing wrong with being nice
- your community is far more important than your code. your code affects people for a moment.
- empathy is a muscle
- codes of conduct aren't just for the people in your community. they're for the people you're missing out on.

# logs / dump
> @lucamaraschi
  Luca Maraschi

- mdb on smart os
- know the underlying system
- prepare for monitoring / getting dumps

# atlassian / TravisTheTechie

# post mortem debugging
> @mhdawson1
  Michael Dawson
> @fierydrake
  Mike Tunniclife
  IBM

- metrics: GC activity, Trhoughput, Response Time
- https://github.com/RuntimeTools/appmetrics
- healthcenter eclipse
- modules: appmetrics, appmetrics-elk, appmetrics-dash, graphite
- require('appmetrics')
- custom metrics: appmetrics.emit('myevent, {time: Date.now(), what: 'ever'});
- drop-in "probes" for monkey patching


# migrating legacy platform to modular node.js
> @moogster31
  Katie Stockton Roberts
  BBC

- BBC knowledge and learning
- time line, cms content etc., bbc food
- food site, 2 million unique users per week, high peaks
- 11'000 recipies
- current solution, PHP, 6 years old
- BBC moving lots to node
- reasons: performance, speedup development, non blocking, ative community, developers like it
- migration, "run alongside", refresh current mobile css, gently
- no more tears approach, bits by bits, small number of moving parts
- improvements: load time, "lego brick" development, reduced development time, same technology in frontend and backend, huge learning curve for non javascript developers

# open technology centers of gravity
> @tmmoore_1
  Todd Moore

- works in foundations, involved in joyent/node transition, working with linux (linus torwalds), apache, eclipse, cloud foundry, etc.
- figuring out how IBM can work with communities
- Centers of Gravity in node.js community
- Developers hold all the powers,
- 3c: code, community, culture
- eco systems: spark, open stack, node.js, cloud foundry, jquery, swagger {...}
- node.js extending the gravity field
- open container initiative, documenting docker stuff
- Spark, SystemML open source looking for contributors
- communities influence each other
- building stuff: well-formed, reusable, modular, extensible
- 78% say they run their business on open source


# dependencies
> @boennemann
  Stephan Bönnemann

- you can be excellent, but not so productive, when you try to do everything yourself
- modules can really help you, become more productive
- for almost everything you wan't to do, there is already solutions you can leverage
- npm 180'000 modules
- community ~50'000 members
- small modules are only nice in theory, dependency __hell__
- __hell__ is a place where you are punished for your own sins
- you have to have proper tests for your modules
- modules are everything when you want to become productive
- treat modules respectfully
- e.g. samber
- modules to help: semantic-release, dont-break, india, diffyproject, next-update

# your own data
> @mattpodwysocki
  Matt Podwysocki
  microsoft

- peer web
- microsoft
- iot, not so interesting in isolation, expecting perfect connectivity, expects certain socio economic level
- democratize the things
- think big, help community, save lives etc...
- node.js can help, modules, pouch db sync,
- security? coin flip protocol, bluetooth like experience, pairing with code
- JXcore, node running on all of devices.
- WiFi Shoplist (node.js) on the itunes, android
- use bluetooth, WiFi to connect, no cloud
- ThaliProject
- possibility, reimplement Tor with javascript
- jx npm install thali
- change the world through software, together

# node & musical performance
> @hughrawlinson
  Hugh Rawlinson

- music hacker
- current state: lots of proprietary stuff
- daw digital audio workstation, synthesizer, record, loop, etc. proprietary
- Max/MSP & Pure, graphical, boxes, connect, changes apply when changing left input, not right input, complex
- Chuck, add shreds, / Superdollider, Tidal
- where does node fit in
- web audio api, local microservices for performers, npm, livecoding in node
- Node Web Audio API,
- module: meyda, Lissajous, Gibber, wat.js
- feature based synthesis
- advantages with node.js modularity, freedom
- power synthesizers

# mad science of node
> @trevnorris
  Trevor Norris

- why? alleviate boredom
- view problems from another perspective
- it even might become useful

- process.hrtime(t)

# contributing to node core
> @Fishrock123
  Jeremiah Senkpiel

- why, does not wan't to be an exclusive club
- is frightening, hedgy on the outside, like a hedgehog, nice in the inside
- 44 Collaborators
- 15 TSC Members
- -> Evangelism, i18n, website, docs, etc.
- starting: Issue/PR Review [good first contribution]
- help make modules smoke-testable
- (ARM) Hardware
- core things
- /doc /lib /src /test CAPITALS.md files
- first making better tests
- /doc/api markdown files

# what is art?
> @mafintosh
  Mathias Buus

__p2p live streaming of dynamic content__
- bittorrent in node.
- bittorrent flow
- merke tree, hash data
- magnet link contains the top hash (of hashes, of data)
- with every added file, you get a new merkle tree
- trust has to be established again
- new protocol: new hash, is a hash of the old hash
- npm install peervision
- npm install -g peervisionary
- -> stream everything

# visulator
> @thlorenz
  Thorsten Lorenz

- why should you learn assembly?
- assembly, high performance code
- using disassembler, you can go back and forth without anything special like 'sourcemaps'
- C&A
- book wiley, assembly language Step by Step,
- CPU:
IR (Instruction Register) -> Control Unit (via Control Signals) -> ALU -> Register Set
- visulator, uses capstone
- use gdb, no ldb

# redhat
> @mofoghlu
  Dr Mícheál Ó Foghlú

- ermergence of bimodal or 2-track IT
- systems of record vs systems of engagement
- mobile is the catalyst - node.js is the tool
- usually node.js on the server side (for mobile apps)
- redhat complete open source company > 1BN revenue / year
- 8k employees, gontinuous growth for over 10 years
- every product is open source
- redhat fully supports node.js bare bone and virtual
- redhat docker image
- containers are basically linux os (redhat as it :-)
- open shift polyglot PaaS
- redhat mobile application platform RHMAP
- solves: private api behind firewall, made public
- node as a proxy, or as microservices / express
- MBAS
- feedhenry , OpenShift 3.0 docker, cuberneties
- upstream requests -> go into enterprise distribution, no addons hidded

# hexagon stickers
> @yosuke_furukawa
  Yosuke Furukawa

- standard for stickers
- https://hexi.pics
- aws lamda invoke lambda functions
- module: okrabyte (OCR)

# hapi
> Peter Elger
  & Wyatt Lyon Preul
  & Matt Harrison
    @mt_harrison

- no middleware
- more like .net like hooks along the request lifecycle
- no regex in routes


## read into / lookup
- npm.im: semantic-release, dont-break, india, diffyproject, next-update
- measuring time: process.hrtime(t)
- mqtt
- aspect api
- fizzbuzz
- bunyan for json
- presentations: slides.com
- require('vasync')
- require('later')
- groupon.github.io
- ngrok local tunnel
- require('picture-tube')
- require('airplay-photos')

