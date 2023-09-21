# docker-image-tika-test
Test docker image for tika support the filesystem strategy

## Usage
You can request the file either via header or via get parameters. If you use the get parameter you should URL encode the value.
```
PUT http://localhost:9998/tika/text
fetcherName: fsf
fetchKey: dummy.pdf

PUT http://localhost:9998/tika/text?fetcherName=fsf&fetchKey=dummy.pdf
```