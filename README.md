Humanitarian Icons for QGIS
=========

**Update:** The new UNOCHA V2 icons 

These icons are based on the work of [Dan Joseph](https://github.com/danbjoseph/map-icons/) which converted the original [UNOCA Humanitarian icons](https://reliefweb.int/report/world/world-humanitarian-and-country-icons-2012) to SVG.

The XML stylesheets in the second link appear to no longer work in the latest version of QGIS. The icons in this repository have an added attribute `param(fill)` which allows QGIS to customise the fill colour of the icons.

To add these icons to QGIS click `preferences`, `system` and add the location of the icons to your SVG paths. 

Contact bmcdonald@iom.int if you with to have additional QGIS-friendly icons added

**Update:** The new UNOCHA V2 icons are added. The following Python code was used to modify the SVGs
```python
import glob
for filepath in glob.iglob('./**/*.svg', recursive=True):
    with open(filepath) as file:
        s = file.read()
    s = s.replace('<path', '<path fill="param(fill) #407CCA" ')
    with open(filepath, "w") as file:
        file.write(s)
```


