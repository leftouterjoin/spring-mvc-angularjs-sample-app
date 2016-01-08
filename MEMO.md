## ■.bowerrc proxy setting

```bash
$ git diff .bowerrc
diff --git a/.bowerrc b/.bowerrc
index 31fdd63..df2748b 100644
--- a/.bowerrc
+++ b/.bowerrc
@@ -1,3 +1,5 @@
 {
-    "directory" : "src/main/webapp/resources/bower_components"
-}
\ No newline at end of file
+    "directory" : "src/main/webapp/resources/bower_components",
+    "proxy" : "http://cihost:3128",
+    "https-proxy" : "http://cihost:3128"
+}
```

## ■Installing frontend dependencies

```bash
bower install
```

## ■動作確認

```bash
source setinv.sh
mvn clean install tomcat7:run-war -Dspring.profiles.active=test
```

## ■Eclipsefy

```bash
mvn eclipse:eclipse -Dwtpversion=2.0
```

Eclipseでインポート

## ■Run setting

* Project Property
	* Web Project Setting: /
	* Debug|Run Configurations -> Arguments -> VM arguments: -Dspring.profiles.active=test


