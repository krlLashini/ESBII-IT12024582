<!DOCTYPE html>
<html>
<head>
<title>Lab 3 - Creating Database</title>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<style type="text/css">
/* GitHub stylesheet for MarkdownPad (http://markdownpad.com) */
/* Author: Nicolas Hery - http://nicolashery.com */
/* Version: b13fe65ca28d2e568c6ed5d7f06581183df8f2ff */
/* Source: https://github.com/nicolahery/markdownpad-github */

/* RESET
=============================================================================*/

html, body, div, span, applet, object, iframe, h1, h2, h3, h4, h5, h6, p, blockquote, pre, a, abbr, acronym, address, big, cite, code, del, dfn, em, img, ins, kbd, q, s, samp, small, strike, strong, sub, sup, tt, var, b, u, i, center, dl, dt, dd, ol, ul, li, fieldset, form, label, legend, table, caption, tbody, tfoot, thead, tr, th, td, article, aside, canvas, details, embed, figure, figcaption, footer, header, hgroup, menu, nav, output, ruby, section, summary, time, mark, audio, video {
  margin: 0;
  padding: 0;
  border: 0;
}

/* BODY
=============================================================================*/

body {
  font-family: Helvetica, arial, freesans, clean, sans-serif;
  font-size: 14px;
  line-height: 1.6;
  color: #333;
  background-color: #fff;
  padding: 20px;
  max-width: 960px;
  margin: 0 auto;
}

body>*:first-child {
  margin-top: 0 !important;
}

body>*:last-child {
  margin-bottom: 0 !important;
}

/* BLOCKS
=============================================================================*/

p, blockquote, ul, ol, dl, table, pre {
  margin: 15px 0;
}

/* HEADERS
=============================================================================*/

h1, h2, h3, h4, h5, h6 {
  margin: 20px 0 10px;
  padding: 0;
  font-weight: bold;
  -webkit-font-smoothing: antialiased;
}

h1 tt, h1 code, h2 tt, h2 code, h3 tt, h3 code, h4 tt, h4 code, h5 tt, h5 code, h6 tt, h6 code {
  font-size: inherit;
}

h1 {
  font-size: 28px;
  color: #000;
}

h2 {
  font-size: 24px;
  border-bottom: 1px solid #ccc;
  color: #000;
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
  color: #777;
  font-size: 14px;
}

body>h2:first-child, body>h1:first-child, body>h1:first-child+h2, body>h3:first-child, body>h4:first-child, body>h5:first-child, body>h6:first-child {
  margin-top: 0;
  padding-top: 0;
}

a:first-child h1, a:first-child h2, a:first-child h3, a:first-child h4, a:first-child h5, a:first-child h6 {
  margin-top: 0;
  padding-top: 0;
}

h1+p, h2+p, h3+p, h4+p, h5+p, h6+p {
  margin-top: 10px;
}

/* LINKS
=============================================================================*/

