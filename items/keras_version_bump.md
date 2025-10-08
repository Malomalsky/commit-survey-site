## keras_version_bump
Model: `refactor(keras): Rename 2.8.0 to 2.9.0`
Reference: `Bump the keras version from 2.8 to 2.9 on head...`
[Model](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=keras_version_bump&choice=model) · [Reference](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=keras_version_bump&choice=reference) · [Tie](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=keras_version_bump&choice=tie) · [Skip](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=keras_version_bump&choice=skip)
Files: 2 | +2/-2
Anchors: `pip_package`, `init__.py`, `setup.py`, `VERSION`

```diff
diff --git a/keras/__init__.py b/keras/__init__.py
index 9801ae029fa3..e75c182e5367 100644
--- a/keras/__init__.py
+++ b/keras/__init__.py
@@ -30,6 +30,6 @@
 
 from tensorflow.python.util.tf_export import keras_export
 
-__version__ = '2.8.0'
+__version__ = '2.9.0'
 
 keras_export('keras.__version__').export_constant(__name__, '__version__')
diff --git a/keras/tools/pip_package/setup.py b/keras/tools/pip_package/setup.py
index d830bb476451..6ee067e0dd4d 100644
--- a/keras/tools/pip_package/setup.py
+++ b/keras/tools/pip_package/setup.py
@@ -30,7 +30,7 @@
 # This version string is semver compatible, but incompatible with pip.
 # For pip, we will remove all '-' characters from this string, and use the
 # result for pip.
-_VERSION = '2.8.0'
+_VERSION = '2.9.0'
 
 REQUIRED_PACKAGES = [
     # We depend on TensorFlow's declared pip dependencies.
```