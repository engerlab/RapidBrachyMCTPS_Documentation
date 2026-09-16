# Scripting

RapidBrachyMCTPS supports scripting through the **Python Console**, powered by the [BrachyUtils](https://github.com/engerlab/brachyutils) library. Familiarity with BrachyUtils is recommended before using this feature; documentation is available [here](https://engerlab.github.io/brachyutils/brachyutils.html).

From the Python Console ![python_console](img/python_console.png){ width="25" }, access the `brachyplan` object with:

```python
>>> slicer.modules.RapidBrachyWidget.logic.brachyplan
```

All other BrachyUtils objects and methods are accessible from the console; tab completion is available to help explore them.