---
layout: post
title: Medicare, yet another bad implementation of form validation
tags:
- idiots
- medicare
---
<p>I&#8217;m in the process of supplying my bank details to <a href="http://www.humanservices.gov.au/customer/information/welcome-medicare-customers-website?utm_id=9">Medicare</a>. Their form validation process is common but that doesn&#8217;t excuse the fact is sucks.</p>

<h2>Name of account holder</h2>

<p>Limited to 30 characters. Are you kidding me? Have you heard of joint accounts?</p>

<h2>Account Numbers</h2>

<p>First time I hit the submit button I get the following error message:</p>

<ul><li>Spaces, blanks and symbols are not valid.</li>
</ul><p>Firstly, if you must insist that the account number does not contain any symbols then tell me only that. I do not have spaces or blank in the account number.</p>

<p>Secondly, do allow standard account number delimiters such as space, - and /. I&#8217;m sure must people will copy and paste their bank account details from their bank&#8217;s website which tend to show account numbers in 999-999 or 999&#160;999 format.</p>

<p>Need help with the code?</p>

<pre><code>accountNumber = accountNumber.Replace("-", "").Replace(" ", "").Replace("/", "")
</code></pre>

<p>Now that wasn&#8217;t hard was it?</p>

<h2>Name of account holder, again</h2>

<p>So I removed the - from the account number and hit submit again. What? Another validation error. Why didn&#8217;t you tell me that the first time I hit submit? This time the error message is:</p>

<ul><li>The symbol you have supplied in the &#8216;Name of account holder&#8217; field is invalid. The only valid symbols to be applied are - (hyphen) and &#8217; (apostrophe).</li>
</ul><p>Again, have you heard of joint accounts? Do you want me to type <strong>and</strong> instead of <strong>&amp;</strong>? Just as well you&#8217;ve allowed enough space in that field, not!</p>
