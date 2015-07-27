# itzsoikot
so simple
https://itzsoikot.wordpress.com

# Install lein2
    # https://github.com/technomancy/leiningen

    $ lein new insane-noises

    # add the following dependencies to insane-noises/project.clj
    # [org.clojure/clojure "1.5.1"]
    # [overtone "0.9.1"]

    $ cd insane-noises
    $ lein repl
    
        ;; boot the server
    user=> (use 'overtone.live)

    ;; listen to the joys of a simple sine wave
    user=> (demo (sin-osc))

    ;; or something more interesting...
    user=>(demo 7 (lpf (mix (saw [50 (line 100 1600 5) 101 100.5]))
                  (lin-lin (lf-tri (line 2 20 5)) -1 1 400 4000)))
