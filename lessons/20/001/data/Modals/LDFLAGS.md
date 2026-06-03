<div class="modal-header">
<h2>LDFLAGS Environment Variable</h2>
</div>
<div class="modal-body">
<p>The main purpose of the <code>configure</code> script is to locate all the libraries that are required to build PLUMED. PLUMED will by default check for these libraries in
certain standard places. If the libraries are not in these standard places, however, then you will need to provide information the configure script on where to find them by using the
<code>LDFLAGS</code>, <code>CPPFLAGS</code> and <code>LIBS</code> flags. If suitable libraries are not found during the execution of the <code>configure</code> script then these
features will be disabled. You should thus carefully check the log that is output by the <code>configure</code> command to ensure that all the libraries you require have been found.
</p>

<p>The <code>LDFLAGS</code> variable tells the <code>configure</code> script the names of directories in which the libraries can be found. If the xdrfile libraries are
in /opt/local (i.e. where MacPorts puts them) then you would use the command below to tell PLUMED where to find them.</p>
<pre class="fragment">
&gt; ./configure LDFLAGS=-L/opt/local/lib CPPFLAGS=-I/opt/local/include
</pre>
</div>
