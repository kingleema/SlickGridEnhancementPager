# SlickGrid Enhancement Pager
***

## What is 
  It is a small plugin that makes SlickGrid pagination use much easier.

## Features
* Easy-to-use server-side paging.
* Standard paging navigation buttons(First, Previous, Next and Last).
* Drop-down selection of page size.
* Jumping to the specified page support.
* <b>Slider pager support.</b>
* Display current paging infomation(e.g. Display 1-10 / 100).
* i18n support.

## Parameters
* container:  an element that renders SlickGrid Enhancement Pager(e.g. div element).
* remoteUrl: a http remote handler that returns json string(<b>Note: content-type: text/plain, charset: utf-8</b>).<br/>
[json string example]<br/>
 `{"Total":3,"Rows":"[{\"Id\":\"1\",\"Name\":\"Tim\"},{\"Id\":\"2\",\"Name\":\"Mary\"},{\"Id\":\"3\",\"Name\":\"Tom\"}]"}// "Total" means the count of the whole recordset, while "Rows" means the returned records of the current page.For details, please see the example.`<br/>
* datagrid: the SlickGrid object.
* pagerType: slider or standard paging navigation buttons.(See the example)
* waiting: set ajax timeout.(default value: 30000, 30s)
* params : addtional params passed to http post.(See the example)
* trans : translation for i18n.

## Usage
> [html code]<br/>
  `<div id="myGrid" style="width:700px;height:500px;"></div>`<br/>
  `<div id="pager" style="width:700px;" class="slick-enhancement-pager">`
 
> [js code]<br/>
  `var grid;`<br/>
  `var columns = [`<br/>
  `               { id: "id", name: "id", field: "id" },`<br/>
  `               { id: "name", name: "name", field: "name" }`<br/>
  `             ];`<br/>
  `var options = {`<br/>
  `   enableCellNavigation: true,`<br/>
  `   enableColumnReorder: false`<br/>
  `};`<br/>
> `$(function () {`<br/>
 `  var data = [];`<br/>
 `  grid = new Slick.Grid("#myGrid", data, columns, options);`<br/>
 `  var pager = new Slick.Controls.EnhancementPager({`<br/>
 `                container: $("#pager"), `<br/>
 `                remoteUrl: "http://localhost:1690/Data.ashx",`<br/>
 `                datagrid: grid`<br/>
 `            });`<br/>
 `});`<br/>

## Example
Please see the details from the example.zip file.(the <i>example.html</i> file under the <u>ASP.NET\SlickgridEnhancementPagerDemo\slickgrid\examples</u> folder or under the <u>PHP</u> folder)

## Icons
Some of icons are from [famfamfam](http://www.famfamfam.com/).

## License
This plugin is released under the MIT license (See the MIT-LICENSE.txt file), so it is free for both personal and commercial use.

## Donate
This small plugin is developed in my spare time.If you like it or feel useful, just "buy me a beer" ;) .<br/>
Any amount will be deeply appreciated with my sincerity!<br/><br/>
<a href="https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=kingleema%40gmail%2ecom&item_name=Supporting%20SlickGrid%20Enhancement%20Pager&no_shipping=0&no_note=1&tax=0&currency_code=USD&lc=US&bn=PP%2dDonationsBF&charset=UTF%2d8" target="_blank">
  <img src="https://www.paypal.com/en_US/i/btn/x-click-but04.gif" alt="Donate" style="border-width:0;" />
</a>