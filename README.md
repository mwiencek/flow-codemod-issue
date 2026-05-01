# flow-codemod-issue

```sh
npm install
./node_modules/.bin/flow-codemod convertLegacyUtilityTypes
```

Result:

```diff
diff --git a/A.js b/A.js
index 22527a1..b9ca39a 100644
--- a/A.js
+++ b/A.js
@@ -1,4 +1,4 @@
 // @flow
 // This is file A.js.
-type A1 = $ReadOnlyArray<mixed>;
-type A2 = $Keys<$Values<A1>>;
+type A1 = ReadonlyArray<unknown>;
+type A2 = keyof Values<A1>;
diff --git a/B.js b/B.js
index 5f887ae..fc509f1 100644
--- a/B.js
+++ b/B.js
@@ -1,4 +1,4 @@
 // @flow
 // This is file B.js.
-type B1 = $NonMaybeType<mixed>;
-type B2 = $ReadOnly<B1>;
+type A1 = ReadonlyArray<unknown>;
+type A2 = keyof Values<A1>;
diff --git a/C.js b/C.js
index 0d9a7e6..be1935e 100644
--- a/C.js
+++ b/C.js
@@ -1,4 +1,4 @@
 // @flow
 // This is file C.js.
-type C1 = $ReadOnlyMap<mixed, mixed>;
-type C2 = $ReadOnlySet<C1>;
+type A1 = ReadonlyArray<unknown>;
+type A2 = keyof Values<A1>;
```
