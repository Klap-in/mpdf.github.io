---
layout: page
title: Replaceable Aliases
parent_title: What Else Can I Do
permalink: /what-else-can-i-do/replaceable-aliases.html
---

<div id="bpmbook" class="bpmbook" style="direction:ltr;">
<div class="topic_user_field">
<div id="U0">

<div class="alert alert-info" role="alert"><b>Note:</b> Prior to mPDF 6.0 you could include <span class="parameter">{nb​}</span> and <span class="parameter">{nbpg​}</span> anywhere in the text of the document, including headers/footers.

In mPDF v6.0+ these will only be replaced when used in headers/footers.</div>
<p>There are several placemarkers you can include, which will be replaced when the PDF file is ouput:</p>
<p class="manual_param_dt"><span class="parameter">{nb​}

</span></p>
<p class="manual_param_dd">Will be replaced by the total number of pages in the document. This disregards any changes you make to page numbering with <a href="{{ "/reference/mpdf-functions/addpage.html" | prepend: site.baseurl }}">AddPage()</a> or &lt;<a href="{{ "/reference/html-control-tags/pagebreak.html" | prepend: site.baseurl }}">pagebreak</a>&gt; and will always return the actual number of pages in the PDF document. You can change this alias (in case you wish to use the text "{nb​}" in your document) using <a href="{{ "/reference/mpdf-functions/aliasnbpages.html" | prepend: site.baseurl }}">AliasNbPages()</a>. The alias is case-sensitive.</p>
<p class="manual_param_dt"><span class="parameter">{nbpg​}</span><span class="parameter">&nbsp;</span></p>
<p class="manual_param_dd">Will be replaced by the total number of pages in the document or page group. If you have reset the page numbering with <a href="{{ "/reference/mpdf-functions/addpage.html" | prepend: site.baseurl }}">AddPage()</a> or &lt;<a href="{{ "/reference/html-control-tags/pagebreak.html" | prepend: site.baseurl }}">pagebreak</a>&gt; the total number of pages in the current page group will be used (up to where the numbering is reset) rather the total number of pages in the whole document. You can change this alias (in case you wish to use the text "{nbpg​}" in your document) using <a href="{{ "/reference/mpdf-functions/aliasnbpages.html" | prepend: site.baseurl }}">AliasNbPageGroups()</a>. The alias is case-sensitive. The numbering style can be changed using <a href="{{ "/reference/mpdf-functions/addpage.html" | prepend: site.baseurl }}">AddPage()</a> or &lt;<a href="{{ "/reference/html-control-tags/pagebreak.html" | prepend: site.baseurl }}">pagebreak</a>&gt;.</p>
<p class="manual_param_dt"><span class="parameter">{PAGENO}</span></p>
<p class="manual_param_dd">Will be replaced by the Page number - but <b>only</b> in headers/footers. If you have reset the page numbering with <a href="{{ "/reference/mpdf-functions/addpage.html" | prepend: site.baseurl }}">AddPage()</a> or &lt;<a href="{{ "/reference/html-control-tags/pagebreak.html" | prepend: site.baseurl }}">pagebreak</a>&gt; the calculated document page number will be used rather the physical PDF document page number. You cannot change this alias. The alias is case-sensitive. The numbering style can be changed using <a href="{{ "/reference/mpdf-functions/addpage.html" | prepend: site.baseurl }}">AddPage()</a> or &lt;<a href="{{ "/reference/html-control-tags/pagebreak.html" | prepend: site.baseurl }}">pagebreak</a>&gt;.</p>
<p class="manual_param_dt"><span class="parameter">{DATE d/m/Y}</span></p>
<p class="manual_param_dd">Will be replaced by today's date - but <b>only</b> in headers/footers. The alias is case-sensitive. The date format can be defined using any of the values in the PHP function <a href="http://www.php.net/manual/en/function.date.php">date()</a>. There must be a space after <span class="parameter">{DATE</span> 

Example: <span class="parameter">{DATE j-m-Y H:m}</span></p>
<p class="manual_param_dt"><span class="parameter">{colsum} {colsum<i><b>N</b></i>}

</span></p>
<p class="manual_param_dd">Place in cell inside a table footer i.e. &lt;tfoot&gt;&lt;td&gt;. The total of values in the corresponding column will be output at the bottom of every page, and the end of the tale. Default output is an integer. An optional integer <i><b>N</b></i> after colsum will specify a fixed number of decimal places. (mPDF &gt;= 5.4)</p>
<p class="manual_param_dt"><span class="parameter">{iteration&nbsp;<b>varname</b>}

</span></p>
<p class="manual_param_dd">Place in cell inside table header i.e. &lt;thead&gt;&lt;td&gt;. You can use any alphanumeric string as a unique varname. (When processed by mPDF it will be replaced by "__varname_" to avoid collision with an mPDF internal variable. The length of the alhanumeric string will determine the length of the placeholder used to space the text i.e. if your counter will reach 1000 you should use a string of at least 4-5 characters in length.</p>
<h2>See Also</h2>
<ul>
<li class="manual_boxlist"><a href="{{ "/reference/mpdf-variables/pagenumprefix.html" | prepend: site.baseurl }}">pagenumPrefix</a> - Specify text to precede page numbers generated by {PAGENO}</li>
<li class="manual_boxlist"><a href="{{ "/reference/mpdf-variables/pagenumsuffix.html" | prepend: site.baseurl }}">pagenumSuffix</a> - Specify text to follow page numbers generated by {PAGENO}</li>
<li class="manual_boxlist"><a href="{{ "/reference/mpdf-variables/nbpgprefix.html" | prepend: site.baseurl }}">nbpgPrefix</a> - Specify text to precede page total generated by {nbpg }</li>
<li class="manual_boxlist"><a href="{{ "/reference/mpdf-variables/nbpgsuffix.html" | prepend: site.baseurl }}">nbpgSuffix</a> - Specify text to follow page numbers generated by {nbpg }</li>
<li class="manual_boxlist"><a href="{{ "/paging/page-numbering.html" | prepend: site.baseurl }}">Page numbering</a> - </li>
<li class="manual_boxlist"><a href="{{ "/reference/mpdf-variables/aliasnbpg.html" | prepend: site.baseurl }}">aliasNbPg</a> - Specify the text to be replaced by the document page total</li>
<li class="manual_boxlist"><a href="{{ "/reference/mpdf-variables/aliasnbpggp.html" | prepend: site.baseurl }}">aliasNbPgGp</a> - Specify the text to be replaced by the group page total</li>
</ul>
</div>
</div>
