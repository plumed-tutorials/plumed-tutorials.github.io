<div class="modal-header">
<h2>LIBS Environment Variable</h2>
</div>
<div class="modal-body">
<p>The main purpose of the <code>configure</code> script is to locate all the libraries that are required to build PLUMED. PLUMED will by default check for these libraries in
certain standard places. If the libraries are not in these standard places, however, then you will need to provide information the configure script on where to find them by using the
<code>LDFLAGS</code>, <code>CPPFLAGS</code> and <code>LIBS</code> flags. If suitable libraries are not found during the execution of the <code>configure</code> script then these
features will be disabled. You should thus carefully check the log that is output by the <code>configure</code> command to ensure that all the libraries you require have been found.</p>

<p>You are required to set the <code>LIBS</code> environmental variable if your libraries have non-standard names. If, for example, your xdrfile library is
called /opt/local/lib/libmyxdrfile.so you can link it using:</p>
<pre class="fragment">
&gt; ./configure LDFLAGS=-L/opt/local/lib CPPFLAGS=-I/opt/local/include LIBS=-lmyxdrfile
</pre>
<p> This command works because PLUMED first tries to link a routine from the xdr library without adding any additional flag. If and only if this command fails the additional flag,
"-lxdrfile" is added to the <code>LIBS</code> envrionmental variable. Consequently, if the user has specified the name of the xdr library using the <code>LIBS</code> environmental
flag this custom version will be used in place of the standardly-named "-lxdrfile" library.</p>

<p>If, for any reason, you would like more control over the libraries that are used to build PLUMED you can use the
<a onclick='openModal("disablelibsearch")'>--disable-libsearch</a> option.</p>
</div>
