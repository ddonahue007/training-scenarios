Now we'll add a legend to the bullet chart...

## Task

1) Make sure the App.js file is still open

2) Locate the code that looks like the following:

<pre class="file">
&lt;ChartBullet
  comparativeWarningMeasureData={[{ name: &#39;Warning&#39;, y: 88 }]}
  maxDomain={{y: 100}}
  padding={{
    bottom: 50,
    left: 150,
    right: 50,
    top: 50
  }}
  primarySegmentedMeasureData={[{ name: &#39;Measure&#39;, y: 60 }]}
  qualitativeRangeData={[{ name: &#39;Range&#39;, y: 50 }, { name: &#39;Range&#39;, y: 75 }]}
  title="Text label"
  subTitle="Measure details"
  height={150}
  width={600}
/&gt;
</pre>

3) Add the following properties to that section:

<pre class="file" data-target="clipboard">
comparativeWarningMeasureLegendData={[{ name: &#39;Warning&#39; }]}
legendOrientation=&quot;horizontal&quot;
legendPosition=&quot;bottom&quot;
primarySegmentedMeasureLegendData={[{ name: &#39;Measure 1&#39; }, { name: &#39;Measure 2&#39; }]}
qualitativeRangeLegendData={[{ name: &#39;Range 1&#39; }, { name: &#39;Range 2&#39; }]}
</pre>

- The `legendOrientation` property specifies whether the legend is rendered horizontally or vertically
- The `legendPosition` property specifies whether the legend is rendered on the bottom or right of the chart
- The `qualitativeRangeLegendData` property adds a qualitative range legend to the bullet chart
- The `primarySegmentedMeasureLegendData` property adds a primary legend to the bullet chart
- The `comparativeWarningMeasureLegendData` property adds comparative warning legend to the bullet chart

4) Once the preview reloads - it should look like this:
<img src="module-bullet/assets/legend.png" alt="Chart with legend" style="box-shadow: rgba(3, 3, 3, 0.2) 0px 1.25px 2.5px 0px;" />

We'll continue by changing the chart's theme color in the next step.