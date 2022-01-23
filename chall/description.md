Help check how secure our latest PaaS (Pdftohtml-as-a-Service) is!

<!-- meme here plz -->

Pick your favorite bug from
[this bloody list](https://gitlab.freedesktop.org/poppler/poppler/-/commits/master/poppler/JBIG2Stream.cc),
or really, just exploit *that bug* so your exploit would also work on latest Poppler [1] and maybe even KItinerary.

The container image is also available on [Docker Hub](https://hub.docker.com/hsogroupie/pdftohtml).

[1] Yeah, turns out propagating bug fixes between different Clone-and-Own codebases takes time :)

```
socat -t90 stdio tcp-connect:$DEPLOY_IP:31337
```
