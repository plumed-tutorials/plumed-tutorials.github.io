<div class="modal-header">
<h2>--enable-rpath option</h2>
</div>
<div class="modal-body">
<p>On OSX it is common practice to hard code the full path to all the libraries that were used during the compilation within the compiled library.
The consequence of this is that, if an executable is linked to shared library, then that executable can find all the libraries which are required to run the
functions within the linked library. The operating system knows where to search for the libraries that were used when the linked libraries was compiled as the
path to these libraries is stored within the linked library. When the <code>libplumed.dylib</code> library is compiled on a system running OSX there is thus no
problem in finding external blas or lapack libraries at later times.</p>

<p>On Linux it is not common practice to hard code paths into libraries in the manner described above. Consequently, if you use the
<code>LDFLAGS</code> option to specify the path to a library at compile time. In other words, if you configure PLUMED using the command:</p>
<pre class="fragment">
&gt; ./configure LDFLAGS="-L/opt/local/lib"
</pre>
<p>Then the libraries in /opt/local/lib may not be found at runtime. One visible symptom of this problem is that <code>src/lib/plumed-shared</code> will
not be linked correctly. The consequence of this is that it is not possible to dynamically link PLUMED with an MD code later, which is only a problem if you
would like to link PLUMED dynamically.</p>

<p>You can resolve this issue by using the command below when configuring PLUMED:</p>
<pre class="fragment">
&gt; ./configure LIBRARY_PATH=/path --enable-rpath
</pre>
<p>This command will hard code the paths defined in <code>LIBRARY_PATH</code> into the PLUMED library and is equivalent to the command:</p>
<pre class="fragment">
&gt; ./configure LDFLAGS="-L/path -Wl,-rpath,/path"
</pre>
</div>
