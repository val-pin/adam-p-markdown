### custom function in `charts` :


* DB changes needed for future modifications:
* Table : charts
* New Field : renderer ( AS text )
* Save path and stroke details in json format

### chart function in db ###

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


Or any other function.

### script changes needed:


*  File : script-chart.phtml
*  Function : new getChartRenderer() required to draw stroke

`   var customFunc = function( chart , code ) {
      return new Function("chart" , code )( chart );
   }

   function getChartFunction( chartObj ) {
    
      if( chartObj.options.renderer ){
        
        customFunc( chartObj , chartObj.options.renderer ); 
      }   
    }`
	

•	This function will be triggered when page loads and filter gets applied via getSeriesAddFunction().

•	This function will also be triggered in zoom chart event occurs.