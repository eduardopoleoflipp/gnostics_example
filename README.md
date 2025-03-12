# gnostic-buf-demo
This demo shows an example on how to add use gnostics with buf. It also shows the most relevant annotations that we'll need to use within the platform domains.

## Usage
`buf generate --path=protos/test_services.proto ` generate the openapi.yaml file.

## Issues
Gnostics does not provide a perfect translations here are some issues I noticed:
- We can't have a ref under the description cuz description is only a string. (Minor)
- By default gnostics will add a tag with the name of the service in this case Messaging1 which messes up readme. Ideally we would only want the tags defined in here. (Top)
- Can't override default responses using operation level annotations (Medium)
- Can't handle oneof (Top)
- The library is abandoned. (Medium. It looks like we either write it ourselves or take over an abandoned one so there's not much of a choice)