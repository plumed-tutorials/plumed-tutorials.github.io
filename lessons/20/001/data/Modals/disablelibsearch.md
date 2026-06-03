<div class="modal-header">
<h2>--disable-libsearch option</h2>
</div>
<div class="modal-body">
<p> By default PLUMED uses a two step procedure when searching for a library. If, for example, PLUMED is searching for the xdr library it will first try to link a routine from this library
without adding any additional flags. If this command fails the additional flag, "-lxdrfile" is then added to the <code>LIBS</code> envrionmental variable and the test is run again.
The <code>--disable-libsearch</code> command ensures that this second step in the search is ommitted. Consequently, when this option is used only those libraries that are
explicitly passed through the <code>LIBS</code> environmental variable are linked. For example if the command:</p>
<pre class="fragment">
&gt; ./configure --disable-libsearch LIBS=-lxdrfile
</pre>
<p>is used then only xdrfile is linked. The BLAS and LAPACK libraries are not be linked and the internal versions of these libraries are used. This option is
useful when installing PLUMED within package managers such as MacPorts as it ensures that only the desired libraries are linked. In other words, no spurious
dependencies are introduced. The only exception to this rule is <code>-ldl</code>, which is a system library on Linux.</p>
</div>
