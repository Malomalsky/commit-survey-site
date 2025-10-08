## pytorch_at_check
Model: `chore(torch/csrc): Chore(torch/csrc): Replace AT_CHECK with TORCH_CHECK…`
Reference: `Change AT_CHECK to TORCH_CHECK in python_arg_parser.h`
[Model](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=pytorch_at_check&choice=model) · [Reference](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=pytorch_at_check&choice=reference) · [Tie](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=pytorch_at_check&choice=tie) · [Skip](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=pytorch_at_check&choice=skip)
Files: 1 | +1/-1
Anchors: `python_arg_parser.h`

```diff
diff --git a/torch/csrc/utils/python_arg_parser.h b/torch/csrc/utils/python_arg_parser.h
index e432b98ff235..86e990ab11ab 100644
--- a/torch/csrc/utils/python_arg_parser.h
+++ b/torch/csrc/utils/python_arg_parser.h
@@ -439,7 +439,7 @@ inline at::MemoryFormat PythonArgs::toMemoryFormat(int i) {
 
 inline at::QScheme PythonArgs::toQScheme(int i) {
   if (!args[i]) return at::kPerTensorAffine;
-  AT_CHECK(THPQScheme_Check(args[i]), "qscheme arg must be an instance of the torch.qscheme");
+  TORCH_CHECK(THPQScheme_Check(args[i]), "qscheme arg must be an instance of the torch.qscheme");
   const auto qscheme = reinterpret_cast<THPQScheme*>(args[i]);
   return qscheme->qscheme;
 }
```