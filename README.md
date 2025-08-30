Example of re-defined symbols in required (nested) namespaces behaving differently between `phel repl` and `phel run`.
Tested with Phel dev-main (bc9801b075d3d3f6c8eb4be337dd07dd8e0414cb), PHP 8.3.24 (cli).

This commit has `module-two.phel` changed to not redefine core `get` which seems to fix the different behavior between repl and run.
