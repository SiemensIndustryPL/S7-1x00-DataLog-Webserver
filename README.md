# S7-1x00 DataLog Download
A bunch of scripts for automating of DataLogs download via SIMATIC S7-1200/1500 Webserver.
#
Currently tested on:
<ul>
 <li>S7-1200 FW V4.4 (works partly)</li>
 <li>S7-1500 FW V2.8</li>
</ul>
<br />
Creating ZIP archive on S7-1200 does not work well for too many DataLogs due to very low webserver performance. Hopefully this will change in the next HW or FW version. There's alternative option <strong>in preparation</strong> with downloading all DataLogs one after another.
#
Setting up:
<ul>
 <li>Upload all files from the repo's subdirectory to your webserver (with all sub-scripts and libraries)</li>
 <li>Do not insert .js extension to the section "files with dynamic content" in your webserver settings</li>
 <li>Change the main page from "index.htm" to "index.html" in your webserver settings</li>
 <li>The scripts do not take user authentication into consideration thus it is necessary to set files permission to "Everyone" in your webserver settings</li>
</ul>
#
The script uses additional libraries (available on MIT license) listed below:
<ul>
 <li>https://github.com/Stuk/jszip</li>
 <li>https://github.com/eligrey/FileSaver.js</li>
</ul>
