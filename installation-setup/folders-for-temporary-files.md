---
layout: page
title: Folders for temporary files
parent_title: Installation & Setup
permalink: /installation-setup/folders-for-temporary-files.html
---

<div id="bpmbook" class="bpmbook" style="direction:ltr;">
<div class="topic_user_field">
<div id="U0">
<p>mPDF is configured to use <span class="filename">[your_path_to_mpdf]/tmp/</span> as a folder to write temporary files (mainly for images), and <span class="filename">[your_path_to_mpdf]/ttfontdata/</span> as a folder to cache font metrics data. Write permissions should ideally be set on both these folders to allow read/write access for the script.</p>
<h3>Images

</h3>
<p>If you wish to use a different folder for temporary files, you should define the constant <code>_MPDF_TEMP_PATH</code> before including the <span class="filename">mpdf.php</span> file e.g.</p>

{% highlight php %}
<?php

define("_MPDF_TEMP_PATH", '../../common/tempfiles/');

include("../mpdf.php");

$mpdf=new mPDF();
{% endhighlight %}

<p>Images will still be processed without write permissions to this folder, but at considerable cost in processing time and memory usage.</p>
<h3>Fonts

</h3>
<p>If you wish to use a different folder for temporary files, you should define the constant <code>_MPDF_TTFONTDATAPATH</code> before including the <span class="filename">mpdf.php</span> file</p>
<p>Fonts can still be used and embedded without write permissions to this folder, but at some cost in processing time and memory usage.</p>
</div>
</div>
