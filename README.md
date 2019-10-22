# Classes for WCF Message Interception
Code in this repo will help you intercept outgoing requests and incoming reponses working with external services.

## Why the repo
There is a lot of articles about message inspectors but it is(https://stackoverflow.com/a/54238550/1397858) the cleanest, .net core compatible and configless. I made it a repo for my and other peoples' future use.

## Setup

### 1. Add Classes To Your Project Where You Make WCF call
Add the files [```LoggingEndpointBehaviour.cs```](LoggingEndpointBehaviour.cs) and [```LoggingMessageInspector.cs```](LoggingMessageInspector.cs) to your project.

Method bodies are empty. Fill them however you want. Or just put breakpoints and view messages on fly. It's your call.

### 2. Add this code between where you instantaniate WCF client and make the call
```
    client.Endpoint.EndpointBehaviors.Add(new LoggingEndpointBehaviour(new LoggingMessageInspector()));
```
That's all. It must be working now. If not, open an issue.

## Contributions are welcome
If you have ideas to make it better open an issue or just send pr. Some ideas:
* Make it a library
  * Make it a nuget package
* Add log appenders
* Fix/add more info to read me
