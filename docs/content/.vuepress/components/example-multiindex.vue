
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
  {"version_major": 2, "version_minor": 0, "state": {"ae361f840913450e9195a45efd4281f2": {"model_name": "AgGridModel", "model_module": "ipyaggrid", "model_module_version": "~0.2.2", "state": {"_dom_classes": [], "_grid_data_down": "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\n", "_grid_data_up": {}, "_grid_options_mono_down": "H4sIAMSLOGIC/7WUTW/CMAyG/wrKGSYNOHHbhph2QRNCO2zi4FJDI6VNlI8BQ/z3JU3o2rVlMLae\nGtvvk7x20z1ZcmbSbIwrRUadtz1ZUWSxfSUzvnmKt71b0u2QBCFGOYUUQ4YeM5JvHiU3wsa1NHjo\nduqIfiuify5i0IoYnIsYtiKGbQjbm2Mp1NV3LrRMKIslZr55JUEEsi6598GqqDgo9Kyo9wGiLnz1\nQb0T+TIzaYTyIR8dqboNENoEoScgi++OV5zXERMfbDVgRdcbyCG/MFCzEDVM4IehJU1DS054jmy/\nk2s9Bwg2QfBCyK4JsvvnyUd/MfkAubgLbvILm1VGCIlK+fgLldoAowo05Vm41rYKM4gYzqrX3TnL\nVXO7g/sT7qt7jPJzMo0y/0TX01Jy4uMHdz7c6hbFvEiV6mPQWKp/B2ZwwmUKOugSZAKlunGFXwmr\nLKPHBSWgi/wzSEi9nSVPhV1pXuH6KDqCIgf7fAKYCc9TEQYAAA==\n", "_grid_options_multi_down": [], "_id": 436924556, "_js_helpers_builtin": "H4sIAMSLOGIC/+1VUW/bNhB+z6+4h6CWA0dxNqAPzlLMcZM2wDZvs9GXYVgZ6WxroUiBR6ZJDf/3\nHinLlmV5SYEC28P4IFHid98dj98dFygLNHTlMmkzBZewPAIeqbB4o00urEUzgJlTic20ipROsbvG\n+HF2Brm4RyBnMBhBRqC0BadSnGUK0w00m0Ewh1evwL/jByHdDpkfEi2kHIbCT/CW+aIa9GIPuWBk\nGs/RvtfOUNSCyCvEz5lyFlsxVGEmmGiV7mH4J1nQsxkxeA2dZjl+1grH4W/UhRN43eexa7mzk40d\no0/XdK2envI0uLH6djKeWJOpedSNyd1ROe/34LzfsPTZ5WxcXkLfJzjfTqmcNhPth0HrjPL+dslW\nh6i7IeOdfr+z7z2vIPlByCYUaoWsw/l4vOSIVnC8XKwGx8vcP2j1cYvdhre2UE7KcnnVOwrvWdDu\nrbIDSL+Py6+o04v7s063V0PcSC2amO8CJoAyZV9SBeswNk73RbuJy/v7asoQ5WHSROeFMOhFRjXK\nGZc0mp90IqRf6kGCUn5oFh1X8JDI5WX5EjARkNUGUxDE1ayPdsXpSTxdXdlb4oujnXrfgH+ARjRN\nOa73e3peO2ZASbjL8+aFPOf/oJb+bvYo+4xTfZPZWurmJkvHhZ9S3UHtdyyKLPamIy1drigwRI2D\nEc7qCWOGUj5PXqZXSFky3qa+SP7486LVexIwQ46Be8qwsuHO5XV8LZJFVCLg8k0jQXUHceGoQnrK\n27TWVVbd51xX26uc16kbmTg7OSnJTuD6sdCG75q5F5wAq2E0+QCO/B8xP33HrsAnt8L/yNoWOSzH\nd39jYlf1WNaQs/DGwDvVI3p4abIDM20uvWrQfVa8R5GGAhWswV6jSfs9vjPaFVxu1rjGuje/0ZpV\nSq32fr2yPrD8a6b46pzq4hnElbZW562gzWG0xqiVfJqg5IRi2u7DFYVBot+cDl1ln4ILEX8ROQ6g\nkz/95b/ihB46DZoFot2iwuceRDuZ/q4/XeGEN1b4gPiGZOG2hFUYnXBUI+4HI97hnUjuB+UxeoMw\nKVtkq1l5qFtDf29sgauLg4Veaov7jRgS6ysqhfM1Gr9+5B72DVUe+P7X+b+j80dJ317n/iaejt+O\nYQDJApP7/5rug+L2lM/GXwBatMMsQwwAAA==\n", "columns_fit": "auto", "compress_data": true, "css_rules_down": [], "export_mode": "disabled", "height": "350px", "js_helpers": "H4sIAMSLOGIC/wMAAAAAAAAAAAA=\n", "js_helpers_custom": "H4sIAMSLOGIC/wMAAAAAAAAAAAA=\n", "js_post_grid": [], "js_pre_grid": [], "js_pre_helpers": [], "layout": "IPY_MODEL_83e881e519ed4466951a77e7c0461ae1", "menu": {"buttons": [], "inputs": [], "button_div_css": ".flex-button-div-436924556 {\ndisplay: flex;\njustify-content: flex-start;\nalign-items: flex-start;\nalign-content: flex-start;\nflex-flow: row wrap;\n}\n", "input_div_css": ".flex-input-div-436924556 {\ndisplay: flex;\njustify-content: flex-start;\nalign-items: baseline;\nalign-content: flex-start;\nflex-flow: row wrap;\n}\n", "menu_div_css": ".flex-menu-div-436924556 {\ndisplay: flex;\njustify-content: flex-start;\nalign-items: flex-start;\nalign-content: flex-start;\nflex-flow: row wrap;\n}\n"}, "quick_filter": false, "theme": "ag-theme-fresh", "user_params": {}}}, "83e881e519ed4466951a77e7c0461ae1": {"model_name": "LayoutModel", "model_module": "@jupyter-widgets/base", "model_module_version": "1.2.0", "state": {}}}}
</script>
<div id="embed-grid-436924556">
  <!-- This script tag will be replaced by the views DOM tree -->
  <script type="application/vnd.jupyter.widget-view+json">
    {"version_major": 2, "version_minor": 0, "model_id": "ae361f840913450e9195a45efd4281f2"}
  </script>
</div>
    '
        height="400"
        width="100%"
        frameborder="0"
      ></iframe>
  </div>
</template>

<script>
export default {
  name: 'example-multiindex',
  data() {return {}}
}
</script>
