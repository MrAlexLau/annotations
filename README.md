
  <title>Highcharts Demo - annotations demo</title>
  
  <script src="http://code.jquery.com/jquery-1.9.1.min.js"></script>
	<script src="http://code.highcharts.com/highcharts.js"></script>
  <script src="./js/annotations.js"></script>
  <script src="./js/demo.js"></script>

<style>
body { font-family: "Lucida Grande", "Lucida Sans Unicode", Verdana, Arial, Helvetica, sans-serif; font-size: 0.8em; line-height: 1.2em }

.form { margin-right: 10px; width: 190px; padding: 0px; background-color: #e8eaeb; padding: 5px; float: left}
.form .form-header { font-size: 1em; padding: 10px;	 background: #3d3d3d; color: #fff; }
.form > p { padding: 5px 10px; margin: 0px; }
.form > p:nth-child(2n) { background: #f7f7f7; }
.form label { width: 150px; float: left; margin-top: 5px;}
.form input { width: 160px; }
.form input[type="radio"] { width: auto; margin-left: 55px;}

.chart-title {background-color: #3d3d3d; color: #fff; width: 609px; padding: 10px; float: left; }

h1,
h2,
h3,
h4,
h5,
h6,
p,
blockquote {
    margin: 0;
    padding: 0;
}
body {
    color: #737373;
    background-color: white;
    margin: 10px 13px 10px 13px;
}
table {
	margin: 10px 0 15px 0;
	border-collapse: collapse;
}
td,th {	
	border: 1px solid #ddd;
	padding: 3px 10px;
}
th {
	padding: 5px 10px;	
}

a {
    color: #0069d6;
}
a:hover {
    color: #0050a3;
    text-decoration: none;
}
a img {
    border: none;
}
p {
    margin-bottom: 9px;
}
h1,
h2,
h3,
h4,
h5,
h6 {
    color: #404040;
    line-height: 36px;
}
h1 {
    margin-bottom: 18px;
    font-size: 30px;
}
h2 {
    font-size: 24px;
}
h3 {
    font-size: 18px;
}
h4 {
    font-size: 16px;
}
h5 {
    font-size: 14px;
}
h6 {
    font-size: 13px;
}
hr {
    margin: 0 0 19px;
    border: 0;
    border-bottom: 1px solid #ccc;
}
blockquote {
    padding: 13px 13px 21px 15px;
    margin-bottom: 18px;
    font-family:georgia,serif;
    font-style: italic;
}
blockquote:before {
    content:"\201C";
    font-size:40px;
    margin-left:-10px;
    font-family:georgia,serif;
    color:#eee;
}
blockquote p {
    font-size: 14px;
    font-weight: 300;
    line-height: 18px;
    margin-bottom: 0;
    font-style: italic;
}
code, pre {
    font-family: Monaco, Andale Mono, Courier New, monospace;
}
code {
    background-color: #fee9cc;
    color: rgba(0, 0, 0, 0.75);
    padding: 1px 3px;
    font-size: 12px;
    -webkit-border-radius: 3px;
    -moz-border-radius: 3px;
    border-radius: 3px;
}
pre {
    display: block;
    padding: 14px;
    margin: 0 0 18px;
    line-height: 16px;
    font-size: 11px;
    border: 1px solid #d9d9d9;
    white-space: pre-wrap;
    word-wrap: break-word;
}
pre code {
    background-color: #fff;
    color:#737373;
    font-size: 11px;
    padding: 0;
}
sup {
    font-size: 0.83em;
    vertical-align: super;
    line-height: 0;
}
* {
	-webkit-print-color-adjust: exact;
}
@media screen and (min-width: 914px) {
    body {
        width: 854px;
        margin:10px auto;
    }
}
@media print {
	body,code,pre code,h1,h2,h3,h4,h5,h6 {
		color: black;
	}
	table, pre {
		page-break-inside: avoid;
	}
}

</style>

<h1>Annotations module</h1>

<h2>Sample code</h2>

<pre><code>new Highcharts.Chart({
  chart: {
    renderTo: container
  },
  series: [{
      data: [29.9, 71.5, 106.4, 129.2, 144.0, 176.0]
  }],
  annotations: [{
    xValue: 4,
    yValue: 125,
    title: {
        text: "Annotated chart!"
    }
  }]
})
</code></pre>

<h2>Available options</h2>

<h3>Chart options</h3>

<table>
<thead>
<tr>
<th align="left">Option            </th>
<th align="left"> Description</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">chart.annotations </td>
<td align="left"> Array containing annotation configuration objects</td>
</tr>
</tbody>
</table>


<h3>Annotation configuration object</h3>

<table>
<thead>
<tr>
<th align="left">Option                                    </th>
<th align="left"> Description</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">x<br>y                                    </td>
<td align="left"> Annotation position defined in pixels</td>
</tr>
<tr>
<td align="left">xValue<br>yValue                          </td>
<td align="left"> Annotation position defined using axis values</td>
</tr>
<tr>
<td align="left">xAxis<br>yAxis                            </td>
<td align="left"> Axis index, default to 0</td>
</tr>
<tr>
<td align="left">anchorX<br>anchorY                        </td>
<td align="left"> Defines annotation anchor point (see below), available values:<br>anchorX: left, center, right<br>anchorY: top, middle, bottom</td>
</tr>
<tr>
<td align="left">allowDragX<br>allowDragY</td>
<td align="left"> Allow user to drag and drop an annotation. Horizontal and vertical.</td>
</tr>
<tr>
<td align="left">linkedTo                                  </td>
<td align="left"> Link annotation to point or series using it's id</td>
</tr>
<tr>
<td align="left">title                                     </td>
<td align="left"> Title configuration object</td>
</tr>
<tr>
<td align="left">title.text                                </td>
<td align="left"> Title text</td>
</tr>
<tr>
<td align="left">title.x<br>title.y                        </td>
<td align="left"> Title position in pixels, relative to annotation position</td>
</tr>
<tr>
<td align="left">title.style                               </td>
<td align="left"> Additional CSS styles for title</td>
</tr>
<tr>
<td align="left">title.style.color                         </td>
<td align="left"> Title text color</td>
</tr>
<tr>
<td align="left">title.style.fontSize                      </td>
<td align="left"> Title font size</td>
</tr>
<tr>
<td align="left">shape                                     </td>
<td align="left"> Shape configuration object</td>
</tr>
<tr>
<td align="left">shape.type                                </td>
<td align="left"> Shape type, available types are "path", "circle" and "rect"</td>
</tr>
<tr>
<td align="left">shape.units                               </td>
<td align="left"> Defines whether shape uses pixels or axis values</td>
</tr>
<tr>
<td align="left">shape.params                              </td>
<td align="left"> Shape parameters (parameters are passed to renderer method like rect, circle or path)</td>
</tr>
</tbody>
</table>


<h3>Available shape parameters</h3>

<table>
<thead>
<tr>
<th align="left">Option                                      </th>
<th align="left"> Description                                        </th>
<th align="left"> Limited to</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">shape.params.x<br>shape.params.y             </td>
<td align="left"> Shape position relative to the annotation position </td>
<td align="left">rect<br>circle</td>
</tr>
<tr>
<td align="left">shape.params.width<br>shape.params.height    </td>
<td align="left"> Rectangle width and height (only for "rect" type)  </td>
<td align="left"> rect</td>
</tr>
<tr>
<td align="left">shape.params.d                               </td>
<td align="left"> Path definition (only for "path" type)             </td>
<td align="left"> path</td>
</tr>
<tr>
<td align="left">shape.params.r                               </td>
<td align="left"> Circle radius                                      </td>
<td align="left"> circle</td>
</tr>
<tr>
<td align="left">shape.params.fill                            </td>
<td align="left"> Fill color, default: transparent                   </td>
<td align="left"> -</td>
</tr>
<tr>
<td align="left">shape.params.stroke                          </td>
<td align="left"> Stroke color, default: black                       </td>
<td align="left"> -</td>
</tr>
<tr>
<td align="left">shape.params.strokeWidth                     </td>
<td align="left"> Stroke width (and line width for path), default: 2 </td>
<td align="left"> -</td>
</tr>
</tbody>
</table>


<h3>Chart.annotations</h3>

<table>
<thead>
<tr>
<th align="left">Property                       </th>
<th align="left"> Description</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">chart.annotations.add(options) </td>
<td align="left"> Add one annotation with given options</td>
</tr>
<tr>
<td align="left">chart.annotations.redraw()     </td>
<td align="left"> Redraw all annotations</td>
</tr>
<tr>
<td align="left">chart.annotations.allItems     </td>
<td align="left"> Array containing all annotations</td>
</tr>
</tbody>
</table>


<h3>Annotation object</h3>

<table>
<thead>
<tr>
<th align="left">Property                   </th>
<th align="left"> Description</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">annotation.update(options) </td>
<td align="left"> Update annotation with given options</td>
</tr>
<tr>
<td align="left">annotation.destroy()       </td>
<td align="left"> Destroy annotation</td>
</tr>
</tbody>
</table>



<h2>Advanced demo</h2>


<h3>Use simple form to setup annotation object (demo.js)</h3>
<div style="margin: 10px 0px 50px 0px;width: 854px; float: left;">
		<div class="form">
				<div class="form-header"> Add annotation: </div>
				<p>
						<label> Shape: </label> <br>
						<input type="radio" name="type" value="circle" checked/>  <span for="circle"> circle </span> <br>
						<input type="radio" name="type" value="rect"/> 	<span for="square"> square </span>  <br>
						<input type="radio" name="type" value="path"/>  <span for="line"> line </span> 
				</p>
				<p>
						<label for="fill"> Fill color: </label>
						<input type="text" id="fill" value="#AB3445"/>
				</p>
				<p>
						<label for="stroke"> Stroke color: </label>
						<input type="text" id="stroke" value="red"/>
				</p>
				<p>
						<label for="strokeWidth"> Stroke width: </label>
						<input type="range" id="strokeWidth" step="1" min="0" max="15"/>
				</p>
				<p>
						<label for="title"> Title: </label>
						<input id="title" type="text" value="Annotation title <br> with line break" /> 
				</p>
		</div>
		<div id="container" style="float: left; height: 342px; width: 640px">
		</div>
</div>
