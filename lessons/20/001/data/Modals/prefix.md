<div class="modal-header">
<h2>--prefix option</h2>
</div>
<div class="modal-body">
<p>The <code>--prefix</code> environmental variable controls the location in which PLUMED is installed when the <code>make install</code> command is run. By default
PLUMED is installed in <code>/usr/local/</code> and you will thus have to run <code>make install</code> with super-user permissions i.e. using <code>sudo make install</code>.
You can, however, specify the location in which to install PLUMED by using the <code>--prefix</code> environmental variable. For example, to install PLUMED in <code>$(HOME)/opt</code>
you would configure using:</p>
<pre class="fragment">
&gt; ./configure --prefix=$HOME/opt
</pre>
<p>Upon install, the executable would then be copied to <code>$(HOME)/opt/bin</code>, the libraries to <code>$(HOME)/opt/lib</code>, the include files to <code>$(HOME)/opt/include</code>, and the
documentation to <code>$(HOME)/opt/shared/doc/plumed</code>. In addition, a directory called <code>$(HOME)/opt/lib/plumed</code> will be created containing files such as the
patch files and the object files (for static patches). Advanced users can further customise the install directories using
using standard autoconf directories (e.g. <code>./configure --bindir=/usr/bin64</code>). Further information on these options can be obtained by running the command:</p>
<pre class="fragment">
&gt; ./configure --help
</pre>
</div>