a {
  color: #4183C4;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

/* LISTS
=============================================================================*/

ul, ol {
  padding-left: 30px;
}

ul li > :first-child, 
ol li > :first-child, 
ul li ul:first-of-type, 
ol li ol:first-of-type, 
ul li ol:first-of-type, 
ol li ul:first-of-type {
  margin-top: 0px;
}

ul ul, ul ol, ol ol, ol ul {
  margin-bottom: 0;
}

dl {
  padding: 0;
}

dl dt {
  font-size: 14px;
  font-weight: bold;
  font-style: italic;
  padding: 0;
  margin: 15px 0 5px;
}

dl dt:first-child {
  padding: 0;
}

dl dt>:first-child {
  margin-top: 0px;
}

dl dt>:last-child {
  margin-bottom: 0px;
}

dl dd {
  margin: 0 0 15px;
  padding: 0 15px;
}

dl dd>:first-child {
  margin-top: 0px;
}

dl dd>:last-child {
  margin-bottom: 0px;
}

/* CODE
=============================================================================*/

pre, code, tt {
  font-size: 12px;
  font-family: Consolas, "Liberation Mono", Courier, monospace;
}

code, tt {
  margin: 0 0px;
  padding: 0px 0px;
  white-space: nowrap;
  border: 1px solid #eaeaea;
  background-color: #f8f8f8;
  border-radius: 3px;
}

pre>code {
  margin: 0;
  padding: 0;
  white-space: pre;
  border: none;
  background: transparent;
}

pre {
  background-color: #f8f8f8;
  border: 1px solid #ccc;
  font-size: 13px;
  line-height: 19px;
  overflow: auto;
  padding: 6px 10px;
  border-radius: 3px;
}

pre code, pre tt {
  background-color: transparent;
  border: none;
}

kbd {
    -moz-border-bottom-colors: none;
    -moz-border-left-colors: none;
    -moz-border-right-colors: none;
    -moz-border-top-colors: none;
    background-color: #DDDDDD;
    background-image: linear-gradient(#F1F1F1, #DDDDDD);
    background-repeat: repeat-x;
    border-color: #DDDDDD #CCCCCC #CCCCCC #DDDDDD;
    border-image: none;
    border-radius: 2px 2px 2px 2px;
    border-style: solid;
    border-width: 1px;
    font-family: "Helvetica Neue",Helvetica,Arial,sans-serif;
    line-height: 10px;
    padding: 1px 4px;
}

/* QUOTES
=============================================================================*/

blockquote {
  border-left: 4px solid #DDD;
  padding: 0 15px;
  color: #777;
}

blockquote>:first-child {
  margin-top: 0px;
}

blockquote>:last-child {
  margin-bottom: 0px;
}

/* HORIZONTAL RULES
=============================================================================*/

hr {
  clear: both;
  margin: 15px 0;
  height: 0px;
  overflow: hidden;
  border: none;
  background: transparent;
  border-bottom: 4px solid #ddd;
  padding: 0;
}

/* TABLES
=============================================================================*/

table th {
  font-weight: bold;
}

table th, table td {
  border: 1px solid #ccc;
  padding: 6px 13px;
}

table tr {
  border-top: 1px solid #ccc;
  background-color: #fff;
}

table tr:nth-child(2n) {
  background-color: #f8f8f8;
}

/* IMAGES
=============================================================================*/

img {
  max-width: 100%
}
</style>
</head>
<body>
<p>NAME 		: K.R.L.LASHINI</p>
<p>REG.NO 		: IT12024582</p>
<p>SUBJECT 	: ENTERPRISE STANDARDS AND BEST PRACTICES FOR IT INFRASTRUCTURE</p>
<p>LAB			: 03 - CREATING DATABASE</p>
<p>DATE		: 17.07.2015</p>
<p><strong># CREATING A DB INSTANCE RUNNING THE MYSQL DATABASE ENGINE #</strong></p>
<p>The basic building block of Amazon RDS is the DB instance. The DB instance is where you create your MySQL databases.</p>
<p>It's important to finish  Setting Up for Amazon RDS. This task has already done while doing Lab1.</p>
<h2>TO LAUNCH A MYSQL DB INSTANCE</h2>
<ol>
<li>Sign in to the AWS Management Console and open the Amazon RDS console at https://console.aws.amazon.com/rds/.In the top right corner of the AWS Management Console, select the region in which you want to create the DB instance.In the navigation pane, click DB Instances.</li>
</ol>
<p><img src="https://cloud.githubusercontent.com/assets/13194331/8958066/3da78238-3620-11e5-9b99-30281815c929.png" /></p>
<p>2.Click Launch DB Instance to start the Launch DB Instance Wizard.The wizard opens on the Select Engine page.In the Launch DB Instance Wizard window, click the Select button for the MySQL DB engine.</p>
<p><img src="https://cloud.githubusercontent.com/assets/13194331/8958067/3da84de4-3620-11e5-88bf-5e5ff210f2cb.png" /></p>
<p><img src="https://cloud.githubusercontent.com/assets/13194331/8958068/3daa8a96-3620-11e5-8e8d-eff466031436.png" /></p>
<p>3.On the Specify DB Details page, specify your DB instance information. The following table shows settings for an example DB instance. Click Next when you are finished. </p>
<p><img src="https://cloud.githubusercontent.com/assets/13194331/8958070/3dabd23e-3620-11e5-888f-a73fb4c582c0.png" /></p>
<p><img src="https://cloud.githubusercontent.com/assets/13194331/8958071/3dad7c6a-3620-11e5-8452-b151e9f7b04b.png" /></p>
<p>4.On the Configure Advanced Settings page, provide additional information that RDS needs to launch the MySQL DB instance.Specify your DB instance information, then click Next Step.</p>
<p><img src="https://cloud.githubusercontent.com/assets/13194331/8958069/3dab4bd4-3620-11e5-988d-197eb0022657.png" /></p>
<p>5.Click Launch DB Instance to create your MySQL DB instance.</p>
<p><img src="https://cloud.githubusercontent.com/assets/13194331/8958075/3dde1cf8-3620-11e5-90ac-8ba73eb5a522.png" /></p>
<p>6.On the final page of the wizard, click Close.On the Amazon RDS console, the new DB instance appears in the list of DB instances. The DB instance will have a status of creating until the DB instance is created and ready for use. When the state changes to available, you can connect to the DB instance. Depending on the DB instance class and store allocated.</p>
<p><img src="https://cloud.githubusercontent.com/assets/13194331/8958074/3dde00b0-3620-11e5-9456-fcea0ed76c49.png" /></p>
<p><img src="https://cloud.githubusercontent.com/assets/13194331/8958073/3ddcf09e-3620-11e5-9314-c94ac90df979.png" /></p>

</body>
</html>
<!-- This document was created with MarkdownPad, the Markdown editor for Windows (http://markdownpad.com) -->
