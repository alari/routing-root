routing-root
============

Polymer html5 Routing Component

How It Works
------------

#### 1. Install an element like you always do.

#### 2. Add an import to your main file

```
<link rel="import" href="bower_components/routing-root/routing-root.html">
```

#### 3. Wrap your view with <routing-root>. Use <routing-recognizer> for individual routes.

```
  <routing-root active="true">
    <routing-recognizer pattern="/test/:param/:param2">
      will be resolved only on match
    </routing-recognizer>
    
    <routing-recognizer pattern="/">
      index page pattern...
    </routing-recognizer>
  </routing-root>
```

#### 4. You may get params by `params` attribute binding. Do it inside your own Polymer definitions.\

```
(...imports...)
<polymer-element name="some-tag" noscript>
  <template>
    <routing-recognizer pattern="/test/:param" params="{{ p }}"></routing-recognizer>
    <routing-history path="{{ path }}"></routing-history>
    <ul>
      <li>Current param is: {{ p.param }}</li>
      <li>Current path is: {{ path }}</li>
    </ul>
  </template>
</polymer-element>
```

#### 5. Change the route by using `<a href>`, or by changing `<routing-history>.path`.

#### 6. Got any question? File an issue!
