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

Structure of the repo:

```
├── README.md                   // this README

├── intro                       // high level introduction asciidoc articles
├── protocols                   // protocols-related asciidoc articles and puml diagrams
│   ├── puml                    // source puml diagrams
│   └── svg                     // temp output: svg files generated from puml source diagrams, completely inlined in output htmls

├── cplx                        // original asciidoc files generated by Clearpool's https://git.clearpool.io/powertrade/powertrade_protocol
├── reference                   // cplx asciidoc files manually corrected by PowerTrade

├── root.asciidoc               // root asciidoc source file (includes all other asciidoc files and defines the structure of API documentation)
├── powertrade.css              // current CSS file

├── ws_api_spec_external.html   // output: generated EXTERNAL version
├── ws_api_spec_internal.html   // output: generated INTERNAL version
├── workspace.code-workspace    // VS Code settings etc
├── index.html                  // old file, keeping for now
```
