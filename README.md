# api documentation for  [pm2-gui (v0.1.4)](https://github.com/Tjatse/pm2-gui)  [![npm package](https://img.shields.io/npm/v/npmdoc-pm2-gui.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-pm2-gui) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-pm2-gui.svg)](https://travis-ci.org/npmdoc/node-npmdoc-pm2-gui)
#### An elegant web & terminal interface for Unitech/PM2.

[![NPM](https://nodei.co/npm/pm2-gui.png?downloads=true)](https://www.npmjs.com/package/pm2-gui)

[![apidoc](https://npmdoc.github.io/node-npmdoc-pm2-gui/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-pm2-gui_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-pm2-gui/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-pm2-gui/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-pm2-gui/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Tjatse"
    },
    "bin": {
        "pm2-gui": "./pm2-gui"
    },
    "bugs": {
        "url": "https://github.com/Tjatse/pm2-gui/issues"
    },
    "dependencies": {
        "ansi-html": "~0.0.5",
        "async": "~1.5.2",
        "blessed": "^0.1.81",
        "chalk": "~1.1.3",
        "commander": "~2.9.0",
        "express": "~4.13.4",
        "express-session": "~1.13.0",
        "inquirer": "~1.0.2",
        "jade": "~1.11.0",
        "lodash": "~4.12.0",
        "pidusage": "~1.0.1",
        "pm2-axon": "~2.0.11",
        "pm2-axon-rpc": "~0.3.6",
        "socket.io": "~1.4.6",
        "socket.io-client": "~1.4.6",
        "windows-cpu": "~0.1.4"
    },
    "description": "An elegant web & terminal interface for Unitech/PM2.",
    "devDependencies": {
        "standard": "*"
    },
    "directories": {},
    "dist": {
        "shasum": "e4d239249dde02d9f546975a2ee78b134f77d7e6",
        "tarball": "https://registry.npmjs.org/pm2-gui/-/pm2-gui-0.1.4.tgz"
    },
    "engines": [
        "node >= 0.8.0"
    ],
    "gitHead": "b0d670c283d551edccc43c230c8a5554e6e6772d",
    "homepage": "https://github.com/Tjatse/pm2-gui",
    "keywords": [
        "monitor",
        "dashboard",
        "PM2",
        "PM2 interface",
        "PM2 web",
        "PM2 ui",
        "PM2 gui",
        "PM2 dashboard",
        "PM2 monitor"
    ],
    "license": "MIT",
    "main": "./pm2-gui.js",
    "maintainers": [
        {
            "name": "tjatse",
            "email": "thisnamemeansnothing@gmail.com"
        }
    ],
    "name": "pm2-gui",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/Tjatse/pm2-gui.git"
    },
    "scripts": {
        "test": "NODE_ENV=test bash test/index.sh"
    },
    "standard": {
        "ignore": [
            "web/public/"
        ],
        "globals": [
            "action",
            "__route_root"
        ]
    },
    "version": "0.1.4"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module pm2-gui](#apidoc.module.pm2-gui)
1.  [function <span class="apidocSignatureSpan">pm2-gui.</span>dashboard (confFile)](#apidoc.element.pm2-gui.dashboard)
1.  [function <span class="apidocSignatureSpan">pm2-gui.</span>exitGraceful (code, signal)](#apidoc.element.pm2-gui.exitGraceful)
1.  [function <span class="apidocSignatureSpan">pm2-gui.</span>monitor (options)](#apidoc.element.pm2-gui.monitor)
1.  [function <span class="apidocSignatureSpan">pm2-gui.</span>startAgent (confFile)](#apidoc.element.pm2-gui.startAgent)
1.  [function <span class="apidocSignatureSpan">pm2-gui.</span>startWebServer (confFile)](#apidoc.element.pm2-gui.startWebServer)
1.  object <span class="apidocSignatureSpan">pm2-gui.</span>monitor.prototype
1.  object <span class="apidocSignatureSpan">pm2-gui.</span>pm
1.  object <span class="apidocSignatureSpan">pm2-gui.</span>stat

#### [module pm2-gui.monitor](#apidoc.module.pm2-gui.monitor)
1.  [function <span class="apidocSignatureSpan">pm2-gui.</span>monitor (options)](#apidoc.element.pm2-gui.monitor.monitor)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.</span>available (options)](#apidoc.element.pm2-gui.monitor.available)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.</span>parseConnectionString (connectionString)](#apidoc.element.pm2-gui.monitor.parseConnectionString)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.</span>toConnectionString (connection)](#apidoc.element.pm2-gui.monitor.toConnectionString)
1.  object <span class="apidocSignatureSpan">pm2-gui.monitor.</span>ACCEPT_KEYS
1.  object <span class="apidocSignatureSpan">pm2-gui.monitor.</span>PM2_DAEMON_PROPS
1.  string <span class="apidocSignatureSpan">pm2-gui.monitor.</span>DEF_CONF_FILE

#### [module pm2-gui.monitor.prototype](#apidoc.module.pm2-gui.monitor.prototype)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_broadcast (event, data, nsp)](#apidoc.element.pm2-gui.monitor.prototype._broadcast)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_connectLogSock (socket)](#apidoc.element.pm2-gui.monitor.prototype._connectLogSock)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_connectProcSock (socket)](#apidoc.element.pm2-gui.monitor.prototype._connectProcSock)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_connectSysSock (socket)](#apidoc.element.pm2-gui.monitor.prototype._connectSysSock)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_init (options)](#apidoc.element.pm2-gui.monitor.prototype._init)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_killTailProcess (pmId)](#apidoc.element.pm2-gui.monitor.prototype._killTailProcess)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_listeningSocketIO ()](#apidoc.element.pm2-gui.monitor.prototype._listeningSocketIO)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_nextTick (tick, continuously)](#apidoc.element.pm2-gui.monitor.prototype._nextTick)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_observePM2 ()](#apidoc.element.pm2-gui.monitor.prototype._observePM2)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_pm2Ver (socket)](#apidoc.element.pm2-gui.monitor.prototype._pm2Ver)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_refreshProcs ()](#apidoc.element.pm2-gui.monitor.prototype._refreshProcs)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_resolveHome (pm2Home)](#apidoc.element.pm2-gui.monitor.prototype._resolveHome)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_systemStat (cb)](#apidoc.element.pm2-gui.monitor.prototype._systemStat)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_throttleRefresh ()](#apidoc.element.pm2-gui.monitor.prototype._throttleRefresh)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>connect (options, success, failure)](#apidoc.element.pm2-gui.monitor.prototype.connect)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>quit ()](#apidoc.element.pm2-gui.monitor.prototype.quit)
1.  [function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>run ()](#apidoc.element.pm2-gui.monitor.prototype.run)

#### [module pm2-gui.pm](#apidoc.module.pm2-gui.pm)
1.  [function <span class="apidocSignatureSpan">pm2-gui.pm.</span>_actionByPMId (sockPath, proc, action, cb)](#apidoc.element.pm2-gui.pm._actionByPMId)
1.  [function <span class="apidocSignatureSpan">pm2-gui.pm.</span>_findById (sockPath, id, cb)](#apidoc.element.pm2-gui.pm._findById)
1.  [function <span class="apidocSignatureSpan">pm2-gui.pm.</span>_rpc (opts)](#apidoc.element.pm2-gui.pm._rpc)
1.  [function <span class="apidocSignatureSpan">pm2-gui.pm.</span>_tailLogs (proc, cb)](#apidoc.element.pm2-gui.pm._tailLogs)
1.  [function <span class="apidocSignatureSpan">pm2-gui.pm.</span>action (sockPath, action, id, cb)](#apidoc.element.pm2-gui.pm.action)
1.  [function <span class="apidocSignatureSpan">pm2-gui.pm.</span>list (sockPath, cb, context)](#apidoc.element.pm2-gui.pm.list)
1.  [function <span class="apidocSignatureSpan">pm2-gui.pm.</span>sub (sockPath, cb, context)](#apidoc.element.pm2-gui.pm.sub)
1.  [function <span class="apidocSignatureSpan">pm2-gui.pm.</span>tail (opts, each, cb)](#apidoc.element.pm2-gui.pm.tail)
1.  [function <span class="apidocSignatureSpan">pm2-gui.pm.</span>version (sockPath, cb)](#apidoc.element.pm2-gui.pm.version)

#### [module pm2-gui.stat](#apidoc.module.pm2-gui.stat)
1.  [function <span class="apidocSignatureSpan">pm2-gui.stat.</span>cpuInfo ()](#apidoc.element.pm2-gui.stat.cpuInfo)
1.  [function <span class="apidocSignatureSpan">pm2-gui.stat.</span>cpuUsage (fn, context)](#apidoc.element.pm2-gui.stat.cpuUsage)
1.  number <span class="apidocSignatureSpan">pm2-gui.stat.</span>uptime
1.  object <span class="apidocSignatureSpan">pm2-gui.stat.</span>cpus
1.  object <span class="apidocSignatureSpan">pm2-gui.stat.</span>memory
1.  string <span class="apidocSignatureSpan">pm2-gui.stat.</span>arch
1.  string <span class="apidocSignatureSpan">pm2-gui.stat.</span>hostname
1.  string <span class="apidocSignatureSpan">pm2-gui.stat.</span>platform
1.  string <span class="apidocSignatureSpan">pm2-gui.stat.</span>release



# <a name="apidoc.module.pm2-gui"></a>[module pm2-gui](#apidoc.module.pm2-gui)

#### <a name="apidoc.element.pm2-gui.dashboard"></a>[function <span class="apidocSignatureSpan">pm2-gui.</span>dashboard (confFile)](#apidoc.element.pm2-gui.dashboard)
- description and source-code
```javascript
function dashboard(confFile) {
  // restore cursor
  process.on('exit', function () {
    process.stdout.write('\u001b[?25h')
  })
  var monitor = slave({
    confFile: confFile
  })
  var options = _.clone(monitor.options)
  var q = Monitor.available(options)

  if (!q) {
    console.error('No agent is online, can not start it.')
    return process.exit(0)
  }
  var ql = q.choices.length
  if (ql === 1) {
    if (q.choices[0].short !== 'localhost') {
      console.info('There is just one remoting server online, try to connect it.')
    }
    return _connectToDashboard(monitor, options, Monitor.parseConnectionString(q.choices[0].value))
  }
  if (!options.agent || !options.agent.offline) {
    q.choices.splice(ql - 1, 0, new inquirer.Separator())
  }

  console.info('Remoting servers are online, choose one you are intrested in.')
  console.log('')
  inquirer.prompt(q).then(function (answers) {
    console.log('')
    _connectToDashboard(monitor, options, Monitor.parseConnectionString(answers.socket_server))
  })
}
```
- example usage
```shell
...
'''

Programmable:
'''javascript
var pm2GUI = require('pm2-gui');
pm2GUI.startWebServer([ini_config_file]);
pm2GUI.startAgent([ini_config_file]);
pm2GUI.dashboard([ini_config_file]);
'''

<a name="config" />
# Configuration
Edit the 'pm2-gui/pm2-gui.ini' file or copy the [config example](./pm2-gui.ini) to '/etc/pm2-gui.ini' (starting with 'pm2-gui start
 /etc/pm2-gui.ini'):

<a name="ui" />
...
```

#### <a name="apidoc.element.pm2-gui.exitGraceful"></a>[function <span class="apidocSignatureSpan">pm2-gui.</span>exitGraceful (code, signal)](#apidoc.element.pm2-gui.exitGraceful)
- description and source-code
```javascript
function exitGraceful(code, signal) {
  code = code || 0
  if (signal !== '-f') {
    console.debug('Slave has exited, code: ' + code + ', signal: ' + (signal || 'NULL'))
  }
  var fds = 0

  function tryToExit () {
    if ((fds & 1) && (fds & 2)) {
      process.exit(code)
    }
  }

  [process.stdout, process.stderr].forEach(function (std) {
    var fd = std.fd
    if (!std.bufferSize) {
      fds = fds | fd
    } else {
      std.write && std.write('', function () {
        fds = fds | fd
        tryToExit()
      })
    }
  })
  tryToExit()
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pm2-gui.monitor"></a>[function <span class="apidocSignatureSpan">pm2-gui.</span>monitor (options)](#apidoc.element.pm2-gui.monitor)
- description and source-code
```javascript
function Monitor(options) {
  if (!(this instanceof Monitor)) {
    return new Monitor(options)
  }

  // Initialize...
  this._init(options)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pm2-gui.startAgent"></a>[function <span class="apidocSignatureSpan">pm2-gui.</span>startAgent (confFile)](#apidoc.element.pm2-gui.startAgent)
- description and source-code
```javascript
function startAgent(confFile) {
  var monitor = slave({
    confFile: confFile
  })

  var options = monitor.options
  options.agent = options.agent || {}
  if (options.agent.offline) {
    console.error('Agent is offline, can not start it.')
    return process.exit(0)
  }
  options.port = options.port || 8088
  var sockio = socketIO()
  sockio.listen(options.port, {
    origins: options.origins || '*:*'
  })
  monitor.sockio = sockio
  monitor.run()
  console.info('Socket.io server is listening on 0.0.0.0:' + options.port)
}
```
- example usage
```shell
...
$ node pm2-gui.js <cmd> [options]
'''

Programmable:
'''javascript
var pm2GUI = require('pm2-gui');
pm2GUI.startWebServer([ini_config_file]);
pm2GUI.startAgent([ini_config_file]);
pm2GUI.dashboard([ini_config_file]);
'''

<a name="config" />
# Configuration
Edit the 'pm2-gui/pm2-gui.ini' file or copy the [config example](./pm2-gui.ini) to '/etc/pm2-gui.ini' (starting with 'pm2-gui start
 /etc/pm2-gui.ini'):
...
```

#### <a name="apidoc.element.pm2-gui.startWebServer"></a>[function <span class="apidocSignatureSpan">pm2-gui.</span>startWebServer (confFile)](#apidoc.element.pm2-gui.startWebServer)
- description and source-code
```javascript
function startWebServer(confFile) {
  var monitor = slave({
    confFile: confFile
  })
  var options = monitor.options

  options.port = options.port || 8088
  var server = Web({
    middleware: function (req, res, next) {
      req._config = options
      next()
    },
    port: options.port
  })

  monitor.sockio = socketIO(server, {
    origins: options.origins || '*:*'
  })
  monitor.run()
  console.info('Web server is listening on 127.0.0.1:' + options.port)
}
```
- example usage
```shell
...
'''bash
$ node pm2-gui.js <cmd> [options]
'''

Programmable:
'''javascript
var pm2GUI = require('pm2-gui');
pm2GUI.startWebServer([ini_config_file]);
pm2GUI.startAgent([ini_config_file]);
pm2GUI.dashboard([ini_config_file]);
'''

<a name="config" />
# Configuration
Edit the 'pm2-gui/pm2-gui.ini' file or copy the [config example](./pm2-gui.ini) to '/etc/pm2-gui.ini' (starting with 'pm2-gui start
 /etc/pm2-gui.ini'):
...
```



# <a name="apidoc.module.pm2-gui.monitor"></a>[module pm2-gui.monitor](#apidoc.module.pm2-gui.monitor)

#### <a name="apidoc.element.pm2-gui.monitor.monitor"></a>[function <span class="apidocSignatureSpan">pm2-gui.</span>monitor (options)](#apidoc.element.pm2-gui.monitor.monitor)
- description and source-code
```javascript
function Monitor(options) {
  if (!(this instanceof Monitor)) {
    return new Monitor(options)
  }

  // Initialize...
  this._init(options)
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pm2-gui.monitor.available"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.</span>available (options)](#apidoc.element.pm2-gui.monitor.available)
- description and source-code
```javascript
available = function (options) {
  options.agent = options.agent || {}
  var remotable = options.remotes && _.keys(options.remotes).length > 0

  if (options.agent.offline && !remotable) {
    return null
  }

  options.port = options.port || 8088

  var q = {
    name: 'socket_server',
    message: 'Which socket server would you wanna connect to',
    type: 'list',
    choices: []
  }
  var wrapLocal = function () {
    return {
      value: (options.agent && options.agent.authorization ? options.agent.authorization + '@' : '') + '127.0.0.1:' + options.port
,
      short: 'localhost'
    }
  }
  if (!remotable) {
    q.choices = [wrapLocal()]
    return q
  }
  var maxShortLength = 0
  for (var remote in options.remotes) {
    var connectionString = options.remotes[remote]
    q.choices.push({
      value: connectionString,
      short: remote
    })
    maxShortLength = Math.max(maxShortLength, remote.length)
  }
  if (!options.agent.offline) {
    var conn = wrapLocal()
    q.choices.push(conn)
    maxShortLength = Math.max(maxShortLength, conn.short.length)
  }

  if (q.choices.length > 1) {
    q.choices.forEach(function (c) {
      c.name = '[' + c.short + Array(maxShortLength - c.short.length + 1).join(options.blank || ' ') + '] '
    })
  }

  return q
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pm2-gui.monitor.parseConnectionString"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.</span>parseConnectionString (connectionString)](#apidoc.element.pm2-gui.monitor.parseConnectionString)
- description and source-code
```javascript
parseConnectionString = function (connectionString) {
  var connection = {
    port: 8088,
    hostname: '127.0.0.1',
    authorization: ''
  }
  var lastAt = connectionString.lastIndexOf('@')
  if (lastAt >= 0) {
    connection.authorization = connectionString.slice(0, lastAt)
    connectionString = connectionString.slice(lastAt + 1)
  }
  if (!/^https?:\/\//i.test(connectionString)) {
    connectionString = 'http://' + connectionString
  }

  if (connectionString) {
    connectionString = url.parse(connectionString)
    connection.hostname = connectionString.hostname
    connection.port = connectionString.port
    connection.path = (connectionString.path || '').replace(/^\/+/, '')
    connection.protocol = connectionString.protocol
  }
  return connection
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pm2-gui.monitor.toConnectionString"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.</span>toConnectionString (connection)](#apidoc.element.pm2-gui.monitor.toConnectionString)
- description and source-code
```javascript
toConnectionString = function (connection) {
  var uri = (connection.protocol || 'http:') + '//' + (connection.hostname || '127.0.0.1') + ':' + connection.port +
    (connection.path || '') + (connection.namespace || '')

  if (connection.authorization) {
    uri += (uri.indexOf('?') > 0 ? '&' : '?') + 'auth=' + connection.authorization
  }
  return uri
}
```
- example usage
```shell
...
 * @param  {Function} success
 * @param  {Function} failure
 */
Monitor.prototype.connect = function (options, success, failure) {
if (!options.port) {
  throw new Error('Port is required!')
}
var serverUri = Monitor.toConnectionString(options)

success = _.once(success)
failure = _.once(failure)

console.info('Connecting to', serverUri)
var socket = socketIOClient(serverUri)
socket.on('connect', function () {
...
```



# <a name="apidoc.module.pm2-gui.monitor.prototype"></a>[module pm2-gui.monitor.prototype](#apidoc.module.pm2-gui.monitor.prototype)

#### <a name="apidoc.element.pm2-gui.monitor.prototype._broadcast"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_broadcast (event, data, nsp)](#apidoc.element.pm2-gui.monitor.prototype._broadcast)
- description and source-code
```javascript
_broadcast = function (event, data, nsp) {
  nsp = nsp || conf.NSP.SYS

  if (this._noClient) {
    return console.debug('No client is connecting, ignore broadcasting', event, 'to', nsp)
  }
  console.debug('Broadcasting', event, 'to', nsp)
  this._sockio.of(nsp).emit(event, data)
}
```
- example usage
```shell
...
    console.debug(prefix, action, 'completed!')
    forceRefresh && self._throttleRefresh()
  })
})
sendProcs()
socket.on('procs', sendProcs)
self._pm2Ver(socket)
this._sysStat && this._broadcast('system_stat', this._sysStat)

// Grep system states once and again.
if (this._status !== 'R') {
  this._nextTick(this.options.refresh || 5000)
}

function sendProcs () {
...
```

#### <a name="apidoc.element.pm2-gui.monitor.prototype._connectLogSock"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_connectLogSock (socket)](#apidoc.element.pm2-gui.monitor.prototype._connectLogSock)
- description and source-code
```javascript
_connectLogSock = function (socket) {
  var self = this

  // Emit error.
  function emitError (err, pmId, keepANSI) {
    var data = {
      pm_id: pmId,
      msg: keepANSI ? chalk.red(err.message) : '<span style="color: #ff0000">Error: ' + err.message + '</span>'
    }
    self._broadcast.call(self, 'log', data, conf.NSP.LOG) // eslint-disable-line no-useless-call
  }

  function startTailProcess (pmId, keepANSI) {
    socket._pm_id = pmId

    if (self._tails[pmId]) {
      return
    }

    // Tail logs.
    pm.tail({
      sockPath: self.options.pm2Conf.DAEMON_RPC_PORT,
      logPath: self.options.pm2Conf.PM2_LOG_FILE_PATH,
      pm_id: pmId
    }, function (err, lines) {
      if (err) {
        return emitError(err, pmId, keepANSI)
      }
      // Emit logs to clients.
      var data = {
        pm_id: pmId,
        msg: lines.map(function (line) {
          if (!keepANSI) {
            line = line.replace(/\s/, '&nbsp;')
            return '<span>' + ansiHTML(line) + '</span>'
          } else {
            return line
          }
        }).join(keepANSI ? '\n' : '')
      }
      self._broadcast.call(self, 'log', data, conf.NSP.LOG) // eslint-disable-line no-useless-call
    }, function (err, tail) {
      if (err) {
        return emitError(err, pmId, keepANSI)
      }
      if (!tail) {
        return emitError(new Error('No log can be found.'), pmId, keepANSI)
      }

      console.info('[pm2:' + pmId + ']', 'tail starting...')
      self._tails[pmId] = tail
    })
  }

  socket.on('disconnect', self._killTailProcess.bind(self))
  socket.on('tail_kill', self._killTailProcess.bind(self))
  socket.on('tail', startTailProcess)
  console.info('Connected to ' + socket.nsp.name + '!')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pm2-gui.monitor.prototype._connectProcSock"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_connectProcSock (socket)](#apidoc.element.pm2-gui.monitor.prototype._connectProcSock)
- description and source-code
```javascript
_connectProcSock = function (socket) {
  var self = this
  // Emit error.
  function emitError (err, pid) {
    var data = {
      pid: pid,
      msg: '<span style="color: #ff0000">Error: ' + err.message + '</span>'
    }
    self._broadcast.call(self, 'proc', data, conf.NSP.PROC) // eslint-disable-line no-useless-call
  }

  function killObserver () {
    var socks = self._sockio.of(conf.NSP.PROC).sockets
    var canNotBeDeleted = {}

    if (Array.isArray(socks) && socks.length > 0) {
      socks.forEach(function (sock) {
        if (sock._pid) {
          canNotBeDeleted[sock._pid.toString()] = 1
        }
      })
    }

    for (var pid in self._usages) {
      var timer
      if (!canNotBeDeleted[pid] && (timer = self._usages[pid])) {
        clearInterval(timer)
        delete self._usages[pid]
        console.debug('[pid:' + pid + ']', 'cpu and memory observer destroyed!')
      }
    }
  }

  function runObserver (pid) {
    socket._pid = pid

    var pidStr = pid.toString()
    if (self._usages[pidStr]) {
      return
    }

    console.debug('[pid:' + pidStr + ']', 'cpu and memory observer is running...')

    function runTimer () {
      pidusage.stat(pid, function (err, stat) {
        if (err) {
          clearInterval(self._usages[pidStr])
          delete self._usages[pidStr]
          return emitError.call(self, err, pid)
        }
        stat.memory = stat.memory * 100 / totalmem

        var data = {
          pid: pid,
          time: Date.now(),
          usage: stat
        }
        self._broadcast.call(self, 'proc', data, conf.NSP.PROC) // eslint-disable-line no-useless-call
      })
    }

    self._usages[pidStr] = setInterval(runTimer, 3000)
    runTimer(this)
  }

  socket.on('disconnect', killObserver)
  socket.on('proc', runObserver)
  console.info('Connected to ' + socket.nsp.name + '!')
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pm2-gui.monitor.prototype._connectSysSock"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_connectSysSock (socket)](#apidoc.element.pm2-gui.monitor.prototype._connectSysSock)
- description and source-code
```javascript
_connectSysSock = function (socket) {
  var self = this
  // Still has one client connects to server at least.
  self._noClient = false

  socket.on('disconnect', function () {
    // Check connecting client.
    self._noClient = self._sockio.of(conf.NSP.SYS).sockets.length === 0
  })

  // Trigger actions of process.
  socket.on('action', function (action, id) {
    var prefix = '[pm2:' + id + ']'
    console.debug(prefix, action, 'sending to pm2 daemon...')
    if (self.options.readonly) {
      console.warn(prefix, 'denied, readonly!')
      return socket.emit('action', id, 'Can not complete the action due to denied by server, it is readonly!')
    }
    pm.action(self.options.pm2Conf.DAEMON_RPC_PORT, action, id, function (err, forceRefresh) {
      if (err) {
        console.error(action, err.message)
        return socket.emit('action', id, 'Can not complete the action due to ' + err.message)
      }
      console.debug(prefix, action, 'completed!')
      forceRefresh && self._throttleRefresh()
    })
  })
  sendProcs()
  socket.on('procs', sendProcs)
  self._pm2Ver(socket)
  this._sysStat && this._broadcast('system_stat', this._sysStat)

  // Grep system states once and again.
  if (this._status !== 'R') {
    this._nextTick(this.options.refresh || 5000)
  }

  function sendProcs () {
    self._procs && socket.emit(typeof self._procs === 'string' ? 'info' : 'procs', self._procs)
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pm2-gui.monitor.prototype._init"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_init (options)](#apidoc.element.pm2-gui.monitor.prototype._init)
- description and source-code
```javascript
_init = function (options) {
  options = options || {}

  defConf = conf.File(options.confFile || path.resolve(__dirname, '..', Monitor.DEF_CONF_FILE)).loadSync().valueOf()
  defConf = _.pick.call(null, defConf, Monitor.ACCEPT_KEYS)

  options = _.pick.apply(options, Monitor.ACCEPT_KEYS).valueOf()
  options = _.defaults(options, defConf)

  options.pm2 = this._resolveHome(options.pm2)
  Log(options.log)

  // Load PM2 config.
  var pm2ConfPath = path.join(options.pm2, 'conf.js')
  var fbMsg = ''
  try {
    options.pm2Conf = require(pm2ConfPath)(options.pm2)
    if (!options.pm2Conf) {
      throw new Error(404)
    }
  } catch (err) {
    fbMsg = 'Can not load PM2 config, the file "' + pm2ConfPath + '" does not exist or empty, fallback to auto-load by pm2 home. '
    console.warn(fbMsg)
    options.pm2Conf = {
      DAEMON_RPC_PORT: path.resolve(options.pm2, 'rpc.sock'),
      DAEMON_PUB_PORT: path.resolve(options.pm2, 'pub.sock'),
      PM2_LOG_FILE_PATH: path.resolve(options.pm2, 'pm2.log')
    }
  }

  Monitor.PM2_DAEMON_PROPS.forEach(function (prop) {
    var val = options.pm2Conf[prop]
    if (!val || !fs.existsSync(val)) {
      throw new Error(fbMsg + 'Unfortunately ' + (val || prop) + ' can not found, please makesure that your pm2 is running and the
 home path is correct.')
    }
  })

  // Bind socket.io server to context.
  if (options.sockio) {
    this.sockio = options.sockio
    delete options.sockio
  }

  // Bind to context.
  this.options = options
  Object.freeze(this.options)
}
```
- example usage
```shell
...
 */
function Monitor (options) {
  if (!(this instanceof Monitor)) {
    return new Monitor(options)
  }

  // Initialize...
  this._init(options)
}

Monitor.ACCEPT_KEYS = ['pm2', 'refresh', 'daemonize', 'readonly', 'max_restarts', 'port', 'log', 'agent', 'remotes', 'origins']
Monitor.DEF_CONF_FILE = 'pm2-gui.ini'
Monitor.PM2_DAEMON_PROPS = ['DAEMON_RPC_PORT', 'DAEMON_PUB_PORT']

/**
...
```

#### <a name="apidoc.element.pm2-gui.monitor.prototype._killTailProcess"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_killTailProcess (pmId)](#apidoc.element.pm2-gui.monitor.prototype._killTailProcess)
- description and source-code
```javascript
_killTailProcess = function (pmId) {
  var self = this

  function killTail (id) {
    var tail = self._tails[id]
    if (!tail) {
      return
    }
    try {
      tail.kill('SIGTERM')
    } catch (err) {}

    delete self._tails[id]
    console.info('[pm2:' + id + ']', 'tail destroyed!')
  }
  if (!isNaN(pmId)) {
    return killTail(pmId)
  }

  var socks = self._sockio.of(conf.NSP.LOG).sockets
  var canNotBeDeleted = {}
  if (socks && socks.length > 0) {
    socks.forEach(function (sock) {
      canNotBeDeleted[sock._pm_id] = 1
    })
  }

  for (var _id in self._tails) {
    if (!canNotBeDeleted[_id]) {
      killTail(_id)
    }
  }
}
```
- example usage
```shell
...
   this.pm2Sock.close()
 }
 if (this._sockio) {
   console.debug('Closing socket.io server.')
   this._sockio.close()

   console.debug('Destroying tails.')
   this._killTailProcess()
 }
}

/**
* Connect to socket.io server.
* @param  {String} ns the namespace.
* @param  {Function} success
...
```

#### <a name="apidoc.element.pm2-gui.monitor.prototype._listeningSocketIO"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_listeningSocketIO ()](#apidoc.element.pm2-gui.monitor.prototype._listeningSocketIO)
- description and source-code
```javascript
_listeningSocketIO = function () {
  if (!this._sockio || this._sockio._listening) {
    console.warn('Avoid duplicated listening!')
    return
  }

  this._sockio._listening = true
  for (var nsp in conf.NSP) {
    this._sockio.of(conf.NSP[nsp]).on('connection', this['_connect' + (nsp[0] + nsp.toLowerCase().slice(1)) + 'Sock'].bind(this))
    console.info('Listening connection event on', nsp.toLowerCase())
  }

  var auth
  if (!(this.options.agent && (auth = this.options.agent.authorization))) {
    return
  }
  this._sockio.use(function (socket, next) {
    if (auth !== socket.handshake.query.auth) {
      return next(new Error('unauthorized'))
    }
    next()
  })
}
```
- example usage
```shell
...

  this._tails = {}
  this._usages = {}

  // Observe PM2
  this._observePM2()

  this._listeningSocketIO()
}

/**
 * Quit monitor.
 * @return {[type]} [description]
 */
Monitor.prototype.quit = function () {
...
```

#### <a name="apidoc.element.pm2-gui.monitor.prototype._nextTick"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_nextTick (tick, continuously)](#apidoc.element.pm2-gui.monitor.prototype._nextTick)
- description and source-code
```javascript
_nextTick = function (tick, continuously) {
  // Return it if worker is running.
  if (this._status === 'R' && !continuously) {
    return
  }
  // Running
  this._status = 'R'
  console.debug('monitor heartbeat per', tick + 'ms')
  // Grep system state
  this._systemStat(function () {
    // If there still has any client, grep again after 'tick' ms.
    if (!this._noClient) {
      return setTimeout(this._nextTick.bind(this, tick, true), tick)
    }
    // Stop
    delete this._status
    console.debug('monitor heartbeat destroyed!')
  })
}
```
- example usage
```shell
...
  sendProcs()
  socket.on('procs', sendProcs)
  self._pm2Ver(socket)
  this._sysStat && this._broadcast('system_stat', this._sysStat)

  // Grep system states once and again.
  if (this._status !== 'R') {
    this._nextTick(this.options.refresh || 5000)
  }

  function sendProcs () {
    self._procs && socket.emit(typeof self._procs === 'string' ? 'info' : 'procs', self._procs)
  }
}
...
```

#### <a name="apidoc.element.pm2-gui.monitor.prototype._observePM2"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_observePM2 ()](#apidoc.element.pm2-gui.monitor.prototype._observePM2)
- description and source-code
```javascript
_observePM2 = function () {
  var pm2Daemon = this.options.pm2Conf.DAEMON_PUB_PORT
  console.info('Connecting to pm2 daemon:', pm2Daemon)
  this.pm2Sock = pm.sub(pm2Daemon, function (data) {
    console.info(chalk.magenta(data.event), data.process.name + '-' + data.process.pm_id)
    this._throttleRefresh()
  }, this)

  // Enforce a refresh operation if RPC is not online.
  this._throttleRefresh()
}
```
- example usage
```shell
...
Monitor.prototype.run = function () {
 this._noClient = true

 this._tails = {}
 this._usages = {}

 // Observe PM2
 this._observePM2()

 this._listeningSocketIO()
}

/**
* Quit monitor.
* @return {[type]} [description]
...
```

#### <a name="apidoc.element.pm2-gui.monitor.prototype._pm2Ver"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_pm2Ver (socket)](#apidoc.element.pm2-gui.monitor.prototype._pm2Ver)
- description and source-code
```javascript
_pm2Ver = function (socket) {
  var pm2RPC = this.options.pm2Conf.DAEMON_RPC_PORT
  console.info('Fetching pm2 version:', pm2RPC)
  pm.version(pm2RPC, function (err, version) {
    socket.emit('pm2_ver', (err || !version) ? '0.0.0' : version)
  })
}
```
- example usage
```shell
...
    }
    console.debug(prefix, action, 'completed!')
    forceRefresh && self._throttleRefresh()
  })
})
sendProcs()
socket.on('procs', sendProcs)
self._pm2Ver(socket)
this._sysStat && this._broadcast('system_stat', this._sysStat)

// Grep system states once and again.
if (this._status !== 'R') {
  this._nextTick(this.options.refresh || 5000)
}
...
```

#### <a name="apidoc.element.pm2-gui.monitor.prototype._refreshProcs"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_refreshProcs ()](#apidoc.element.pm2-gui.monitor.prototype._refreshProcs)
- description and source-code
```javascript
_refreshProcs = function () {
  pm.list(this.options.pm2Conf.DAEMON_RPC_PORT, function (err, procs) {
    if (err) {
      return this._broadcast('info', 'Can not connect to pm2 daemon, ' + err.message)
    }
    // Wrap processes and cache them.
    this._procs = procs.map(function (proc) {
      proc.pm2_env = proc.pm2_env || {
        USER: 'UNKNOWN'
      }
      var pm2Env = {
        user: proc.pm2_env.USER
      }

      for (var key in proc.pm2_env) {
        // Ignore useless fields.
        if (key.slice(0, 1) === '_' ||
          key.indexOf('axm_') === 0 || !!~['versioning', 'command'].indexOf(key) ||
          key.charCodeAt(0) <= 90) {
          continue
        }
        pm2Env[key] = proc.pm2_env[key]
      }
      proc.pm2_env = pm2Env
      return proc
    })
    // Emit to client.
    this._broadcast('procs', this._procs)
  }, this)
}
```
- example usage
```shell
...
*/
Monitor.prototype._throttleRefresh = function () {
 if (this._throttle) {
   clearTimeout(this._throttle)
 }
 this._throttle = setTimeout(function (ctx) {
   ctx._throttle = null
   ctx._refreshProcs()
 }, 500, this)
}

/**
* Refresh processes
* @private
*/
...
```

#### <a name="apidoc.element.pm2-gui.monitor.prototype._resolveHome"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_resolveHome (pm2Home)](#apidoc.element.pm2-gui.monitor.prototype._resolveHome)
- description and source-code
```javascript
_resolveHome = function (pm2Home) {
  if (pm2Home && pm2Home.indexOf('~/') === 0) {
    // Get root directory of PM2.
    pm2Home = process.env.PM2_HOME || path.resolve(process.env.HOME || process.env.HOMEPATH, pm2Home.substr(2))

    // Make sure exist.
    if (!pm2Home || !fs.existsSync(pm2Home)) {
      throw new Error('PM2 root can not be located, try to initialize PM2 by executing 'pm2 ls' or set environment variable vi '
export PM2_HOME=[ROOT]'.')
    }
  }
  return pm2Home
}
```
- example usage
```shell
...

defConf = conf.File(options.confFile || path.resolve(__dirname, '..', Monitor.DEF_CONF_FILE)).loadSync().valueOf()
defConf = _.pick.call(null, defConf, Monitor.ACCEPT_KEYS)

options = _.pick.apply(options, Monitor.ACCEPT_KEYS).valueOf()
options = _.defaults(options, defConf)

options.pm2 = this._resolveHome(options.pm2)
Log(options.log)

// Load PM2 config.
var pm2ConfPath = path.join(options.pm2, 'conf.js')
var fbMsg = ''
try {
  options.pm2Conf = require(pm2ConfPath)(options.pm2)
...
```

#### <a name="apidoc.element.pm2-gui.monitor.prototype._systemStat"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_systemStat (cb)](#apidoc.element.pm2-gui.monitor.prototype._systemStat)
- description and source-code
```javascript
_systemStat = function (cb) {
  stat.cpuUsage(function (err, cpuUsage) {
    if (err) {
      // Log only.
      console.error('Can not load system/cpu/memory information: ', err.message)
    } else {
      // System states.
      this._sysStat = _.defaults(_(stat).pick('cpus', 'arch', 'hostname', 'platform', 'release', 'uptime', 'memory').clone(), {
        cpu: cpuUsage
      })
      this._broadcast.call(this, 'system_stat', this._sysStat) // eslint-disable-line no-useless-call
    }
    cb.call(this)
  }, this)
}
```
- example usage
```shell
...
if (this._status === 'R' && !continuously) {
  return
}
// Running
this._status = 'R'
console.debug('monitor heartbeat per', tick + 'ms')
// Grep system state
this._systemStat(function () {
  // If there still has any client, grep again after 'tick' ms.
  if (!this._noClient) {
    return setTimeout(this._nextTick.bind(this, tick, true), tick)
  }
  // Stop
  delete this._status
  console.debug('monitor heartbeat destroyed!')
...
```

#### <a name="apidoc.element.pm2-gui.monitor.prototype._throttleRefresh"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>_throttleRefresh ()](#apidoc.element.pm2-gui.monitor.prototype._throttleRefresh)
- description and source-code
```javascript
_throttleRefresh = function () {
  if (this._throttle) {
    clearTimeout(this._throttle)
  }
  this._throttle = setTimeout(function (ctx) {
    ctx._throttle = null
    ctx._refreshProcs()
  }, 500, this)
}
```
- example usage
```shell
...
  }
  pm.action(self.options.pm2Conf.DAEMON_RPC_PORT, action, id, function (err, forceRefresh) {
    if (err) {
      console.error(action, err.message)
      return socket.emit('action', id, 'Can not complete the action due to ' + err.message)
    }
    console.debug(prefix, action, 'completed!')
    forceRefresh && self._throttleRefresh()
  })
})
sendProcs()
socket.on('procs', sendProcs)
self._pm2Ver(socket)
this._sysStat && this._broadcast('system_stat', this._sysStat)
...
```

#### <a name="apidoc.element.pm2-gui.monitor.prototype.connect"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>connect (options, success, failure)](#apidoc.element.pm2-gui.monitor.prototype.connect)
- description and source-code
```javascript
connect = function (options, success, failure) {
  if (!options.port) {
    throw new Error('Port is required!')
  }
  var serverUri = Monitor.toConnectionString(options)

  success = _.once(success)
  failure = _.once(failure)

  console.info('Connecting to', serverUri)
  var socket = socketIOClient(serverUri)
  socket.on('connect', function () {
    success(socket)
  })

  socket.on('error', function (err) {
    !failure(err, socket)
  })

  socket.on('connect_error', function (err) {
    !failure(err, socket)
  })
}
```
- example usage
```shell
...

 // Process events.
 sub.on('process:*', function (e, d) {
   if (d && !!~allowedEvents.indexOf(d.event)) {
     cb.call(context, d)
   }
 })
 sub.connect(sockPath)
 return sub
}

/**
* Get PM2 version.
* @param {String} sockPath
* @param {Function} cb
...
```

#### <a name="apidoc.element.pm2-gui.monitor.prototype.quit"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>quit ()](#apidoc.element.pm2-gui.monitor.prototype.quit)
- description and source-code
```javascript
quit = function () {
  if (this.pm2Sock) {
    console.debug('Closing pm2 pub emitter socket.')
    this.pm2Sock.close()
  }
  if (this._sockio) {
    console.debug('Closing socket.io server.')
    this._sockio.close()

    console.debug('Destroying tails.')
    this._killTailProcess()
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.pm2-gui.monitor.prototype.run"></a>[function <span class="apidocSignatureSpan">pm2-gui.monitor.prototype.</span>run ()](#apidoc.element.pm2-gui.monitor.prototype.run)
- description and source-code
```javascript
run = function () {
  this._noClient = true

  this._tails = {}
  this._usages = {}

  // Observe PM2
  this._observePM2()

  this._listeningSocketIO()
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.pm2-gui.pm"></a>[module pm2-gui.pm](#apidoc.module.pm2-gui.pm)

#### <a name="apidoc.element.pm2-gui.pm._actionByPMId"></a>[function <span class="apidocSignatureSpan">pm2-gui.pm.</span>_actionByPMId (sockPath, proc, action, cb)](#apidoc.element.pm2-gui.pm._actionByPMId)
- description and source-code
```javascript
_actionByPMId = function (sockPath, proc, action, cb) {
  var noBusEvent = action === 'delete' && proc.pm2_env.status !== 'online'
  var pmId = proc.pm_id

  action += 'ProcessId'
  var watchEvent = ['stopWatch', action, {
    id: pmId
  }, function () {}]

  if (!!~['restart'].indexOf(action)) { // eslint-disable-line no-extra-boolean-cast
    watchEvent.splice(0, 1, 'restartWatch')
    watchEvent.pop()
  }

  var actionEvent = [action, pmId, function (err, sock) {
    cb(err, noBusEvent)
  }]

  if (action === 'restartProcessId') {
    actionEvent.splice(1, 1, {
      id: pmId
    })
  }

  pm._rpc({
    sockPath: sockPath,
    events: [
      watchEvent,
      actionEvent
    ]
  })
}
```
- example usage
```shell
...
      return cb(err)
    }
    if (!procs || procs.length === 0) {
      return cb(new Error('No PM2 process running, the sockPath is "' + sockPath + '", please make sure it is existing!'))
    }

    async.map(procs, function (proc, next) {
      pm._actionByPMId(sockPath, proc, action, next.bind(null, null))
    }, cb)
  })
} else {
  pm._findById(sockPath, id, function (err, proc) {
    if (err) {
      return cb(err)
    }
...
```

#### <a name="apidoc.element.pm2-gui.pm._findById"></a>[function <span class="apidocSignatureSpan">pm2-gui.pm.</span>_findById (sockPath, id, cb)](#apidoc.element.pm2-gui.pm._findById)
- description and source-code
```javascript
_findById = function (sockPath, id, cb) {
  pm.list(sockPath, function (err, procs) {
    if (err) {
      return cb(err)
    }
    if (!procs || procs.length === 0) {
      return cb(new Error('No PM2 process running, the sockPath is "' + sockPath + '", please make sure it is existing!'))
    }

    var proc = _.find(procs, function (p) {
      return p && p.pm_id === id
    })

    if (!proc) {
      return cb(new Error('Cannot find pm process by pm_id: ' + id))
    }

    cb(null, proc)
  }, true)
}
```
- example usage
```shell
...
      }

      async.map(procs, function (proc, next) {
        pm._actionByPMId(sockPath, proc, action, next.bind(null, null))
      }, cb)
    })
  } else {
    pm._findById(sockPath, id, function (err, proc) {
      if (err) {
        return cb(err)
      }
      pm._actionByPMId(sockPath, proc, action, cb)
    })
  }
}
...
```

#### <a name="apidoc.element.pm2-gui.pm._rpc"></a>[function <span class="apidocSignatureSpan">pm2-gui.pm.</span>_rpc (opts)](#apidoc.element.pm2-gui.pm._rpc)
- description and source-code
```javascript
_rpc = function (opts) {
  var req = axon.socket('req')
  var rpcSock = req.connect(opts.sockPath)
  var rpcClient = new rpc.Client(req)

  // Connect RPC server.
  rpcSock.on('connect', function () {
    // Execute request.
    var waterfalls = opts.events.map(function (event) {
      return function (next) {
        var cb = typeof event[event.length - 1] === 'function' ? event.pop() : null
        if (cb) {
          event.push(function () {
            // Wrap arguments, no [].slice (avoid leak)!!!
            var args = new Array(arguments.length)
            for (var i = 0; i < args; i++) {
              args[i] = arguments[i]
            }
            cb.apply(opts.context, arguments)
            next()
          })
        }
        rpcClient.call.apply(rpcClient, event)
        if (!cb) {
          next()
        }
      }
    })
    async.waterfall(waterfalls, function () {
      rpcSock.close()
    })
  })
}
```
- example usage
```shell
...

/**
 * Get PM2 version.
 * @param {String} sockPath
 * @param {Function} cb
 */
pm.version = function (sockPath, cb) {
  pm._rpc({
    sockPath: sockPath,
    events: [
      ['getVersion', {}, cb]
    ]
  })
}
...
```

#### <a name="apidoc.element.pm2-gui.pm._tailLogs"></a>[function <span class="apidocSignatureSpan">pm2-gui.pm.</span>_tailLogs (proc, cb)](#apidoc.element.pm2-gui.pm._tailLogs)
- description and source-code
```javascript
_tailLogs = function (proc, cb) {
  var logs = {
    'pm2': proc.pm2_log
  }
  if (proc.pm_log_path) {
    logs.entire = proc.pm2_env.pm_log_path
  } else {
    if (proc.pm2_env.pm_out_log_path) {
      logs.out = proc.pm2_env.pm_out_log_path
    }
    if (proc.pm2_env.pm_err_log_path) {
      logs.err = proc.pm2_env.pm_err_log_path
    }
  }

  var logFiles = []
  for (var key in logs) {
    var file = logs[key]
    if (fs.existsSync(file)) {
      logFiles.push(file)
    }
  }
  if (logFiles.length === 0) {
    return null
  }
  var tail = spawn('tail', ['-n', 20, '-f'].concat(logFiles), {
    killSignal: 'SIGTERM',
    detached: true,
    stdio: ['ignore', 'pipe', 'pipe']
  })

  // Use utf8 encoding.
  tail.stdio.forEach(function (stdio) {
    stdio && stdio.setEncoding('utf8')
  })

  // stdout.
  tail.stdout.on('data', function (data) {
    var lines = []
    data.split(/\n/).forEach(function (line) {
      if (!re_blank.test(line)) {
        lines.push(line)
      }
    })
    if (lines.length > 0) {
      cb(null, lines)
    }
  })

  // handle error.
  tail.stderr.on('data', function (data) {
    console.error(data.toString())
    tail.disconnect()
    cb(new Error(data.toString().replace(/\n/, '')))
  })
  tail.unref()
  return tail
}
```
- example usage
```shell
...
 // Fetch the proccess that we need.
 pm._findById(opts.sockPath, opts.pm_id, function (err, proc) {
   if (err) {
     return cb(err)
   }
   proc.pm2_log = opts.logPath
   // Tail logs.
   cb(null, pm._tailLogs(proc, each))
 })
}
/**
* Use linux 'tail' command to grep logs.
* @param {Object} proc
* @param {Function} cb
* @returns {*}
...
```

#### <a name="apidoc.element.pm2-gui.pm.action"></a>[function <span class="apidocSignatureSpan">pm2-gui.pm.</span>action (sockPath, action, id, cb)](#apidoc.element.pm2-gui.pm.action)
- description and source-code
```javascript
action = function (sockPath, action, id, cb) {
  if (id === 'all') {
    pm.list(sockPath, function (err, procs) {
      if (err) {
        return cb(err)
      }
      if (!procs || procs.length === 0) {
        return cb(new Error('No PM2 process running, the sockPath is "' + sockPath + '", please make sure it is existing!'))
      }

      async.map(procs, function (proc, next) {
        pm._actionByPMId(sockPath, proc, action, next.bind(null, null))
      }, cb)
    })
  } else {
    pm._findById(sockPath, id, function (err, proc) {
      if (err) {
        return cb(err)
      }
      pm._actionByPMId(sockPath, proc, action, cb)
    })
  }
}
```
- example usage
```shell
...
  socket.on('action', function (action, id) {
var prefix = '[pm2:' + id + ']'
console.debug(prefix, action, 'sending to pm2 daemon...')
if (self.options.readonly) {
  console.warn(prefix, 'denied, readonly!')
  return socket.emit('action', id, 'Can not complete the action due to denied by server, it is readonly!')
}
pm.action(self.options.pm2Conf.DAEMON_RPC_PORT, action, id, function (err, forceRefresh) {
  if (err) {
    console.error(action, err.message)
    return socket.emit('action', id, 'Can not complete the action due to ' + err.message)
  }
  console.debug(prefix, action, 'completed!')
  forceRefresh && self._throttleRefresh()
})
...
```

#### <a name="apidoc.element.pm2-gui.pm.list"></a>[function <span class="apidocSignatureSpan">pm2-gui.pm.</span>list (sockPath, cb, context)](#apidoc.element.pm2-gui.pm.list)
- description and source-code
```javascript
list = function (sockPath, cb, context) {
  if (!fs.existsSync(sockPath)) {
    return cb.call(context, [])
  }
  pm._rpc({
    sockPath: sockPath,
    events: [
      ['getMonitorData', {}, cb]
    ],
    context: context || this
  })
}
```
- example usage
```shell
...
}

/**
 * Refresh processes
 * @private
 */
Monitor.prototype._refreshProcs = function () {
pm.list(this.options.pm2Conf.DAEMON_RPC_PORT, function (err, procs) {
  if (err) {
    return this._broadcast('info', 'Can not connect to pm2 daemon, ' + err.message)
  }
  // Wrap processes and cache them.
  this._procs = procs.map(function (proc) {
    proc.pm2_env = proc.pm2_env || {
      USER: 'UNKNOWN'
...
```

#### <a name="apidoc.element.pm2-gui.pm.sub"></a>[function <span class="apidocSignatureSpan">pm2-gui.pm.</span>sub (sockPath, cb, context)](#apidoc.element.pm2-gui.pm.sub)
- description and source-code
```javascript
sub = function (sockPath, cb, context) {
  var sub = axon.socket('sub-emitter')
  // Once awake from sleeping.
  sub.on('log:*', function (e, d) {
    // Do not subscribe it.
    sub.off('log:*')
    d.event = 'awake'
    cb.call(context, d)
  })

  // Process events.
  sub.on('process:*', function (e, d) {
    if (d && !!~allowedEvents.indexOf(d.event)) {
      cb.call(context, d)
    }
  })
  sub.connect(sockPath)
  return sub
}
```
- example usage
```shell
...
/**
 * Observe PM2
 * @private
 */
Monitor.prototype._observePM2 = function () {
  var pm2Daemon = this.options.pm2Conf.DAEMON_PUB_PORT
  console.info('Connecting to pm2 daemon:', pm2Daemon)
  this.pm2Sock = pm.sub(pm2Daemon, function (data) {
    console.info(chalk.magenta(data.event), data.process.name + '-' + data.process.pm_id)
    this._throttleRefresh()
  }, this)

  // Enforce a refresh operation if RPC is not online.
  this._throttleRefresh()
}
...
```

#### <a name="apidoc.element.pm2-gui.pm.tail"></a>[function <span class="apidocSignatureSpan">pm2-gui.pm.</span>tail (opts, each, cb)](#apidoc.element.pm2-gui.pm.tail)
- description and source-code
```javascript
tail = function (opts, each, cb) {
  // Fetch the proccess that we need.
  pm._findById(opts.sockPath, opts.pm_id, function (err, proc) {
    if (err) {
      return cb(err)
    }
    proc.pm2_log = opts.logPath
    // Tail logs.
    cb(null, pm._tailLogs(proc, each))
  })
}
```
- example usage
```shell
...
socket._pm_id = pmId

if (self._tails[pmId]) {
  return
}

// Tail logs.
pm.tail({
  sockPath: self.options.pm2Conf.DAEMON_RPC_PORT,
  logPath: self.options.pm2Conf.PM2_LOG_FILE_PATH,
  pm_id: pmId
}, function (err, lines) {
  if (err) {
    return emitError(err, pmId, keepANSI)
  }
...
```

#### <a name="apidoc.element.pm2-gui.pm.version"></a>[function <span class="apidocSignatureSpan">pm2-gui.pm.</span>version (sockPath, cb)](#apidoc.element.pm2-gui.pm.version)
- description and source-code
```javascript
version = function (sockPath, cb) {
  pm._rpc({
    sockPath: sockPath,
    events: [
      ['getVersion', {}, cb]
    ]
  })
}
```
- example usage
```shell
...
/**
* Get PM2 version and return it to client.
* @private
*/
Monitor.prototype._pm2Ver = function (socket) {
 var pm2RPC = this.options.pm2Conf.DAEMON_RPC_PORT
 console.info('Fetching pm2 version:', pm2RPC)
 pm.version(pm2RPC, function (err, version) {
   socket.emit('pm2_ver', (err || !version) ? '0.0.0' : version)
 })
}

/**
* Broadcast to all connected clients.
* @param {String} event
...
```



# <a name="apidoc.module.pm2-gui.stat"></a>[module pm2-gui.stat](#apidoc.module.pm2-gui.stat)

#### <a name="apidoc.element.pm2-gui.stat.cpuInfo"></a>[function <span class="apidocSignatureSpan">pm2-gui.stat.</span>cpuInfo ()](#apidoc.element.pm2-gui.stat.cpuInfo)
- description and source-code
```javascript
cpuInfo = function () {
  var cpus = this.cpus
  var idle = 0
  var total = 0
  for (var i in cpus) {
    idle += cpus[i].times.idle
    for (var k in cpus[i].times) {
      total += cpus[i].times[k]
    }
  }
  return {
    'idle': idle,
    'total': total
  }
}
```
- example usage
```shell
...
/**
* System CPU usage percentage (total).
* @param fn
* @param context
*/
stat.cpuUsage = function (fn, context) {
 setTimeout(function (ctx, stat1) {
   var stat2 = ctx.cpuInfo()
   var perc = 100 * (1 - (stat2.idle - stat1.idle) / (stat2.total - stat1.total))
   fn.call(context, null, perc.toFixed(2))
 }, 1000, this, this.cpuInfo())
}

/**
* System CPU usage detail information.
...
```

#### <a name="apidoc.element.pm2-gui.stat.cpuUsage"></a>[function <span class="apidocSignatureSpan">pm2-gui.stat.</span>cpuUsage (fn, context)](#apidoc.element.pm2-gui.stat.cpuUsage)
- description and source-code
```javascript
cpuUsage = function (fn, context) {
  setTimeout(function (ctx, stat1) {
    var stat2 = ctx.cpuInfo()
    var perc = 100 * (1 - (stat2.idle - stat1.idle) / (stat2.total - stat1.total))
    fn.call(context, null, perc.toFixed(2))
  }, 1000, this, this.cpuInfo())
}
```
- example usage
```shell
...

/**
 * Grep system states.
 * @param {Function} cb
 * @private
 */
Monitor.prototype._systemStat = function (cb) {
stat.cpuUsage(function (err, cpuUsage) {
  if (err) {
    // Log only.
    console.error('Can not load system/cpu/memory information: ', err.message)
  } else {
    // System states.
    this._sysStat = _.defaults(_(stat).pick('cpus', 'arch', 'hostname', 'platform', 'release', 'uptime', 'memory').clone(), {
      cpu: cpuUsage
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
