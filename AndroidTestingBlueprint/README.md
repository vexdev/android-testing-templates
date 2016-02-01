# Android Testing Blueprint

Issue spotted: When referencing a class from android.test.mock the following exception is produced at runtime:

```
com.example.android.testing.blueprint.test.AndroidTestOnlyModuleTest > verifyResourceString[Nexus 6 - 6.0] FAILED
	java.lang.NoClassDefFoundError: Failed resolution of: Landroid/test/mock/MockContentResolver;
	at com.example.android.testing.blueprint.test.AndroidTestOnlyModuleTest.verifyResourceString(AndroidTestOnlyModuleTest.java:54)
:module-flavor1-androidTest-only:connectedDebugAndroidTest FAILED

FAILURE: Build failed with an exception.
```

How to reproduce:

```
./gradlew module-flavor1-androidTest-only:connectedAndroidTest
```
