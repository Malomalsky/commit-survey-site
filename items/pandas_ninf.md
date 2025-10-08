## pandas_ninf
Model: `refactor: Rename Np.NINF to -np.inf`
Reference: `ENH: Remove NINF and PINF usages (#54468)`
[Model](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=pandas_ninf&choice=model) · [Reference](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=pandas_ninf&choice=reference) · [Tie](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=pandas_ninf&choice=tie) · [Skip](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=pandas_ninf&choice=skip)
Files: 0 | +4/-4
Anchors: `MINfloat32`, `MINfloat64`, `float32_t`, `float64_t`, `np.inf`

```diff
@@ -51,8 +51,8 @@ cdef extern from "pandas/skiplist.h":
     int skiplist_min_rank(skiplist_t*, double) nogil
 
 cdef:
-    float32_t MINfloat32 = np.NINF
-    float64_t MINfloat64 = np.NINF
+    float32_t MINfloat32 = -np.inf
+    float64_t MINfloat64 = -np.inf
 
     float32_t MAXfloat32 = np.inf
     float64_t MAXfloat64 = np.inf
@@ -805,7 +805,7 @@ def test_empty_like(self):
     complex("inf"),
     complex("-inf"),
     np.inf,
-    np.NINF,
+    -np.inf,
 ]
 
 int_na_vals = [
@@ -393,7 +393,7 @@ def test_frame_read_json_dtype_missing_value(self, dtype):
 
         tm.assert_frame_equal(result, expected)
 
-    @pytest.mark.parametrize("inf", [np.inf, np.NINF])
+    @pytest.mark.parametrize("inf", [np.inf, -np.inf])
     @pytest.mark.parametrize("dtype", [True, False])
     def test_frame_infinity(self, inf, dtype):
         # infinities get mapped to nulls which get mapped to NaNs during
```