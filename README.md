```
➜  rules_js-1p-peer-dep git:(main) ✗ bazel build //...
INFO: Analyzed 3 targets (0 packages loaded, 0 targets configured).
ERROR: /Users/john/figma/rules_js-1p-peer-dep/app/BUILD.bazel:6:11: Transpiling & type-checking TypeScript project @@//app:ts [tsc -p app/tsconfig.json] failed: (Exit 2): tsc.sh failed: error executing TsProject command (from target //app:ts) bazel-out/darwin_arm64-opt-exec-ST-13d3ddad9198/bin/external/aspect_rules_ts~2.1.1~ext~npm_typescript/tsc.sh --project app/tsconfig.json --outDir app --rootDir app --declarationDir app

Use --sandbox_debug to see verbose messages from the sandbox and retain the sandbox build root for debugging
node_modules/.aspect_rules_js/component-lib@0.0.0/node_modules/component-lib/component.d.ts(1,19): error TS2307: Cannot find module 'react' or its corresponding type declarations.
Use --verbose_failures to see the command lines of failed build steps.
INFO: Elapsed time: 1.166s, Critical Path: 1.04s
INFO: 2 processes: 2 internal.
ERROR: Build did NOT complete successfully
```

Expected result: builds successfully.
