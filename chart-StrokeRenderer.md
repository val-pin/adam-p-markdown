custom stroke render field in `charts` :
-

* DB changes needed for future modifications:
* Table : charts
* New Field : renderer ( AS text )
* Save path and stroke details in json format

	// json array
	{"0":{"path":["M", 300, 0, "L", 300, 300],"attr":{"strokeWidth":2,"stroke":"red"}},"1":	{"path":["M", 0, 150, "L", 500, 150],"attr":{"strokeWidth":2,"stroke":"red"}}}
_[Note: First json array targets x stroke and second y stroke.]_

script changes needed:
-

*  File : script-chart.phtml
*  Function : new getChartRenderer() required to draw stroke


	// chart stroke code here

	chart.renderer.path(['M', 300, 0, 'L', 300, 300])
        .attr({
            'stroke-width': 2,
            stroke: 'red'
        })
        .add();
        
     chart.renderer.path(['M', 0, 150, 'L', 500, 150])
        .attr({
            'stroke-width': 2,
            stroke: 'red'
        })
        .add();

•	This function will be triggered when chart is called on getDashboardOnReady().

•	This function will also be triggered in zoom chart event.
