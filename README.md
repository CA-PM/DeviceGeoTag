# BusyTimes
A set of charts which displays the overall volume of an interface, device, or group for the specified metric family and metric. 
The data is bucketized and displayed in aggregate (sum) based on the:
	* Hour of Day (0-24)
	* Day of Week (Sunday - Saturday)
	* Day of Month (1-31)

![](./screenShot.jpg?raw=true "Example Screenshot")

##Installation Instructions:

1. Copy app to user app directory on CAPC (/opt/CA/PerformanceCenter/PC/webapps/pc/apps/user)
2. Modify/Add a view to a dashboard (for group context) or a context page (interface, device)
3. Add browser view(s) with height of 700
4. Add URL to app location with key parameters defined (see below)

###CAPC Browser view sample URL:

This example would be placed on an interface context page to view the bucketized Errors metric to understand when errors are most frequently occuring for the given interface:

/pc/apps/user/BusyTime/index.html?interfaceID={ItemIdDA}&startTime={TimeStartUTC}&endTime={TimeEndUTC}&metricFamily=portmfs&metric=im_Errors

###Key URL parameters:

<table>
    <tr>
        <td>Parameter</td>
        <td>Description</td>
    </tr>
    <tr>
    	<td>interfaceID</td>
    	<td>The ID of the interface for the given context page</td>
    </tr>
    <tr>
    	<td>deviceID</td>
    	<td>The ID of the device for the given context page</td>
    </tr>
    <tr>
    	<td>groupID</td>
    	<td>The ID of the group for the given Dashboard</td>
    </tr>
    <tr>
    	<td>metricFamily</td>
    	<td>The OpenAPI ID for the targetted Metric Family (see QueryBuilder for MF names)</td>
    </tr>
        <tr>
    	<td>metric</td>
    	<td>The OpenAPI name for the desired metric (see QueryBuilder for metric names</td>
    </tr>
        <tr>
    	<td>startTime</td>
    	<td>The start time (UNIX Epoch time) from the CAPC Time selector</td>
    </tr>
        <tr>
    	<td>endTime</td>
    	<td>The end time (UNIX Epoch time) from the CAPC Time selector</td>
    </tr>
</table>


===================================================================================

License (refer to license.txt in folder for 3rd party license details)

Copyright (c) 2016 CA Technologies
 
The MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
 
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
 
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

===================================================================================

