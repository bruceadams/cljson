# cljson

Cljson is an [edn](https://github.com/edn-format/edn) reader and writer that uses
JSON for the transport format. This should be fast in the browser.

## Install

Artifacts are published on [Clojars](http://clojars.org/tailrecursion/cljson).

Leiningen:
```clojure
[tailrecursion/cljson "0.1.0-SNAPSHOT"]
```

Maven:
```xml
<dependency>
  <groupId>tailrecursion</groupId>
  <artifactId>cljson</artifactId>
  <version>0.1.0-SNAPSHOT</version>
</dependency>
```

## Usage

Cljson transforms Clojure data to and from the restricted set of types which can
be encoded as JSON. The resulting JSON can be passed back and forth between a
serverside Clojure application and the ClojureScript running in a browser without
needing to use `#'read-string` or `#'pr-str`, which are slow in the browser.

There are two functions exported by this library: `clj->cljson` and `cljson->clj`.
They convert Clojure data to and from JSON strings in the Clojure library, and to
and from native JavaScript primitives which can be encoded as JSON in the ClojureScript
library.

## License

Copyright © 2013 FIXME

Distributed under the Eclipse Public License, the same as Clojure.
