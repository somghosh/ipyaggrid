
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
  {"version_major": 2, "version_minor": 0, "state": {"d570feaf72c94c46bdd2a44746c9e9b5": {"model_name": "AgGridModel", "model_module": "ipyaggrid", "model_module_version": "~0.2.2", "state": {"_dom_classes": [], "_grid_data_down": "H4sIAMSLOGIC/5WWQY+bMBCF/4rFqZX2YBsw0Bshu9tITRWVtDlUPUzCiEUxODKw3aja/17T7iHG\nEVmOmMmnmfF7j/z84x1Af4UavU/EY5QS2Xp3xFO6KqtmOLvvtTrhcFbD8V9V2hfV8HzS1WE48BPK\n+OsdsVDZEz6jlEjWIKt9bzO/55e8oVQriZ0F5Tzyx9D8eJagj+YlnQIu+upwtGCBCIQDg840WHU4\nhdrIc6367smeNxDOvN9wj5Lk+XaKlq6zSxCPWBCMQVvz40ZNUR6ULqx+RBg5022wL1F1JKTBrft8\nK7U6Y4kfjZGPIOGlQoOkc9rjPovDMWtVnwxttip4Ivx4zHro9ZmsVqu598ijgDp7y6Azgm0mW9uo\npqvgYC8sipMxK6330LZQKE2Kk5whDD8WceA6CoyfmhI1aSc1u1RFiRYuTEJna1lfgDEGnb01yt1J\n12YjSDLQUs13esgSR2v3bWfsSXZQqoZ8yHcf5/mdCeFILlNaNWDyyATIWCxpW8ElcavOqgNbxT5l\nY+SybzvUszcYU+5E22elm/97ea9GjEOdS13DM+q3Zbw7PqjwqRMfX0JGp3e0hK7tG2uwgLkkxnxG\nlij7FyQ5FtDciqMfSh7b31BiY4+bBM64eZouSJLgLeRQZ8NE5FzmYr0z4qb8FszU2bd5pbFHjbVJ\nkVmWj2I32Xg4L2r5le9cNv2xHDx5tiBCCMePSz4d+lcyx/TuqipgbK6qfN/8F3j99RehDgloqggA\nAA==\n", "_grid_data_up": {}, "_grid_options_mono_down": "H4sIAMSLOGIC/3WRS2/CMBCE/0rkUyshJJAq+jhVIHriIcoNcTDxJli1vdHaLm2j/PfaSUpCaX2K\nZr6deMclA8MPCqaoNmDlF7DHxJGHQcJSVF6bGWQ2aLuSZRKUCJ8MSebSsIAcgQugJddxjK0avRok\nPVjzN7hGF1G9BFPeuNcsClC/4IJk+ge6ruVqH4xmrblUDqjbqVFfkZw0eSdzIzV3sMGT7cSc0BcL\nr5x89g6ndRudKyDjwQtyaCjIJQMhXUyPF8m8SZ1Ec1Nw4trelgTOk0lO0gg8DXn+QlKsiojY3f3d\nZDwZjR7G++FPxtRbh/qpimu3D7H9LMDWPzJeH4DOF4q1tFsyni97Zrt9zHDw4f6Z2J6tHi9CHT3+\nnSsPc6TQUjt3BFUA2WEEOyNM9qNn55Q2+uyv617q7BR1bMnhRW6jQkywrArnG0CHflaqAgAA\n", "_grid_options_multi_down": [], "_id": 857271192, "_js_helpers_builtin": "H4sIAMSLOGIC/+1VUW/bNhB+z6+4h6CWA0dxNqAPzlLMcZM2wDZvs9GXYVgZ6WxroUiBR6ZJDf/3\nHinLlmV5SYEC28P4IFHid98dj98dFygLNHTlMmkzBZewPAIeqbB4o00urEUzgJlTic20ipROsbvG\n+HF2Brm4RyBnMBhBRqC0BadSnGUK0w00m0Ewh1evwL/jByHdDpkfEi2kHIbCT/CW+aIa9GIPuWBk\nGs/RvtfOUNSCyCvEz5lyFlsxVGEmmGiV7mH4J1nQsxkxeA2dZjl+1grH4W/UhRN43eexa7mzk40d\no0/XdK2envI0uLH6djKeWJOpedSNyd1ROe/34LzfsPTZ5WxcXkLfJzjfTqmcNhPth0HrjPL+dslW\nh6i7IeOdfr+z7z2vIPlByCYUaoWsw/l4vOSIVnC8XKwGx8vcP2j1cYvdhre2UE7KcnnVOwrvWdDu\nrbIDSL+Py6+o04v7s063V0PcSC2amO8CJoAyZV9SBeswNk73RbuJy/v7asoQ5WHSROeFMOhFRjXK\nGZc0mp90IqRf6kGCUn5oFh1X8JDI5WX5EjARkNUGUxDE1ayPdsXpSTxdXdlb4oujnXrfgH+ARjRN\nOa73e3peO2ZASbjL8+aFPOf/oJb+bvYo+4xTfZPZWurmJkvHhZ9S3UHtdyyKLPamIy1drigwRI2D\nEc7qCWOGUj5PXqZXSFky3qa+SP7486LVexIwQ46Be8qwsuHO5XV8LZJFVCLg8k0jQXUHceGoQnrK\n27TWVVbd51xX26uc16kbmTg7OSnJTuD6sdCG75q5F5wAq2E0+QCO/B8xP33HrsAnt8L/yNoWOSzH\nd39jYlf1WNaQs/DGwDvVI3p4abIDM20uvWrQfVa8R5GGAhWswV6jSfs9vjPaFVxu1rjGuje/0ZpV\nSq32fr2yPrD8a6b46pzq4hnElbZW562gzWG0xqiVfJqg5IRi2u7DFYVBot+cDl1ln4ILEX8ROQ6g\nkz/95b/ihB46DZoFot2iwuceRDuZ/q4/XeGEN1b4gPiGZOG2hFUYnXBUI+4HI97hnUjuB+UxeoMw\nKVtkq1l5qFtDf29sgauLg4Veaov7jRgS6ysqhfM1Gr9+5B72DVUe+P7X+b+j80dJ317n/iaejt+O\nYQDJApP7/5rug+L2lM/GXwBatMMsQwwAAA==\n", "columns_fit": "size_to_fit", "compress_data": true, "css_rules_down": [], "export_mode": "buttons", "height": "350px", "js_helpers": "H4sIAMSLOGIC/wMAAAAAAAAAAAA=\n", "js_helpers_custom": "H4sIAMSLOGIC/wMAAAAAAAAAAAA=\n", "js_post_grid": [], "js_pre_grid": [], "js_pre_helpers": [], "layout": "IPY_MODEL_aacd6e3c03bc4ee18837d8adce3785e1", "menu": {"buttons": [{"name": "Log foo 1", "action": "console.log(\"foo\");", "css": ".flex-child-log-foo-1-857271192 {\norder: 0;\nalign-self: auto;\nwidth: 150px;\nmargin: 5px;\nflex: 0.00 1.00 auto;\nfont-size: 12px;\n}\n"}, {"name": "Log bar 1", "action": "console.log(\"bar\");", "css": ".flex-child-log-bar-1-857271192 {\norder: 0;\nalign-self: auto;\nwidth: 150px;\nmargin: 5px;\nflex: 0.00 1.00 auto;\nfont-size: 12px;\n}\n"}, {"name": "Log foo 2", "action": "console.log(\"foo\");", "css": ".flex-child-log-foo-2-857271192 {\norder: 0;\nalign-self: auto;\nwidth: 150px;\nmargin: 5px;\nflex: 0.00 1.00 auto;\nfont-size: 12px;\n}\n"}, {"name": "Log foo 3", "action": "console.log(\"foo\");", "css": ".flex-child-log-foo-3-857271192 {\norder: 0;\nalign-self: auto;\nwidth: 150px;\nmargin: 5px;\nflex: 0.00 1.00 auto;\nfont-size: 12px;\n}\n"}, {"name": "Log foo 4", "action": "console.log(\"foo\");", "css": ".flex-child-log-foo-4-857271192 {\norder: 0;\nalign-self: auto;\nwidth: 150px;\nmargin: 5px;\nflex: 0.00 1.00 auto;\nfont-size: 12px;\n}\n"}, {"name": "Export to CSV", "action": "console.log(\"exporting to CSV\"); helpers.exportToCsv(gridOptions);", "css": ".flex-child-export-to-csv-857271192 {\norder: 0;\nalign-self: auto;\nwidth: 150px;\nmargin: 5px;\nflex: 0.00 1.00 auto;\nfont-size: 12px;\n}\n"}, {"name": "Export to Excel", "action": "console.log(\"exporting to Excel\"); helpers.exportToExcel(gridOptions);", "css": ".flex-child-export-to-excel-857271192 {\norder: 0;\nalign-self: auto;\nwidth: 150px;\nmargin: 5px;\nflex: 0.00 1.00 auto;\nfont-size: 12px;\n}\n"}, {"name": "Export Grid", "action": "exportFunc.exportGrid(gridOptions, view, parseInt(inputAggregationLevel.value, 10))", "container_css": ".flex-child-container-export-grid-857271192 {\norder: 0;\nalign-self: auto;\nwidth: 150px;\nmargin: 5px;\nflex: 0.00 1.00 auto;\n}\n", "css": ".flex-child-export-grid-857271192 {\norder: 0;\nalign-self: auto;\nflex: 0.00 1.00 auto;\nfont-size: 12px;\n}\n"}], "inputs": [{"name": "Quick Filter", "css": ".flex-child-quick-filter-857271192 {\norder: 0;\nalign-self: auto;\nmargin: 5px;\nflex: 0.00 1.00 auto;\nwidth: 150px;\n}\n"}, {"name": "Toggle Edit", "css": ".flex-child-toggle-edit-857271192 {\norder: 0;\nalign-self: auto;\nmargin: 5px;\nflex: 0.00 1.00 auto;\n}\n"}, {"name": "Toggle Delete", "css": ".flex-child-toggle-delete-857271192 {\norder: 0;\nalign-self: auto;\nmargin: 5px;\nflex: 0.00 1.00 auto;\n}\n"}], "button_div_css": ".flex-button-div-857271192 {\ndisplay: flex;\njustify-content: flex-start;\nalign-items: flex-start;\nalign-content: flex-start;\nflex-flow: row wrap;\n}\n", "input_div_css": ".flex-input-div-857271192 {\ndisplay: flex;\njustify-content: flex-start;\nalign-items: baseline;\nalign-content: flex-start;\nflex-flow: row wrap;\n}\n", "menu_div_css": ".flex-menu-div-857271192 {\ndisplay: flex;\njustify-content: flex-start;\nalign-items: flex-start;\nalign-content: flex-start;\nflex-flow: row wrap;\n}\n"}, "show_toggle_delete": true, "show_toggle_edit": true, "theme": "ag-theme-balham", "user_params": {}}}, "aacd6e3c03bc4ee18837d8adce3785e1": {"model_name": "LayoutModel", "model_module": "@jupyter-widgets/base", "model_module_version": "1.2.0", "state": {}}}}
</script>
<div id="embed-grid-857271192">
  <!-- This script tag will be replaced by the views DOM tree -->
  <script type="application/vnd.jupyter.widget-view+json">
    {"version_major": 2, "version_minor": 0, "model_id": "d570feaf72c94c46bdd2a44746c9e9b5"}
  </script>
</div>
    '
        height="480"
        width="100%"
        frameborder="0"
      ></iframe>
  </div>
</template>

<script>
export default {
  name: 'example-custom-menu-1',
  data() {return {}}
}
</script>
