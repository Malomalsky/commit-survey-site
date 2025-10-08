## use_projects_typos
Model: `test(testsjs): Add Tests for Duplicates/results`
Reference: `typos in useProjects / useTeams tests (#30042)`
[Model](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=use_projects_typos&choice=model) · [Reference](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=use_projects_typos&choice=reference) · [Tie](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=use_projects_typos&choice=tie) · [Skip](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=use_projects_typos&choice=skip)
Files: 2 | +2/-2

```diff
diff --git a/tests/js/spec/utils/useProjects.spec.tsx b/tests/js/spec/utils/useProjects.spec.tsx
@@ -47,7 +47,7 @@ describe('useProjects', function () {
-    // de-duplicates itesm in the query results
+    // de-duplicates items in the query results
     mockRequest.mockClear();
     await act(() => onSearch('test'));
 });
diff --git a/tests/js/spec/utils/useTeams.spec.tsx b/tests/js/spec/utils/useTeams.spec.tsx
@@ -47,7 +47,7 @@ describe('useTeams', function () {
-    // de-duplicates itesm in the query results
+    // de-duplicates items in the query results
     mockRequest.mockClear();
     await act(() => onSearch('test'));
 });
```