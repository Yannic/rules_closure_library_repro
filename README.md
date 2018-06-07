# Repro for rules_closure

This provides a repro case for
https://groups.google.com/forum/#!topic/closure-rules-discuss/8bwlPD8G6wY.

This repo contains a vendored version of `closure-library`. To demonstrate what
will happen when files are missing in the vendored version, the
deprecated `goog.result.*` was removed. See https://github.com/google/closure-library/commit/b863d8ece6dfdbdc6a62a7df4452d52bb1fdad8d for an real-world example of the
removal of deprecated code.

## Build

```
bazel test @io_bazel_rules_closure//closure/protobuf/...
```
