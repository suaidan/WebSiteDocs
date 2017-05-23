﻿# Available Charts

<ol style="list-style: none; padding: 0">
    <li>
        <h3>1. CartesianChart</h3>

        <p>
            The <i>Cartesian Chart</i> class allows you to plot any series that uses a
            <i>Cartesian coordinate system</i>, every point is a pair of values (<i>X</i>, <i>Y</i>),
            it supports many series, you can combine any of these seriesin the same plot:
        </p>

        <div class="row spaced">
            <div class="col-lg-3 col-md-4 col-sm-6 col-xs-12 text-center">
                <div>Line Series</div>
                <img ng-src="{{source}}/v1/Available Charts/lineSeries.jpg" />
            </div>
            <div class="col-lg-3 col-md-4 col-sm-6 col-xs-12 text-center">
                <div>Vertical Line Series</div>
                <img ng-src="{{source}}/v1/Available Charts/verticallineseries.jpg" />
            </div>
            <div class="col-lg-3 col-md-4 col-sm-6 col-xs-12 text-center">
                <div>Column Series</div>
                <img ng-src="{{source}}/v1/Available Charts/columnseries.jpg" />
            </div>
            <div class="col-lg-3 col-md-4 col-sm-6 col-xs-12 text-center">
                <div>Row Series</div>
                <img ng-src="{{source}}/v1/Available Charts/rowseries.jpg" />
            </div>
            <div class="col-lg-3 col-md-4 col-sm-6 col-xs-12 text-center">
                <div>Stacked Area Series</div>
                <img ng-src="{{source}}/v1/Available Charts/stackedareaseries.jpg" />
            </div>
            <div class="col-lg-3 col-md-4 col-sm-6 col-xs-12 text-center">
                <div>Vertical Stacked Area Series</div>
                <img ng-src="{{source}}/v1/Available Charts/verticalstackedareaseries.jpg" />
            </div>
            <div class="col-lg-3 col-md-4 col-sm-6 col-xs-12 text-center">
                <div>Stacked Column Series</div>
                <img ng-src="{{source}}/v1/Available Charts/stackedcolumnseries.jpg" />
            </div>
            <div class="col-lg-3 col-md-4 col-sm-6 col-xs-12 text-center">
                <div>Stacked Row Series</div>
                <img ng-src="{{source}}/v1/Available Charts/stackedrowsseries.jpg" />
            </div>
            <div class="col-lg-3 col-md-4 col-sm-6 col-xs-12 text-center">
                <div>Heat Series</div>
                <img ng-src="{{source}}/v1/Available Charts/Heat Series.jpg" />
            </div>
            <div class="col-lg-3 col-md-4 col-sm-6 col-xs-12 text-center">
                <div>OHCLand Candle Series</div>
                <img ng-src="{{source}}/v1/Available Charts/ohclseries.jpg" />
            </div>
            <div class="col-lg-3 col-md-4 col-sm-6 col-xs-12 text-center">
                <div>Bubbles Series</div>
                <img ng-src="{{source}}/v1/Available Charts/buubleseries.jpg" />
            </div>
            <div class="col-lg-3 col-md-4 col-sm-6 col-xs-12 text-center">
                <div>StepLine Series</div>
                <img ng-src="{{source}}/v1/Available Charts/stepline.png" />
            </div>
        </div>

        <p>
            Here is an example, notice some series use a specialized
            point, LiveCharts already knows how to plot many types, if you need to define your own,
            please take a read at 
            <a href="/App/Examples/v1/{{sms.platform}}/Types and Mappers">Types and Mappers</a> article.
        </p>

        <pre class="prettyprint">using LiveCharts;
using LiveCharts.Defaults; //Contains the already defined types

LiveCharts.SeriesCollection series = new LiveCharts.SeriesCollecion 
{
  new LineSeries
  {
    //The ObservableValue class notifies the chart to update when value changes

    Values = new ChartValues&lt;LiveCharts.Defaults.ObservableValue&gt;
    {
        new LiveCharts.Defaults.ObservableValue(4),
        new LiveCharts.Defaults.ObservableValue(4),
        // ...
    }
  },
  new ColumnSeries
  {
    Values = new ChartValues&lt;ObservableValue&gt;
    {
      new ObservableValue(4),
      new ObservableValue(2),
      // ...
    }
  },
  new OhlcSeries
  {
    Values = new ChartValues&lt;OhlcPoint&gt;
    {
      new OhlcPoint(32, 35, 30, 32),
      new OhlcPoint(33, 38, 31, 37),
      // ..
    }
  }
}</pre>
    </li>
    <li>
        <h3>2. Pie Chart</h3>

        <p>Use it to plot pies and doughnuts</p>
    </li>
    <li>
        <h3>3. Gauge</h3>

        <p>It has 2 modes, 180 and 360 degrees, useful to display progress or completion.</p>
    </li>
    <li>
        <h3>4. Angular Gauge</h3>

        <p>Use it to display the current value in a range, for example a velocimeter.</p>
    </li>
    <li>
        <h3>5. Maps</h3>

        <p>LiveCharts also support geo heat maps, they compare the values according to geographic zone.</p>
    </li>
</ol>