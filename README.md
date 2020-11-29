# PowerTrade API Docs

These API docs are a preview for the unreleased PowerTrade test environment. They are provided as a directional reference for early partners and are likely to change frequently without update or warning until a test environment is released.

Make sure to have/install:

- Java with correct values in $JAVA_HOME, $PATH;
- asciidoctor with extentions;

To generate EXTERNAL VERSION (under /api-docs directory):

```
$ asciidoctor -v -w -r asciidoctor-diagram root.asciidoc -a for_internal_use@=false -o ws_api_spec_external.html
```

To generate INTERNAL VERSION (under /api-docs directory):

```
$ asciidoctor -v -w -r asciidoctor-diagram root.asciidoc -a for_internal_use@=true -o ws_api_spec_internal.html
```
