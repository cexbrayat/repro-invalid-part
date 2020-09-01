# Repro

With ascidoctor-epub alpha.18, this document throws:
```
asciidoctor: ERROR: main.adoc: line 17: invalid part, must have at least one section (e.g., chapter, appendix, etc.)
```

It does emit the epub with no visible issue, but the ERROR is intriguing.

To reproduce, you can use the latest docker-asciidoctor image:

```
docker run -it -v $PWD:/documents/ asciidoctor/docker-asciidoctor asciidoctor -b epub3 -r asciidoctor-epub3 main.adoc
```

With an older asciidocto-epub version, this works without logging this error.
