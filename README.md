# Phog Edge Service

A NodeJS service that runs locally and provices HTTP & web-socket interfaces for either desktop or web-applications.

It is intended to be run via `npx` but facility is provided for compiling via `nexe`.


## HTTP

GET `/command/:name/:value`
POST `/command` `{name: 'cmd_name', value: <cmd_value>}`
ALL `/feedback/:name`


## WS

`/feedback` ~ listens for any new feedback values
`/command` ~ listens for any relevant commands the have been posted


## Security

The app is started with a CLI arg for api-key=XXX which must be matched by any application accessing it.
i.e. the api-key accompanies any request made to this service.
