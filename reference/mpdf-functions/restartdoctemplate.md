---
layout: page
title: RestartDocTemplate()
parent_title: mPDF functions
permalink: /reference/mpdf-functions/restartdoctemplate.html
---

<div id="bpmbook" class="bpmbook" style="direction:ltr;">
<div class="topic_user_field">
<div id="U0">
<p>(mPDFI &gt;= 2.4)</p>
<p>RestartDocTemplate – Re-start the use of a Document template from the next page</p>
<h2>Description</h2>

<div class="alert alert-info" role="alert">void <b>RestartDocTemplate</b> ( )</div>
<p>Restart the use of a document template (set by <a href="{{ "/reference/mpdf-functions/setdoctemplate.html" | prepend: site.baseurl }}">SetDocTemplate()</a>) from the next page.</p>
<h2>Parameters</h2>
<p class="manual_param_dt"><span class="parameter">none</span></p>
<h2>Changelog</h2>
<table class="bpmTopic"> <thead>
<tr> <th>Version</th><th>Description</th> </tr>
</thead> <tbody>
<tr>
<td>2.4</td>
<td>Function was added.</td>
</tr>
</tbody> </table>
<h2>Examples</h2>

{% highlight php %}
Example #1
{% endhighlight %}

{% highlight php %}
<?php

<?php

include("../mpdf.php");

$mpdf=new mPDF(); 

$mpdf->SetImportUse(); 

// Document template consisting of 2 pages, first with logo and addresses, 2nd with a simple header

$mpdf->SetDocTemplate('logoheader.pdf',true); 

$mpdf->AddPage();

$mpdf->WriteHTML($firstletter);

$mpdf->RestartDocTemplate();

$mpdf->AddPage();

$mpdf->WriteHTML($secondletter);

$mpdf->RestartDocTemplate();

$mpdf->AddPage();

$mpdf->WriteHTML($thirdletter);

$mpdf->Output();

?>
{% endhighlight %}

<h2>See Also</h2>
<ul>
<li><a href="{{ "/reference/mpdf-functions/setimportuse.html" | prepend: site.baseurl }}">SetImportUse()</a> - Enable the use of imported PDF files or templates</li>
<li><a href="{{ "/reference/mpdf-functions/setdoctemplate.html" | prepend: site.baseurl }}">SetDocTemplate()</a> - Specify an external PDF file to use as a template</li>
<li><a href="{{ "/reference/mpdf-functions/thumbnail.html" | prepend: site.baseurl }}">Thumbnail()</a> - Print thumbnails of an external PDF file

</li>
<li><a href="{{ "/reference/mpdf-functions/setsourcefile.html" | prepend: site.baseurl }}">SetSourceFile()</a> - Specify the source PDF file used to import pages into the document

</li>
<li><a href="{{ "/reference/mpdf-functions/usetemplate.html" | prepend: site.baseurl }}">UseTemplate()</a> - Insert an imported page from an external PDF file</li>
<li><a href="{{ "/reference/mpdf-functions/setpagetemplate.html" | prepend: site.baseurl }}">SetPageTemplate()</a> - Specify a page from an external PDF file to use as a template

</li>
</ul>
<p>&nbsp;</p>
</div>
</div>
