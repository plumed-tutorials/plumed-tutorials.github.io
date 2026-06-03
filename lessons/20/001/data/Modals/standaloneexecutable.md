<div class="modal-header">
<h2>--standalone-executable option</h2>
</div>
<div class="modal-body" id="--standalone-executable-content">
<p>The PLUMED executable which relies on the resource files present in the compilation directory.
During installation these files are copied to <code>$(prefix)/lib/plumed</code> and the compilation directory can therefore be deleted.
If you do not install PLUMED, however, you need to ensure that none of the files in <code>src/lib/plumed</code> are not
moved or renamed.</p>
<p>The path to the PLUMED root directory is hard coded in the plumed executable as can be verified by using the command:</p>
<pre class="fragment">
&gt; plumed info --root
</pre>
<p>If you try to run a non-installed plumed executable and if the <code>src/lib/plumed</code>
directory is not in place PLUMED will throw an error as shown below:</p>
<pre class="fragment">
&gt; plumed help
ERROR: I cannot find /xxx/yyy/patches directory
</pre>
<p>You can force plumed to ignore this error and to run anyway by using the option --standalone-executable as shown below</p>
<pre class="fragment">
&gt; plumed --standalone-executable help
</pre>
<p>Many features are not be available if you run in this way. This is currently the only way to use the PLUMED static executable on Windows, however.</p>
</div>
