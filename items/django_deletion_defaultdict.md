## django_deletion_defaultdict
Model: `refactor(django/db): Counter defaultdict partial`
Reference: `Used defaultdict in deletion.Collector.`
[Model](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=django_deletion_defaultdict&choice=model) · [Reference](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=django_deletion_defaultdict&choice=reference) · [Tie](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=django_deletion_defaultdict&choice=tie) · [Skip](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=django_deletion_defaultdict&choice=skip)
Files: 1 | +12/-13
Anchors: `Counter`, `self.data`, `self.field_updates`

```diff
diff --git a/django/db/models/deletion.py b/django/db/models/deletion.py
@@
-from collections import Counter
+from collections import Counter, defaultdict
+from functools import partial
@@
-        # Initially, {model: {instances}}, later values become lists.
-        self.data = {}
-        self.field_updates = {}
+        # Initially, {model: {instances}}, later values become lists.
+        self.data = defaultdict(set)
+        self.field_updates = defaultdict(partial(defaultdict, set))
@@
-        # {model: {models}}
-        self.dependencies = {}
+        # {model: {models}}
+        self.dependencies = defaultdict(set)
@@
-        instances = self.data.setdefault(model, set())
+        instances = self.data[model]
@@
-            self.dependencies.setdefault(
-                source._meta.concrete_model, set()
-            ).add(model._meta.concrete_model)
+            self.dependencies[source._meta.concrete_model].add(
+                model._meta.concrete_model
+            )
@@
-        self.field_updates.setdefault(
-            model, {}
-        ).setdefault((field, value), set()).update(objs)
+        self.field_updates[model][field, value].update(objs)
```