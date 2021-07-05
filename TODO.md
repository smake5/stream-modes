# TODO

## MVP spec

The MVP for this project is an HTML widget that possesses the features
enumerated below. The widget will be connected via a websocket to a
backend service that provides an API for cool stuff.

* mode name
    - for now, just "focus" and "vibe" mode
* timer
    - would be nice if it made a noise upon expiration so that i notice
* display arbitrary text
    - just something to provide whatever context i feel necessary
    - im thinking sometimes ill input a ! chat command that further
      explains the task and project being worked on.

* technology
    - client
        * curl
    - api backend
        * flask
            - lightweight
            - theoretically accessible to more people on twitch than ruby (disaster_robot's primary proficiency)
    - widget ui
        * vanilla js
            - the widget is a pretty minor js implementation, prob
              doesnt warrent much more than vanilla js
### MVP API spec

* POST /widget
    - Create a widget
    - Args:
        * default_mode
        * timer_enabled
        * text
* POST /widgets/:widget_uuid
    - Update a widget
    - Args:
        * text
* POST /widgets/:widget_uuid/timer/start
* POST /widgets/:widget_uuid/timer/stop

* POST /widgets/:widget_uuid/mode/:mode_uuid
    - Set the widget mode

## 1.0+ spec

* Analytics on widget state change
* Web sockets
* Automatic mode transitions