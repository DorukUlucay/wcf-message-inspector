# Classes for WCF Message Interception
Code in this repo will help you intercept outgoing request and incoming reponses working with external services.
There is a lot of articles about message inspectors but it is(https://stackoverflow.com/a/54238550/1397858) the cleanest, .net core compatible and configless. I made it a repo for my and other peoples' future use.

# Setup

## 1. Add ```LoggingEndpointBehaviour.cs``` and ```LoggingMessageInspector.cs``` to your project.
Method bodies are empty. Fill them however you want. Or just put breakpoints and view messages on fly. It's your call.

## 2. Add this code where you instantaniate WCF client:
```
    client.Endpoint.EndpointBehaviors.Add(new LoggingEndpointBehaviour(new LoggingMessageInspector()));
```
