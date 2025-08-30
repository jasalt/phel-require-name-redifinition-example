Example of re-defined symbols in required (nested) namespaces behaving differently between `phel repl` and `phel run`.

Tested with Phel dev-main (bc9801b075d3d3f6c8eb4be337dd07dd8e0414cb), PHP 8.3.24 (cli).

See entry points for results:

- `main-requiring-one.phel`: requires module-one requiring function from module-two, `phel repl` throws exception and `phel run` has no output
- `main-requiring-two.phel`: requires the module-two function directly, seems to work as expected for bot `phel repl` and `phel run`
- `main-requiring-both.phel`: requires both modules, `phel run` behaves as with previous separate cases, `phel repl` fails now in both


The issue seems to exist previously with Phel 0.20.0 also, with `main-requiring-one.phel` having exactly same behavior with that.
