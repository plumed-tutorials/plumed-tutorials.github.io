<div class="modal-header">
<h2>--enable-molfile-plugins option</h2>
</div>
<div class="modal-body">
<p>The <code>--enable-molfile-plugins</code> flag ensures that PLUMED is linked with VMD plugins. If PLUMED is configured with this flag you will thus be able to
read all the trajectory formats that VMD can read with plumed driver.

To be clear the PLUMED source code contains VMD plugins for a small number of trajectory formats (dcd, gromacs files, pdb and amber files) so you will most likely not need this flag.
You will only need it you would like to be able to read in some a particularly exotic trajectory file type.  If you do need to work with these other types of file can get the molfile plugins by
downloading the SOURCE of VMD. This sourcecode contains
a plugins directory. You will need to adapt the build.sh script within this directory and then compile the code within the directory. Once this process is completed
you should get the molfile plugins compiled as a static library called <code>libmolfile_plugin.a</code>. The location of this library, the <code>libmolfile_plugin.h</code> and
the <code>molfile_plugin.h</code> include files will then need to be passed to configure using a command similar to:</p>
<pre class="fragment">
&gt; ./configure LDFLAGS="-L/pathtovmdplugins/ARCH/molfile" CPPFLAGS="-I/pathtovmdplugins/include -I/pathtovmdplugins/ARCH/molfile"
</pre>
<p>It may also be necessary to add the location of the TCL interpreter to the <code>LDFLAGS</code> using a command such as:</p>
<pre class="fragment">
&gt; ./configure LDFLAGS="-ltcl8.5 -L/mypathtotcl -L/pathtovmdplugins/ARCH/molfile" \
         CPPFLAGS="-I/pathtovmdplugins/include -I/pathtovmdplugins/ARCH/molfile"
</pre>
<p>To be clear, however, some of the molfile plugin sourcecode is included in PLUMED and you can thus use some of the most common types of trajectory file even if you do not download VMD on your machine.</p>
</div>
