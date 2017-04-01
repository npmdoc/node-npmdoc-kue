# api documentation for  [kue (v0.11.5)](http://automattic.github.io/kue/)  [![npm package](https://img.shields.io/npm/v/npmdoc-kue.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-kue) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-kue.svg)](https://travis-ci.org/npmdoc/node-npmdoc-kue)
#### Feature rich priority job queue backed by redis

[![NPM](https://nodei.co/npm/kue.png?downloads=true)](https://www.npmjs.com/package/kue)

[![apidoc](https://npmdoc.github.io/node-npmdoc-kue/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-kue_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-kue/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-kue/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "TJ Holowaychuk",
        "email": "tj@learnboost.com"
    },
    "bin": {
        "kue-dashboard": "bin/kue-dashboard"
    },
    "bugs": {
        "url": "https://github.com/Automattic/kue/issues"
    },
    "contributors": [
        {
            "name": "Behrad Zari",
            "email": "behradz@gmail.com"
        }
    ],
    "dependencies": {
        "body-parser": "^1.12.2",
        "express": "^4.12.2",
        "lodash": "^4.0.0",
        "nib": "~1.1.2",
        "node-redis-warlock": "~0.2.0",
        "pug": "^2.0.0-beta3",
        "redis": "~2.6.0-2",
        "reds": "^0.2.5",
        "stylus": "~0.54.5",
        "yargs": "^4.0.0"
    },
    "description": "Feature rich priority job queue backed by redis",
    "devDependencies": {
        "async": "^1.4.2",
        "chai": "^3.3.0",
        "coffee-script": "~1.10.0",
        "mocha": "^2.3.3",
        "should": "^3.1.0",
        "sinon": "^1.17.2",
        "supertest": "^1.1.0"
    },
    "directories": {},
    "dist": {
        "shasum": "ac2fa8c8087e4d4c48e5c9c2d4b17687eed0e1df",
        "tarball": "https://registry.npmjs.org/kue/-/kue-0.11.5.tgz"
    },
    "gitHead": "d5f0b655c6d697f526e0c8105faa06a153703cdf",
    "homepage": "http://automattic.github.io/kue/",
    "keywords": [
        "job",
        "queue",
        "worker",
        "redis"
    ],
    "license": "MIT",
    "main": "index",
    "maintainers": [
        {
            "name": "tjholowaychuk",
            "email": "tj@vision-media.ca"
        },
        {
            "name": "drudge",
            "email": "nick@penree.com"
        },
        {
            "name": "behrad",
            "email": "behradz@gmail.com"
        }
    ],
    "name": "kue",
    "optionalDependencies": {
        "reds": "^0.2.5"
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/Automattic/kue.git"
    },
    "scripts": {
        "test": "make test-all"
    },
    "version": "0.11.5"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module kue](#apidoc.module.kue)
1.  [function <span class="apidocSignatureSpan">kue.</span>Job ( type, data )](#apidoc.element.kue.Job)
1.  [function <span class="apidocSignatureSpan">kue.</span>createQueue ( options )](#apidoc.element.kue.createQueue)
1.  object <span class="apidocSignatureSpan">kue.</span>Job.prototype
1.  object <span class="apidocSignatureSpan">kue.</span>redis
1.  object <span class="apidocSignatureSpan">kue.</span>workers
1.  string <span class="apidocSignatureSpan">kue.</span>version

#### [module kue.Job](#apidoc.module.kue.Job)
1.  boolean <span class="apidocSignatureSpan">kue.Job.</span>disableSearch
1.  boolean <span class="apidocSignatureSpan">kue.Job.</span>jobEvents
1.  [function <span class="apidocSignatureSpan">kue.</span>Job ( type, data )](#apidoc.element.kue.Job.Job)
1.  [function <span class="apidocSignatureSpan">kue.Job.</span>get ( id, jobType, fn )](#apidoc.element.kue.Job.get)
1.  [function <span class="apidocSignatureSpan">kue.Job.</span>log ( id, fn )](#apidoc.element.kue.Job.log)
1.  [function <span class="apidocSignatureSpan">kue.Job.</span>range ( from, to, order, fn )](#apidoc.element.kue.Job.range)
1.  [function <span class="apidocSignatureSpan">kue.Job.</span>rangeByState ( state, from, to, order, fn )](#apidoc.element.kue.Job.rangeByState)
1.  [function <span class="apidocSignatureSpan">kue.Job.</span>rangeByType ( type, state, from, to, order, fn )](#apidoc.element.kue.Job.rangeByType)
1.  [function <span class="apidocSignatureSpan">kue.Job.</span>remove ( id, fn )](#apidoc.element.kue.Job.remove)
1.  [function <span class="apidocSignatureSpan">kue.Job.</span>removeBadJob ( id, jobType)](#apidoc.element.kue.Job.removeBadJob)
1.  object <span class="apidocSignatureSpan">kue.Job.</span>priorities

#### [module kue.Job.prototype](#apidoc.module.kue.Job.prototype)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>_getBackoffImpl ()](#apidoc.element.kue.Job.prototype._getBackoffImpl)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>active ( clbk )](#apidoc.element.kue.Job.prototype.active)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>attempt ( fn )](#apidoc.element.kue.Job.prototype.attempt)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>attempts ( n )](#apidoc.element.kue.Job.prototype.attempts)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>backoff ( param )](#apidoc.element.kue.Job.prototype.backoff)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>complete ( clbk )](#apidoc.element.kue.Job.prototype.complete)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>delay ( ms )](#apidoc.element.kue.Job.prototype.delay)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>delayed ( clbk )](#apidoc.element.kue.Job.prototype.delayed)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>error ( err )](#apidoc.element.kue.Job.prototype.error)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>events (events)](#apidoc.element.kue.Job.prototype.events)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>failed ( clbk )](#apidoc.element.kue.Job.prototype.failed)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>failedAttempt ( theErr, fn )](#apidoc.element.kue.Job.prototype.failedAttempt)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>get ( key, fn )](#apidoc.element.kue.Job.prototype.get)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>inactive ( clbk )](#apidoc.element.kue.Job.prototype.inactive)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>log ( str )](#apidoc.element.kue.Job.prototype.log)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>priority ( level )](#apidoc.element.kue.Job.prototype.priority)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>progress ( complete, total, data )](#apidoc.element.kue.Job.prototype.progress)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>reattempt ( attempts, clbk )](#apidoc.element.kue.Job.prototype.reattempt)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>refreshTtl ()](#apidoc.element.kue.Job.prototype.refreshTtl)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>remove ( fn )](#apidoc.element.kue.Job.prototype.remove)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>removeOnComplete ( param )](#apidoc.element.kue.Job.prototype.removeOnComplete)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>save ( fn )](#apidoc.element.kue.Job.prototype.save)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>searchKeys ( keys )](#apidoc.element.kue.Job.prototype.searchKeys)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>set ( key, val, fn )](#apidoc.element.kue.Job.prototype.set)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>state ( state, fn )](#apidoc.element.kue.Job.prototype.state)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>subscribe ( callback )](#apidoc.element.kue.Job.prototype.subscribe)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>toJSON ()](#apidoc.element.kue.Job.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>ttl ( param )](#apidoc.element.kue.Job.prototype.ttl)
1.  [function <span class="apidocSignatureSpan">kue.Job.prototype.</span>update ( fn )](#apidoc.element.kue.Job.prototype.update)

#### [module kue.redis](#apidoc.module.kue.redis)
1.  [function <span class="apidocSignatureSpan">kue.redis.</span>client ()](#apidoc.element.kue.redis.client)
1.  [function <span class="apidocSignatureSpan">kue.redis.</span>configureFactory ( options, queue )](#apidoc.element.kue.redis.configureFactory)
1.  [function <span class="apidocSignatureSpan">kue.redis.</span>createClientFactory ( options )](#apidoc.element.kue.redis.createClientFactory)
1.  [function <span class="apidocSignatureSpan">kue.redis.</span>pubsubClient ()](#apidoc.element.kue.redis.pubsubClient)
1.  [function <span class="apidocSignatureSpan">kue.redis.</span>reset ()](#apidoc.element.kue.redis.reset)



# <a name="apidoc.module.kue"></a>[module kue](#apidoc.module.kue)

#### <a name="apidoc.element.kue.Job"></a>[function <span class="apidocSignatureSpan">kue.</span>Job ( type, data )](#apidoc.element.kue.Job)
- description and source-code
```javascript
function Job( type, data ) {
  this.type          = type;
  this.data          = data || {};
  this._max_attempts = 1;
  this._jobEvents = exports.jobEvents;
//  this.client = redis.client();
  this.client = Job.client/* || (Job.client = redis.client())*/;
  this.priority('normal');
  this.on('error', function( err ) {
  });// prevent uncaught exceptions on failed job errors
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.createQueue"></a>[function <span class="apidocSignatureSpan">kue.</span>createQueue ( options )](#apidoc.element.kue.createQueue)
- description and source-code
```javascript
createQueue = function ( options ) {
  if( !Queue.singleton ) {
    Queue.singleton = new Queue(options);
  }
  events.subscribe();
  return Queue.singleton;

}
```
- example usage
```shell
...
  - [Screencasts](#screencasts)
  - [License](#license)



## Creating Jobs

First create a job 'Queue' with 'kue.createQueue()':

'''js
var kue = require('kue')
  , queue = kue.createQueue();
'''

Calling 'queue.create()' with the type of job ("email"), and arbitrary job data will return a 'Job', which can then be 'save()'ed
, adding it to redis, with a default priority level of "normal". The 'save()' method optionally accepts a callback, responding with
 an 'error' if something goes wrong. The 'title' key is special-cased, and will display in the job listings within the UI, making
 it easier to find a specific job.
...
```



# <a name="apidoc.module.kue.Job"></a>[module kue.Job](#apidoc.module.kue.Job)

#### <a name="apidoc.element.kue.Job.Job"></a>[function <span class="apidocSignatureSpan">kue.</span>Job ( type, data )](#apidoc.element.kue.Job.Job)
- description and source-code
```javascript
function Job( type, data ) {
  this.type          = type;
  this.data          = data || {};
  this._max_attempts = 1;
  this._jobEvents = exports.jobEvents;
//  this.client = redis.client();
  this.client = Job.client/* || (Job.client = redis.client())*/;
  this.priority('normal');
  this.on('error', function( err ) {
  });// prevent uncaught exceptions on failed job errors
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.Job.get"></a>[function <span class="apidocSignatureSpan">kue.Job.</span>get ( id, jobType, fn )](#apidoc.element.kue.Job.get)
- description and source-code
```javascript
get = function ( id, jobType, fn ) {
  if (typeof jobType === 'function' && !fn) {
    fn = jobType;
    jobType = '';
  }
  var client = redis.client()
    , job    = new Job;

  job.id = id;
  job.zid = client.createFIFO(id);
  client.hgetall(client.getKey('job:' + job.id), function( err, hash ) {
    if( err ) return fn(err);
    if( !hash ) {
      exports.removeBadJob(job.id, jobType);
      return fn(new Error('job "' + job.id + '" doesnt exist'));
    }
    if( !hash.type ) {
      exports.removeBadJob(job.id, jobType);
      return fn(new Error('job "' + job.id + '" is invalid'))
    }
    // TODO: really lame, change some methods so
    // we can just merge these
    job.type              = hash.type;
    job._ttl              = hash.ttl;
    job._delay            = hash.delay;
    job.priority(Number(hash.priority));
    job._progress         = hash.progress;
    job._attempts         = Number(hash.attempts);
    job._max_attempts     = Number(hash.max_attempts);
    job._state            = hash.state;
    job._error            = hash.error;
    job.created_at        = hash.created_at;
    job.promote_at        = hash.promote_at;
    job.updated_at        = hash.updated_at;
    job.failed_at         = hash.failed_at;
    job.started_at        = hash.started_at;
    job.duration          = hash.duration;
    job.workerId          = hash.workerId;
    job._removeOnComplete = hash.removeOnComplete;
    try {
      if( hash.data ) job.data = JSON.parse(hash.data);
      if( hash.result ) job.result = JSON.parse(hash.result);
      if( hash.progress_data ) job.progress_data = JSON.parse(hash.progress_data);
      if( hash.backoff ) {
        var source = 'job._backoff = ' + hash.backoff + ';';
//                require('vm').runInContext( source );
        eval(source);
      }
    } catch(e) {
      err = e;
    }
    fn(err, job);
  });
}
```
- example usage
```shell
...
Queue-level events provide access to the job-level events previously mentioned, however scoped to the 'Queue' instance to apply
logic at a "global" level. An example of this is removing completed jobs:

'''js
queue.on('job enqueue', function(id, type){
  console.log( 'Job %s got queued of type %s', id, type );

}).on('job complete', function(id, result){
  kue.Job.get(id, function(err, job){
    if (err) return;
    job.remove(function(err){
      if (err) throw err;
      console.log('removed completed job #%d', job.id);
    });
  });
});
...
```

#### <a name="apidoc.element.kue.Job.log"></a>[function <span class="apidocSignatureSpan">kue.Job.</span>log ( id, fn )](#apidoc.element.kue.Job.log)
- description and source-code
```javascript
log = function ( id, fn ) {
<span class="apidocCodeCommentSpan">  /*redis*/
</span>  Job.client/*()*/.lrange(Job.client.getKey('job:' + id + ':log'), 0, -1, fn);
}
```
- example usage
```shell
...

'''js
var job = queue.create('email', {
    title: 'welcome email for tj'
  , to: 'tj@learnboost.com'
  , template: 'welcome-email'
}).save( function(err){
   if( !err ) console.log( job.id );
});
'''

### Job Priority

To specify the priority of a job, simply invoke the 'priority()' method with a number, or priority name, which is mapped to a number
.
...
```

#### <a name="apidoc.element.kue.Job.range"></a>[function <span class="apidocSignatureSpan">kue.Job.</span>range ( from, to, order, fn )](#apidoc.element.kue.Job.range)
- description and source-code
```javascript
range = function ( from, to, order, fn ) {
  redis.client().zrange(redis.client().getKey('jobs'), from, to, get(fn, order));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.Job.rangeByState"></a>[function <span class="apidocSignatureSpan">kue.Job.</span>rangeByState ( state, from, to, order, fn )](#apidoc.element.kue.Job.rangeByState)
- description and source-code
```javascript
rangeByState = function ( state, from, to, order, fn ) {
  redis.client().zrange(redis.client().getKey('jobs:' + state), from, to, get(fn, order));
}
```
- example usage
```shell
...
  // you may want to fetch each id to get the Job object out of it...
});
'''

however the second one doesn't scale to large deployments, there you can use more specific 'Job' static methods:

'''js
kue.Job.rangeByState( 'failed', 0, n, 'asc', function( err, jobs ) {
  // you have an array of maximum n Job objects here
});
'''
or

'''js
kue.Job.rangeByType( 'my-job-type', 'failed', 0, n, 'asc', function( err, jobs ) {
...
```

#### <a name="apidoc.element.kue.Job.rangeByType"></a>[function <span class="apidocSignatureSpan">kue.Job.</span>rangeByType ( type, state, from, to, order, fn )](#apidoc.element.kue.Job.rangeByType)
- description and source-code
```javascript
rangeByType = function ( type, state, from, to, order, fn ) {
  redis.client().zrange(redis.client().getKey('jobs:' + type + ':' + state), from, to, get(fn, order, type));
}
```
- example usage
```shell
...
kue.Job.rangeByState( 'failed', 0, n, 'asc', function( err, jobs ) {
  // you have an array of maximum n Job objects here
});
'''
or

'''js
kue.Job.rangeByType( 'my-job-type', 'failed', 0, n, 'asc', function( err, jobs ) {
  // you have an array of maximum n Job objects here
});
'''

**Note** *that the last two methods are subject to change in later Kue versions.*
...
```

#### <a name="apidoc.element.kue.Job.remove"></a>[function <span class="apidocSignatureSpan">kue.Job.</span>remove ( id, fn )](#apidoc.element.kue.Job.remove)
- description and source-code
```javascript
remove = function ( id, fn ) {
  fn = fn || noop;
  exports.get(id, function( err, job ) {
    if( err ) return fn(err);
    if( !job ) return fn(new Error('failed to find job ' + id));
    job.remove(fn);
  });
}
```
- example usage
```shell
...
'''js
queue.on('job enqueue', function(id, type){
  console.log( 'Job %s got queued of type %s', id, type );

}).on('job complete', function(id, result){
  kue.Job.get(id, function(err, job){
    if (err) return;
    job.remove(function(err){
      if (err) throw err;
      console.log('removed completed job #%d', job.id);
    });
  });
});
'''
...
```

#### <a name="apidoc.element.kue.Job.removeBadJob"></a>[function <span class="apidocSignatureSpan">kue.Job.</span>removeBadJob ( id, jobType)](#apidoc.element.kue.Job.removeBadJob)
- description and source-code
```javascript
removeBadJob = function ( id, jobType) {
  var client = redis.client();
  var zid = client.createFIFO(id);
  client.multi()
    .del(client.getKey('job:' + id + ':log'))
    .del(client.getKey('job:' + id))
    .zrem(client.getKey('jobs:inactive'), zid)
    .zrem(client.getKey('jobs:active'), zid)
    .zrem(client.getKey('jobs:complete'), zid)
    .zrem(client.getKey('jobs:failed'), zid)
    .zrem(client.getKey('jobs:delayed'), zid)
    .zrem(client.getKey('jobs'), zid)
    .zrem(client.getKey('jobs:' + jobType + ':inactive'), zid)
    .zrem(client.getKey('jobs:' + jobType+ ':active'), zid)
    .zrem(client.getKey('jobs:' + jobType + ':complete'), zid)
    .zrem(client.getKey('jobs:' + jobType + ':failed'), zid)
    .zrem(client.getKey('jobs:' + jobType + ':delayed'), zid)
    .exec();
  if( !exports.disableSearch ) {
    getSearch().remove(id);
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kue.Job.prototype"></a>[module kue.Job.prototype](#apidoc.module.kue.Job.prototype)

#### <a name="apidoc.element.kue.Job.prototype._getBackoffImpl"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>_getBackoffImpl ()](#apidoc.element.kue.Job.prototype._getBackoffImpl)
- description and source-code
```javascript
_getBackoffImpl = function () {
  var supported_backoffs = {
    fixed: function( delay ) {
      return function( attempts ) {
        return delay;
      };
    }
    , exponential: function( delay ) {
      return function( attempts ) {
        return Math.round(delay * 0.5 * ( Math.pow(2, attempts) - 1));
      };
    }
  };
  if( _.isPlainObject(this._backoff) ) {
    return supported_backoffs[ this._backoff.type ](this._backoff.delay || this._delay);
  } else {
    return this._backoff;
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.Job.prototype.active"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>active ( clbk )](#apidoc.element.kue.Job.prototype.active)
- description and source-code
```javascript
active = function ( clbk ) {
  return this.state('active', clbk);
}
```
- example usage
```shell
...


### Programmatic Job Management

If you did none of above in [Error Handling](#error-handling) section or your process lost active jobs in any way, you can recover
 from them when your process is restarted. A blind logic would be to re-queue all stuck jobs:

'''js
queue.active( function( err, ids ) {
  ids.forEach( function( id ) {
    kue.Job.get( id, function( err, job ) {
      // Your application should check if job is a stuck one
      job.inactive();
    });
  });
});
...
```

#### <a name="apidoc.element.kue.Job.prototype.attempt"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>attempt ( fn )](#apidoc.element.kue.Job.prototype.attempt)
- description and source-code
```javascript
attempt = function ( fn ) {
  var client = this.client
    , id     = this.id
    , key    = client.getKey('job:' + id);

  this._attempts = this._attempts || 0;
  if( this._attempts < this._max_attempts ) {
    client.hincrby(key, 'attempts', 1, function( err, attempts ) {
      this._attempts = attempts;
      fn(err, Math.max(0, this._max_attempts - attempts), attempts, this._max_attempts);
    }.bind(this));
  } else {
    fn(null, 0, this._attempts, this._max_attempts);
  }
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.Job.prototype.attempts"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>attempts ( n )](#apidoc.element.kue.Job.prototype.attempts)
- description and source-code
```javascript
attempts = function ( n ) {
  this._max_attempts = n;
  return this;
}
```
- example usage
```shell
...
 , high: -10
 , critical: -15
};
'''

### Failure Attempts

By default jobs only have _one_ attempt, that is when they fail, they are marked as a failure, and remain that way until you intervene
. However, Kue allows you to specify this, which is important for jobs such as transferring an email, which upon failure, may usually
 retry without issue. To do this invoke the '.attempts()' method with a number.

'''js
queue.create('email', {
    title: 'welcome email for tj'
  , to: 'tj@learnboost.com'
  , template: 'welcome-email'
}).priority('high').attempts(5).save();
...
```

#### <a name="apidoc.element.kue.Job.prototype.backoff"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>backoff ( param )](#apidoc.element.kue.Job.prototype.backoff)
- description and source-code
```javascript
backoff = function ( param ) {
  if( 0 == arguments.length ) return this._backoff;
  this._backoff = param;
  return this;
}
```
- example usage
```shell
...
'''

### Failure Backoff
Job retry attempts are done as soon as they fail, with no delay, even if your job had a delay set via 'Job#delay'. If you want to
 delay job re-attempts upon failures (known as backoff) you can use 'Job#backoff' method in different ways:

'''js
// Honor job's original delay (if set) at each attempt, defaults to fixed backoff
job.attempts(3).backoff( true )

// Override delay value, fixed backoff
job.attempts(3).backoff( {delay: 60*1000, type:'fixed'} )

// Enable exponential backoff using original delay (if set)
job.attempts(3).backoff( {type:'exponential'} )
...
```

#### <a name="apidoc.element.kue.Job.prototype.complete"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>complete ( clbk )](#apidoc.element.kue.Job.prototype.complete)
- description and source-code
```javascript
complete = function ( clbk ) {
  return this.set('progress', 100).state('complete', clbk);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.Job.prototype.delay"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>delay ( ms )](#apidoc.element.kue.Job.prototype.delay)
- description and source-code
```javascript
delay = function ( ms ) {
  if( 0 == arguments.length ) return this._delay;
  if( _.isDate(ms) ) {
    ms = parseInt(ms.getTime() - Date.now())
  }
  if( ms > 0 ) {
    this._delay = ms;
  }
  return this;
}
```
- example usage
```shell
...
});
'''

The events available are the same as mentioned in "Job Events", however prefixed with "job ".

### Delayed Jobs

Delayed jobs may be scheduled to be queued for an arbitrary distance in time by invoking the '.delay(ms)' method, passing the number
 of milliseconds relative to _now_. Alternatively, you can pass a JavaScript 'Date' object with a specific time in the future.
This automatically flags the 'Job' as "delayed".

'''js
var email = queue.create('email', {
  title: 'Account renewal required'
, to: 'tj@learnboost.com'
, template: 'renewal-email'
...
```

#### <a name="apidoc.element.kue.Job.prototype.delayed"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>delayed ( clbk )](#apidoc.element.kue.Job.prototype.delayed)
- description and source-code
```javascript
delayed = function ( clbk ) {
  return this.state('delayed', clbk);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.Job.prototype.error"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>error ( err )](#apidoc.element.kue.Job.prototype.error)
- description and source-code
```javascript
error = function ( err ) {
  var str, summary;
  if( 0 == arguments.length ) return this._error;

  if( 'string' == typeof err ) {
    str     = err;
    summary = '';
  } else {
    if( err.stack && 'string' === typeof err.stack ) {
      str = err.stack
    } else { //TODO what happens to CallSite[] err.stack?
      str = err.message
    }
    summary = ('string' === typeof str) ? str.split('\n')[ 0 ] : '';
  }
  this.set('error', str);
  this.log('%s', summary);
  events.emit(this.id, 'error', str);
  return this;
}
```
- example usage
```shell
...



2. Binding to 'uncaughtException' and gracefully shutting down the Kue, however this is not a recommended error handling idiom in
 javascript since you are losing the error context.

'''js
process.once( 'uncaughtException', function(err){
  console.error( 'Something bad happened: ', err );
  queue.shutdown( 1000, function(err2){
    console.error( 'Kue shutdown result: ', err2 || 'OK' );
    process.exit( 0 );
  });
});
'''
...
```

#### <a name="apidoc.element.kue.Job.prototype.events"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>events (events)](#apidoc.element.kue.Job.prototype.events)
- description and source-code
```javascript
events = function (events) {
  this._jobEvents = !!events;
  return this;
}
```
- example usage
```shell
...
 '''js
 kue.createQueue({jobEvents: false})
 '''

 Alternatively, you can use the job level function 'events' to control whether events are fired for a job at the job level.

 '''js
var job = queue.create('test').events(false).save();
 '''

### Queue Events

Queue-level events provide access to the job-level events previously mentioned, however scoped to the 'Queue' instance to apply
logic at a "global" level. An example of this is removing completed jobs:

'''js
...
```

#### <a name="apidoc.element.kue.Job.prototype.failed"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>failed ( clbk )](#apidoc.element.kue.Job.prototype.failed)
- description and source-code
```javascript
failed = function ( clbk ) {
  this.failed_at = Date.now();
  return this.set('failed_at', this.failed_at).state('failed', clbk);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.Job.prototype.failedAttempt"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>failedAttempt ( theErr, fn )](#apidoc.element.kue.Job.prototype.failedAttempt)
- description and source-code
```javascript
failedAttempt = function ( theErr, fn ) {
  this.error(theErr).failed(function() {
    this.attempt(function( error, remaining, attempts/*, max*/ ) {
      if( error ) {
        this.emit( 'error', error );
        return fn && fn( error );
      }
      if( remaining > 0 ) {
        this.reattempt(attempts, function( err ) {
          if( err ) {
            this.emit( 'error', err );
            return fn && fn( err );
          }
          fn && fn( err, true, attempts );
        }.bind(this));
      } else if( remaining === 0 )  {
        fn && fn( null, false, attempts );
      } else {
        fn && fn( new Error('Attempts Exceeded') );
      }
    }.bind(this));
  }.bind(this));
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.Job.prototype.get"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>get ( key, fn )](#apidoc.element.kue.Job.prototype.get)
- description and source-code
```javascript
get = function ( key, fn ) {
  this.client.hget(this.client.getKey('job:' + this.id), key, fn || noop);
  return this;
}
```
- example usage
```shell
...
Queue-level events provide access to the job-level events previously mentioned, however scoped to the 'Queue' instance to apply
logic at a "global" level. An example of this is removing completed jobs:

'''js
queue.on('job enqueue', function(id, type){
  console.log( 'Job %s got queued of type %s', id, type );

}).on('job complete', function(id, result){
  kue.Job.get(id, function(err, job){
    if (err) return;
    job.remove(function(err){
      if (err) throw err;
      console.log('removed completed job #%d', job.id);
    });
  });
});
...
```

#### <a name="apidoc.element.kue.Job.prototype.inactive"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>inactive ( clbk )](#apidoc.element.kue.Job.prototype.inactive)
- description and source-code
```javascript
inactive = function ( clbk ) {
  return this.state('inactive', clbk);
}
```
- example usage
```shell
...
  }
});
'''

and iterating over job ids

'''js
queue.inactive( function( err, ids ) { // others are active, complete, failed, delayed
  // you may want to fetch each id to get the Job object out of it...
});
'''

however the second one doesn't scale to large deployments, there you can use more specific 'Job' static methods:

'''js
...
```

#### <a name="apidoc.element.kue.Job.prototype.log"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>log ( str )](#apidoc.element.kue.Job.prototype.log)
- description and source-code
```javascript
log = function ( str ) {
  if(typeof str === 'string') {
    var formatted = util.format.apply(util, arguments);
  }else{
    var formatted = util.inspect(str);
  }
  this.client.rpush(this.client.getKey('job:' + this.id + ':log'), formatted, noop);
  this.set('updated_at', Date.now());
  return this;
}
```
- example usage
```shell
...

'''js
var job = queue.create('email', {
    title: 'welcome email for tj'
  , to: 'tj@learnboost.com'
  , template: 'welcome-email'
}).save( function(err){
   if( !err ) console.log( job.id );
});
'''

### Job Priority

To specify the priority of a job, simply invoke the 'priority()' method with a number, or priority name, which is mapped to a number
.
...
```

#### <a name="apidoc.element.kue.Job.prototype.priority"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>priority ( level )](#apidoc.element.kue.Job.prototype.priority)
- description and source-code
```javascript
priority = function ( level ) {
  if( 0 == arguments.length ) return this._priority;
  this._priority = null == priorities[ level ]
    ? level
    : priorities[ level ];
  return this;
}
```
- example usage
```shell
...
To specify the priority of a job, simply invoke the 'priority()' method with a number, or priority name, which is mapped to a number
.

'''js
queue.create('email', {
title: 'welcome email for tj'
  , to: 'tj@learnboost.com'
  , template: 'welcome-email'
}).priority('high').save();
'''

The default priority map is as follows:

'''js
{
low: 10
...
```

#### <a name="apidoc.element.kue.Job.prototype.progress"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>progress ( complete, total, data )](#apidoc.element.kue.Job.prototype.progress)
- description and source-code
```javascript
progress = function ( complete, total, data ) {
  if( 0 == arguments.length ) return this._progress;
  var n = Math.min(100, complete * 100 / total | 0);
  this.set('progress', n);

  // If this stringify fails because of a circular structure, even the one in events.emit would.
  // So it does not make sense to try/catch this.
  if( data ) this.set('progress_data', JSON.stringify(data));

  this.set('updated_at', Date.now());
  this.refreshTtl();
  events.emit(this.id, 'progress', n, data);
  return this;
}
```
- example usage
```shell
...
job.log({key: 'some key', value: 10});
job.log({[1,2,3,5,8]});
job.log(10.1);
'''

### Job Progress

Job progress is extremely useful for long-running jobs such as video conversion. To update the job's progress simply invoke 'job
.progress(completed, total [, data])':

'''js
job.progress(frames, totalFrames);
'''

data can be used to pass extra information about the job. For example a message or an object with some extra contextual data to
the current status.
...
```

#### <a name="apidoc.element.kue.Job.prototype.reattempt"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>reattempt ( attempts, clbk )](#apidoc.element.kue.Job.prototype.reattempt)
- description and source-code
```javascript
reattempt = function ( attempts, clbk ) {
  clbk = clbk || noop;
  if( this.backoff() ) {
    var delay = this.delay();
    if( _.isFunction(this._getBackoffImpl()) ) {
      try {
        delay = this._getBackoffImpl().apply(this, [ attempts ]);
      } catch(e) {
        clbk(e);
      }
    }
    var self = this;
    this.delay(delay).update(function( err ) {
      if( err ) return clbk(err);
      self.delayed(clbk);
    });
  } else {
    this.inactive(clbk);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.Job.prototype.refreshTtl"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>refreshTtl ()](#apidoc.element.kue.Job.prototype.refreshTtl)
- description and source-code
```javascript
refreshTtl = function () {
  ('active' === this.state() && this._ttl > 0)
    ?
    this.client.zadd(this.client.getKey('jobs:' + this.state()), Date.now() + parseInt(this._ttl), this.zid, noop)
    :
    noop();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.Job.prototype.remove"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>remove ( fn )](#apidoc.element.kue.Job.prototype.remove)
- description and source-code
```javascript
remove = function ( fn ) {
  var client = this.client;
  client.multi()
    .zrem(client.getKey('jobs:' + this.state()), this.zid)
    .zrem(client.getKey('jobs:' + this.type + ':' + this.state()), this.zid)
    .zrem(client.getKey('jobs'), this.zid)
    .del(client.getKey('job:' + this.id + ':log'))
    .del(client.getKey('job:' + this.id))
    .exec(function( err ) {
//            events.remove(this);
      events.emit(this.id, 'remove', this.type);
      if( !exports.disableSearch ) {
        getSearch().remove(this.id, fn);
      } else {
        fn && fn(err);
      }
    }.bind(this));
  return this;
}
```
- example usage
```shell
...
'''js
queue.on('job enqueue', function(id, type){
  console.log( 'Job %s got queued of type %s', id, type );

}).on('job complete', function(id, result){
  kue.Job.get(id, function(err, job){
    if (err) return;
    job.remove(function(err){
      if (err) throw err;
      console.log('removed completed job #%d', job.id);
    });
  });
});
'''
...
```

#### <a name="apidoc.element.kue.Job.prototype.removeOnComplete"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>removeOnComplete ( param )](#apidoc.element.kue.Job.prototype.removeOnComplete)
- description and source-code
```javascript
removeOnComplete = function ( param ) {
  if( 0 == arguments.length ) return this._removeOnComplete;
  this._removeOnComplete = param;
  return this;
}
```
- example usage
```shell
...
**Note** *in a clustered deployment your application should be aware not to involve a job that is valid, currently inprocess by
other workers.*

### Job Cleanup

Jobs data and search indexes eat up redis memory space, so you will need some job-keeping process in real world deployments. Your
 first chance is using automatic job removal on completion.

'''javascript
queue.create( ... ).removeOnComplete( true ).save()
'''

But if you eventually/temporally need completed job data, you can setup an on-demand job removal script like below to remove top
 'n' completed jobs:

'''js
kue.Job.rangeByState( 'complete', 0, n, 'asc', function( err, jobs ) {
jobs.forEach( function( job ) {
...
```

#### <a name="apidoc.element.kue.Job.prototype.save"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>save ( fn )](#apidoc.element.kue.Job.prototype.save)
- description and source-code
```javascript
save = function ( fn ) {
  var client = this.client
    , fn     = fn || noop
    , max    = this._max_attempts
    , self   = this;

  // update
  if( this.id ) return this.update(fn);

  // incr id
  client.incr(client.getKey('ids'), function( err, id ) {
    if( err ) return fn(err);
    // add the job for event mapping
    self.id = id;
    self.zid = client.createFIFO(id);
    self.subscribe(function() {
      self._state     = self._state || (this._delay ? 'delayed' : 'inactive');
      if( max ) { self.set('max_attempts', max); }
      client.sadd(client.getKey('job:types'), self.type, noop);
      self.set('type', self.type);
      var now         = Date.now();
      self.created_at = now;
      self.set('created_at', self.created_at);
      self.promote_at = now + (self._delay || 0);
      self.set('promote_at', self.promote_at);
      self.update(fn);
    }.bind(this));
  }.bind(this));
  return this;
}
```
- example usage
```shell
...
Calling 'queue.create()' with the type of job ("email"), and arbitrary job data will return a 'Job', which can then be 'save()'ed
, adding it to redis, with a default priority level of "normal". The 'save()' method optionally accepts a callback, responding with
 an 'error' if something goes wrong. The 'title' key is special-cased, and will display in the job listings within the UI, making
 it easier to find a specific job.

'''js
var job = queue.create('email', {
    title: 'welcome email for tj'
  , to: 'tj@learnboost.com'
  , template: 'welcome-email'
}).save( function(err){
   if( !err ) console.log( job.id );
});
'''

### Job Priority

To specify the priority of a job, simply invoke the 'priority()' method with a number, or priority name, which is mapped to a number
.
...
```

#### <a name="apidoc.element.kue.Job.prototype.searchKeys"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>searchKeys ( keys )](#apidoc.element.kue.Job.prototype.searchKeys)
- description and source-code
```javascript
searchKeys = function ( keys ) {
  if( 0 == arguments.length ) return this._searchKeys;
  this._searchKeys = keys || [];
  if( !_.isArray(this._searchKeys) ) {
    this._searchKeys = [ this._searchKeys ];
  }
  return this;
}
```
- example usage
```shell
...
'''javascript
var kue = require('kue');
queue = kue.createQueue();
queue.create('email', {
    title: 'welcome email for tj'
  , to: 'tj@learnboost.com'
  , template: 'welcome-email'
}).searchKeys( ['to', 'title'] ).save();
'''

Search feature is turned off by default from Kue '>=0.9.0'. Read more about this [here](https://github.com/Automattic/kue/issues
/412). You should enable search indexes and add [reds](https://www.npmjs.com/package/reds) in your dependencies if you need to:

'''javascript
var kue = require('kue');
q = kue.createQueue({
...
```

#### <a name="apidoc.element.kue.Job.prototype.set"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>set ( key, val, fn )](#apidoc.element.kue.Job.prototype.set)
- description and source-code
```javascript
set = function ( key, val, fn ) {
  this.client.hset(this.client.getKey('job:' + this.id), key, val, fn || noop);
  return this;
}
```
- example usage
```shell
...
kue.createQueue(...);
kue.app.listen(3000);
'''

The title defaults to "Kue", to alter this invoke:

'''js
kue.app.set('title', 'My Application');
'''

**Note** *that if you are using non-default Kue options, 'kue.createQueue(...)' must be called before accessing 'kue.app'.*

### Third-party interfaces

You can also use [Kue-UI](https://github.com/StreetHub/kue-ui) web interface contributed by [Arnaud Bénard](https://github.com/arnaudbenard
)
...
```

#### <a name="apidoc.element.kue.Job.prototype.state"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>state ( state, fn )](#apidoc.element.kue.Job.prototype.state)
- description and source-code
```javascript
state = function ( state, fn ) {
  if( 0 == arguments.length ) return this._state;
  var client   = this.client
    , fn       = fn || noop;
  var oldState = this._state;
  var multi    = client.multi();
  if( oldState && oldState != '' && oldState != state ) {
    multi
      .zrem(client.getKey('jobs:' + oldState), this.zid)
      .zrem(client.getKey('jobs:' + this.type + ':' + oldState), this.zid);
  }
  multi
    .hset(client.getKey('job:' + this.id), 'state', state)
    .zadd(client.getKey('jobs:' + state), this._priority, this.zid)
    .zadd(client.getKey('jobs:' + this.type + ':' + state), this._priority, this.zid);

  // use promote_at as score when job moves to delayed
  ('delayed' === state) ? multi.zadd(client.getKey('jobs:' + state), parseInt(this.promote_at), this.zid) : noop();
  ('active' === state && this._ttl > 0) ? multi.zadd(client.getKey('jobs:' + state), Date.now() + parseInt(this._ttl), this.zid) :
noop();
  ('active' === state && !this._ttl) ? multi.zadd(client.getKey('jobs:' + state), this._priority<0?this._priority:-this._priority
, this.zid) : noop();
  ('inactive' === state) ? multi.lpush(client.getKey(this.type + ':jobs'), 1) : noop();

  this.set('updated_at', Date.now());
  this._state = state;
  multi.exec(function( err, replies ) {
    if( !err ) {
      (this._state === 'inactive') ? events.emit(this.id, 'enqueue', this.type) : noop();
    }
    return fn(err);
  }.bind(this));
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.Job.prototype.subscribe"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>subscribe ( callback )](#apidoc.element.kue.Job.prototype.subscribe)
- description and source-code
```javascript
subscribe = function ( callback ) {
  if( this._jobEvents ) {
    events.add(this, callback);
  } else {
    callback && callback();
  }
  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.Job.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>toJSON ()](#apidoc.element.kue.Job.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  return {
    id: this.id
    , type: this.type
    , data: this.data
    , result: this.result
    , priority: this._priority
    , progress: this._progress || 0
    , progress_data: this.progress_data
    , state: this._state
    , error: this._error
    , created_at: this.created_at
    , promote_at: this.promote_at
    , updated_at: this.updated_at
    , failed_at: this.failed_at
    , started_at: this.started_at
    , duration: this.duration
    , delay: this._delay
    , workerId: this.workerId
    , ttl: this._ttl
    , attempts: {
      made: Number(this._attempts) || 0
      , remaining: this._attempts > 0 ? this._max_attempts - this._attempts : Number(this._max_attempts) || 1
      , max: Number(this._max_attempts) || 1
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.Job.prototype.ttl"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>ttl ( param )](#apidoc.element.kue.Job.prototype.ttl)
- description and source-code
```javascript
ttl = function ( param ) {
  if( 0 == arguments.length ) return this._ttl;
  if( param > 0 ) {
    this._ttl = param;
  }
  return this;
}
```
- example usage
```shell
...
In the last scenario, provided function will be executed (via eval) on each re-attempt to get next attempt delay value, meaning
that you can't reference external/context variables within it.

### Job TTL

Job producers can set an expiry value for the time their job can live in active state, so that if workers didn't reply in timely
 fashion, Kue will fail it with 'TTL exceeded' error message preventing that job from being stuck in active state and spoiling concurrency
.

'''js
queue.create('email', {title: 'email job with TTL'}).ttl(milliseconds).save();
'''

### Job Logs

Job-specific logs enable you to expose information to the UI at any point in the job's life-time. To do so simply invoke 'job.log
()', which accepts a message string as well as variable-arguments for sprintf-like support:

'''js
...
```

#### <a name="apidoc.element.kue.Job.prototype.update"></a>[function <span class="apidocSignatureSpan">kue.Job.prototype.</span>update ( fn )](#apidoc.element.kue.Job.prototype.update)
- description and source-code
```javascript
update = function ( fn ) {
  var json;

  // serialize json data
  try {
    json = JSON.stringify(this.data);
  } catch(err) {
    fn(err);
    return this;
  }

  // delay
  if( this._delay ) {
    this.set('delay', this._delay);
    if( this.created_at ) {
      var timestamp   = parseInt(this.failed_at || this.created_at, 10)
        , delay       = parseInt(this._delay);
      this.promote_at = timestamp + delay;
      this.set('promote_at', this.promote_at);
    }
  }
  if( this._ttl ) {
    this.set('ttl', this._ttl);
  }
  if( this._removeOnComplete ) this.set('removeOnComplete', this._removeOnComplete);
  if( this._backoff ) {
    if( _.isPlainObject(this._backoff) ) this.set('backoff', JSON.stringify(this._backoff));
    else this.set('backoff', this._backoff.toString());
  }

  // updated timestamp
  this.set('updated_at', Date.now());
  this.refreshTtl();

  // priority
  this.set('priority', this._priority);

  this.client.zadd(this.client.getKey('jobs'), this._priority, this.zid, noop);

  // data
  this.set('data', json, function() {
    // state
    this.state(this._state, fn);
  }.bind(this));

  if( !exports.disableSearch ) {
    if( this.searchKeys() ) {
      this.searchKeys().forEach(function( key ) {
        var value = _.get(this.data, key);
        if( !_.isString(value) ) {
          value = JSON.stringify(value);
        }
        getSearch().index(value, this.id);
      }.bind(this));
    } else {
      getSearch().index(json, this.id);
    }
  }
  return this;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.kue.redis"></a>[module kue.redis](#apidoc.module.kue.redis)

#### <a name="apidoc.element.kue.redis.client"></a>[function <span class="apidocSignatureSpan">kue.redis.</span>client ()](#apidoc.element.kue.redis.client)
- description and source-code
```javascript
client = function () {
  return exports._client || (exports._client = exports.createClient());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.redis.configureFactory"></a>[function <span class="apidocSignatureSpan">kue.redis.</span>configureFactory ( options, queue )](#apidoc.element.kue.redis.configureFactory)
- description and source-code
```javascript
configureFactory = function ( options, queue ) {
  options.prefix = options.prefix || 'q';

  if( typeof options.redis === 'string' ) {
    // parse the url
    var conn_info = url.parse(options.redis, true<span class="apidocCodeCommentSpan"> /* parse query string */);
    if( conn_info.protocol !== 'redis:' ) {
      throw new Error('kue connection string must use the redis: protocol');
    }

    options.redis = {
      port: conn_info.port || 6379,
      host: conn_info.hostname,
      db: (conn_info.pathname ? conn_info.pathname.substr(1) : null) || 0,
      // see https://github.com/mranney/node_redis#rediscreateclient
      options: conn_info.query
    };

    if( conn_info.auth ) {
      options.redis.auth = conn_info.auth.replace(/.*?:/, '');
    }

  }

  options.redis = options.redis || {};

  // guarantee that redis._client has not been populated.
  // may warrant some more testing - i was running into cases where shutdown
  // would call redis.reset but an event would be emitted after the reset
  // which would re-create the client and cache it in the redis module.
  exports.reset();

  /**
   * Create a RedisClient.
   *
   * @return {RedisClient}
   * @api private
   */
</span>  exports.createClient = function() {
    var clientFactoryMethod = options.redis.createClientFactory || exports.createClientFactory;
    var client              = clientFactoryMethod(options);

    client.on('error', function( err ) {
      queue.emit('error', err);
    });

    client.prefix           = options.prefix;

    // redefine getKey to use the configured prefix
    client.getKey = function( key ) {
      if( client.constructor.name == 'Redis'  || client.constructor.name == 'Cluster') {
        // {prefix}:jobs format is needed in using ioredis cluster to keep they keys in same node
        // otherwise multi commands fail, since they use ioredis's pipeline.
        return '{' + this.prefix + '}:' + key;
      }
      return this.prefix + ':' + key;
    };

    client.createFIFO = function( id ) {
      //Create an id for the zset to preserve FIFO order
      var idLen = '' + id.toString().length;
      var len = 2 - idLen.length;
      while (len--) idLen = '0' + idLen;
      return idLen + '|' + id;
    };

    // Parse out original ID from zid
    client.stripFIFO = function( zid ) {
      if ( typeof zid === 'string' ) {
        return +zid.substr(zid.indexOf('|')+1);
      } else {
        // Sometimes this gets called with an undefined
        // it seems to be OK to have that not resolve to an id
        return zid;
      }
    };

    return client;
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.redis.createClientFactory"></a>[function <span class="apidocSignatureSpan">kue.redis.</span>createClientFactory ( options )](#apidoc.element.kue.redis.createClientFactory)
- description and source-code
```javascript
createClientFactory = function ( options ) {
  var socket = options.redis.socket;
  var port   = !socket ? (options.redis.port || 6379) : null;
  var host   = !socket ? (options.redis.host || '127.0.0.1') : null;
  var db   = !socket ? (options.redis.db || 0) : null;
  var client = redis.createClient(socket || port, host, options.redis.options);
  if( options.redis.auth ) {
    client.auth(options.redis.auth);
  }
  if( db >= 0 ){
    client.select(db);
  }
  return client;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.redis.pubsubClient"></a>[function <span class="apidocSignatureSpan">kue.redis.</span>pubsubClient ()](#apidoc.element.kue.redis.pubsubClient)
- description and source-code
```javascript
pubsubClient = function () {
  return exports._pubsub || (exports._pubsub = exports.createClient());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.kue.redis.reset"></a>[function <span class="apidocSignatureSpan">kue.redis.</span>reset ()](#apidoc.element.kue.redis.reset)
- description and source-code
```javascript
reset = function () {
  exports._client && exports._client.quit();
  exports._pubsub && exports._pubsub.quit();
  exports._client = null;
  exports._pubsub = null;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
