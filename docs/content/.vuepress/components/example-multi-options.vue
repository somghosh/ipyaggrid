
<template>
  <div class="example-ipyaggrid">
      <iframe 
        srcdoc='<!-- Load RequireJS, used by the IPywidgets for dependency management -->
<script 
  src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.3.4/require.min.js" 
  integrity="sha256-Ae2Vz/4ePdIu6ZyI/5ZGsYnb+m0JlOmKPjt6XZ9JJkA=" 
  crossorigin="anonymous">
</script>

<!-- Load IPywidgets bundle for embedding. -->
<script 
  src="https://unpkg.com/@jupyter-widgets/html-manager@*/dist/embed-amd.js" 
  crossorigin="anonymous">
</script>
<!-- The state of all the widget models on the page -->
<script type="application/vnd.jupyter.widget-state+json">
  {"version_major": 2, "version_minor": 0, "state": {"04181aedf063463f9b4559b2dd9d1aab": {"model_name": "AgGridModel", "model_module": "ipyaggrid", "model_module_version": "~0.2.2", "state": {"_dom_classes": [], "_grid_data_down": "H4sIAMSLOGIC/5WWQY+bMBCF/4rFqZX2YBsw0Bshu9tITRWVtDlUPUzCiEUxODKw3aja/17T7iHG\nEVmOmMmnmfF7j/z84x1Af4UavU/EY5QS2Xp3xFO6KqtmOLvvtTrhcFbD8V9V2hfV8HzS1WE48BPK\n+OsdsVDZEz6jlEjWIKt9bzO/55e8oVQriZ0F5Tzyx9D8eJagj+YlnQIu+upwtGCBCIQDg840WHU4\nhdrIc6367smeNxDOvN9wj5Lk+XaKlq6zSxCPWBCMQVvz40ZNUR6ULqx+RBg5022wL1F1JKTBrft8\nK7U6Y4kfjZGPIOGlQoOkc9rjPovDMWtVnwxttip4Ivx4zHro9ZmsVqu598ijgDp7y6Azgm0mW9uo\npqvgYC8sipMxK6330LZQKE2Kk5whDD8WceA6CoyfmhI1aSc1u1RFiRYuTEJna1lfgDEGnb01yt1J\n12YjSDLQUs13esgSR2v3bWfsSXZQqoZ8yHcf5/mdCeFILlNaNWDyyATIWCxpW8ElcavOqgNbxT5l\nY+SybzvUszcYU+5E22elm/97ea9GjEOdS13DM+q3Zbw7PqjwqRMfX0JGp3e0hK7tG2uwgLkkxnxG\nlij7FyQ5FtDciqMfSh7b31BiY4+bBM64eZouSJLgLeRQZ8NE5FzmYr0z4qb8FszU2bd5pbFHjbVJ\nkVmWj2I32Xg4L2r5le9cNv2xHDx5tiBCCMePSz4d+lcyx/TuqipgbK6qfN/8F3j99RehDgloqggA\nAA==\n", "_grid_data_up": {}, "_grid_options_mono_down": "H4sIAMSLOGIC/wMAAAAAAAAAAAA=\n", "_grid_options_multi_down": [["Sorting, color, filter", "H4sIAMSLOGIC/3WQy07DMBBFf8XyJiCVKoJdkWCRqjtKBd0hFlNnklj4EfmBgCj/ju20IX2QVXTu\nnZPJdJRp4aVaYmXpgrx1tOIoyvBKteE1V3RGaINQolmDxMifB97PyKQs4QPPq0+RHhcZDOl5V5co\nTsqt4exCdXPADIUoBNi4Oq28Yo5rddWCAWmvSUcMOm8UGcD8E4RH8nB3m+c5eSRZst80vG4ysiBZ\ndk962r8HLSrYCXzVxnFVB7UzHke84sKhOaWFFi9o+U/crwJhYzJcdvvdYtyvo8rLHZoi0QSqg4pC\nvZ6E+0+EW1CHX+6fie0YTfolOJz00y+vtJHg9nMNihaNncfiXxAmp+rlaNmrx3yTTpncTMt4WKeP\nvAPFaLC0D88ve3wkUWICAAA=\n"], ["Selection, grouping, no-filter", "H4sIAMSLOGIC/3WQzW6DMBCEXwX5HPUBek2UnppGTW5RDxsYiNU1tha7f4h3rw2UQNP65P1mdla7\nrcotB1NvUDbqPju1qtTgIn6VFV3pWq0ydQEVkB0ZJP505bpIxEtArMS+P4gNbiTdKpuFGXrFbdRj\noktjToN667UF+JfZic7/sO573L1EATWdGQcrXtdV1EriBhPfavaQG7y2/IxGfy2XO4CRe23rfp/A\nXjvuhw8XPH46pBO2qg7mDFn3tAflzxhF1W4mjuPjTsrjw//TcZykmb8gj5n/jThga8WQH/suYAdp\n7pLxKsTOefRmShmjJ31PQmZYJ7fGxcrbRe5AkRIa1cX3DYKjUAlKAgAA\n"]], "_id": 90702902, "_is_grid_options_multi": true, "_js_helpers_builtin": "H4sIAMSLOGIC/+1VUW/bNhB+z6+4h6CWA0dxNqAPzlLMcZM2wDZvs9GXYVgZ6WxroUiBR6ZJDf/3\nHinLlmV5SYEC28P4IFHid98dj98dFygLNHTlMmkzBZewPAIeqbB4o00urEUzgJlTic20ipROsbvG\n+HF2Brm4RyBnMBhBRqC0BadSnGUK0w00m0Ewh1evwL/jByHdDpkfEi2kHIbCT/CW+aIa9GIPuWBk\nGs/RvtfOUNSCyCvEz5lyFlsxVGEmmGiV7mH4J1nQsxkxeA2dZjl+1grH4W/UhRN43eexa7mzk40d\no0/XdK2envI0uLH6djKeWJOpedSNyd1ROe/34LzfsPTZ5WxcXkLfJzjfTqmcNhPth0HrjPL+dslW\nh6i7IeOdfr+z7z2vIPlByCYUaoWsw/l4vOSIVnC8XKwGx8vcP2j1cYvdhre2UE7KcnnVOwrvWdDu\nrbIDSL+Py6+o04v7s063V0PcSC2amO8CJoAyZV9SBeswNk73RbuJy/v7asoQ5WHSROeFMOhFRjXK\nGZc0mp90IqRf6kGCUn5oFh1X8JDI5WX5EjARkNUGUxDE1ayPdsXpSTxdXdlb4oujnXrfgH+ARjRN\nOa73e3peO2ZASbjL8+aFPOf/oJb+bvYo+4xTfZPZWurmJkvHhZ9S3UHtdyyKLPamIy1drigwRI2D\nEc7qCWOGUj5PXqZXSFky3qa+SP7486LVexIwQ46Be8qwsuHO5XV8LZJFVCLg8k0jQXUHceGoQnrK\n27TWVVbd51xX26uc16kbmTg7OSnJTuD6sdCG75q5F5wAq2E0+QCO/B8xP33HrsAnt8L/yNoWOSzH\nd39jYlf1WNaQs/DGwDvVI3p4abIDM20uvWrQfVa8R5GGAhWswV6jSfs9vjPaFVxu1rjGuje/0ZpV\nSq32fr2yPrD8a6b46pzq4hnElbZW562gzWG0xqiVfJqg5IRi2u7DFYVBot+cDl1ln4ILEX8ROQ6g\nkz/95b/ihB46DZoFot2iwuceRDuZ/q4/XeGEN1b4gPiGZOG2hFUYnXBUI+4HI97hnUjuB+UxeoMw\nKVtkq1l5qFtDf29sgauLg4Veaov7jRgS6ysqhfM1Gr9+5B72DVUe+P7X+b+j80dJ317n/iaejt+O\nYQDJApP7/5rug+L2lM/GXwBatMMsQwwAAA==\n", "columns_fit": "size_to_fit", "compress_data": true, "css_rules_down": [".number-cell {text-align: left;}", ".price-high {color: red;}"], "export_mode": "disabled", "height": "350px", "js_helpers": "H4sIAMSLOGIC/wMAAAAAAAAAAAA=\n", "js_helpers_custom": "H4sIAMSLOGIC/wMAAAAAAAAAAAA=\n", "js_post_grid": [], "js_pre_grid": [], "js_pre_helpers": [], "layout": "IPY_MODEL_f77f5e03c99142f4b730da1f79b4414b", "menu": {"buttons": [], "inputs": [{"name": "Dropdown Menu", "css": ".flex-child-dropdown-menu-90702902 {\norder: 0;\nalign-self: auto;\nmargin: 5px;\nflex: 0.00 1.00 auto;\nwidth: 150px;\n}\n"}], "button_div_css": ".flex-button-div-90702902 {\ndisplay: flex;\njustify-content: flex-start;\nalign-items: flex-start;\nalign-content: flex-start;\nflex-flow: row wrap;\n}\n", "input_div_css": ".flex-input-div-90702902 {\ndisplay: flex;\njustify-content: flex-start;\nalign-items: baseline;\nalign-content: flex-start;\nflex-flow: row wrap;\n}\n", "menu_div_css": ".flex-menu-div-90702902 {\ndisplay: flex;\njustify-content: flex-start;\nalign-items: flex-start;\nalign-content: flex-start;\nflex-flow: row wrap;\n}\n"}, "quick_filter": false, "theme": "ag-theme-balham", "user_params": {}}}, "f77f5e03c99142f4b730da1f79b4414b": {"model_name": "LayoutModel", "model_module": "@jupyter-widgets/base", "model_module_version": "1.2.0", "state": {}}}}
</script>
<div id="embed-grid-90702902">
  <!-- This script tag will be replaced by the views DOM tree -->
  <script type="application/vnd.jupyter.widget-view+json">
    {"version_major": 2, "version_minor": 0, "model_id": "04181aedf063463f9b4559b2dd9d1aab"}
  </script>
</div>
    '
        height="410"
        width="100%"
        frameborder="0"
      ></iframe>
  </div>
</template>

<script>
export default {
  name: 'example-multi-options',
  data() {return {}}
}
</script>
