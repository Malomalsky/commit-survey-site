## pandas_docs_reference
Model: `docs(doc/source): Document House/compares`
Reference: `Fixes non-existent doc/source/api.rst issue (#31280)`
[Model](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=pandas_docs_reference&choice=model) · [Reference](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=pandas_docs_reference&choice=reference) · [Tie](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=pandas_docs_reference&choice=tie) · [Skip](https://script.google.com/macros/s/AKfycbwr_vEK2da4tzmnJy-LHrKdu90GrZlfblXpNmwskDrR3w4BxMHWEJxRIqw9VPyPSgCz/exec?id=pandas_docs_reference&choice=skip)
Files: 1 | +7/-6
Anchors: `Sphinx`, `API`, `Every`, `Reference`, `api.html`, `methods.This`, `pandas.pydata.org`

```diff
diff --git a/doc/source/development/contributing.rst b/doc/source/development/contributing.rst
@@
-* Our API documentation in ``doc/source/api.rst`` houses the auto-generated
+* Our API documentation files in ``doc/source/reference`` house the auto-generated
   documentation from the docstrings. For classes, there are a few subtleties around
   controlling which methods and attributes have pages auto-generated.
@@
-Every method should be included in a ``toctree`` in ``api.rst``, else Sphinx will
+Every method should be included in a ``toctree`` in one of the documentation files in
+``doc/source/reference``, else Sphinx will
   emit a warning.
@@
-The summary also compares the list of methods documented in ``doc/source/api.rst``
-(which is used to generate the `API Reference <https://pandas.pydata.org/pandas-docs/stable/api.html>`_ page)
-and the actual public methods. This will identify methods documented in ``doc/source/api.rst``
-that are not actually class methods, and existing methods that are not documented in ``doc/source/api.rst``.
+The summary also compares the list of methods documented in the files in ``doc/source/reference``
+(which is used to generate the `API Reference <https://pandas.pydata.org/pandas-docs/stable/api.html>`_ page)
+and the actual public methods. This will identify methods documented in ``doc/source/reference``
+that are not actually class methods, and existing methods that are not documented in ``doc/source/reference``.
```