title: Express.js
---

### Settings

    app.set('x', 'yyy')
    app.get('x') //=> 'yyy'

    app.enable('trust proxy')
    app.disable('trust proxy')

    app.enabled('trust proxy') //=> true

### Env

    app.get('env')

### Config

    app.configure('production', function() {
      app.set...
    });

### Wares

    app.use(express.static(__dirname + '/public'));
    app.use(express.logger());

### Helpers

    app.locals({
      title: "MyApp",
    });

### Request

    req.params

    // GET  /user/tj
    req.params.name //=> "tj"

    req.params[0]

    // GET /search?q=tobi+ferret
    req.query.q // => "tobi ferret"

    req.cookies

    req.accepted
    [ { value: 'application/json', quality: 1, type: 'application', subtype: 'json' },
      { value: 'text/html', quality: 0.5, type: 'text',subtype: 'html' } ]

    req.is('html')
    req.is('text/html')

    req.path
    req.xhr

## Response

    res.redirect('/')
    res.redirect(301, '/')

    res.set('Content-Type', 'text/html')

    res.send('hi')
    res.send(200, 'hi')

    res.json({ a: 2 })
