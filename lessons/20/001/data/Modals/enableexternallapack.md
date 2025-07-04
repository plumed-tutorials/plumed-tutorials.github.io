<div class="modal-header">
<h2>--enable-external-lapack option</h2>
</div>
<div class="modal-body">
<p>PLUMED uses the blas and lapack libraries to perform linear algebra and the source code for these two libraries is included. <b>For production calculations,
however, we would strongly encourage you to link to libraries containing suitably-optimized versions of these libraries and to not rely on the versions of blas and 
lapack that are included within PLUMED.</b></p>

<p>You can use a specific version of BLAS or LAPACK availble to <code>configure</code> using the <code>LDFLAGS</code> and <code>LIBS</code> environment variables as shown
below:</p>
<pre class="fragment">
&gt; ./configure LDFLAGS=-L/path/to/blas/lib LIBS=-lnameoflib
</pre>
<p>The <code>configure</code> script will check if the functions that are required from this library are found in the usual way (i.e. by checking without additional
-llapack and -lblas options added to the <code>LIBS</code> environmental variable first and then with these options added to these variabels). Furthermore, two checks
for any required functions are performed. In the first, of these checks the name of the functions are searched for. If this search is unsucessful then a
search for a version of the function with a final underscore added to the name is then performed. If no functions are found in these two steps then the versions of
blas and lapack that are internal to PLUMED are used.</p>

<p>If you prefer to disable the search for external versions of blas and lapack because, for example, the system libraries have problems you can configure using the
command</p>
<pre class="fragment">
&gt; ./configure --disable-external-blas
</pre>
<p>You can also only disable the external LAPACK. In other words, you can use the internal version of LAPACK with an external version of BLAS by using the command:</p>
<pre class="fragment">
&gt; ./configure --disable-external-lapack
</pre>
<p> Using this option is quite sensible as one can typically only heavily optimize the BLAS library. Using the internal LAPACK with an external version of BLAS
should, therefore, not slow your calculations down significantly. You could thus use this option on systems where the native LAPACK libraries have problems</p>
<p>We have had numerous emails from users who have struggled to link PLUMED with BLAS and LAPACK. We have even struggled with this ourselves. From these experiences, however,
some sensible steps that you can use to check whether or not the configuration has been setup correctly have emerged. If you are having difficulties you should
Open the Makefile.conf file that is output after <code>configure</code> has finished running. Check that the flags necessary for loading the
BLAS and LAPACK libraries are included in the the <code>DYNAMIC_LIB</code> variable that is contained in this file. If BLAS and LAPACK have been detected correctly
-llapack, -lblas and, in some cases, -lgfortran will appear after this variable. On some machines full path specification with -L may be necessary in place of -llapack,
-lblas anmd -gfortran. Depending on system configuration, your libraries may even not be called -llapack and -lblas. You will thus have to ensure that the correct names
for these libraries are used. If the correct libraries appear after <code>DYNAMIC_LIB</code> in the Makefile.conf file and if PLUMED still doesn't compile some other things
to try include:</p>
<ul>
<li> If the linker complains and suggests recompiling LAPACK with -fPIC, it means that you have static LAPACK libraries. Either install dynamic LAPACK libraries
or switch to static compilation of PLUMED by unsetting the SOEXT variable in the configuration file.</li>
<li> If the linker complains about other missing functions (typically functions with names that start with the prefix "for_") you need to link some additional Fortran libraries.
 PLUMED is written in C++ and C++ linkers often do not include Fortran libraries by default, which is unfortunate as the fortran libraries are required for LAPACK and BLAS to
 work. If you encounter this problem we woudl recommend checking the documentation for your compiler.</li>
<li> If the linker complains that dsyevr_ cannot be found, try adding the flag -DF77_NO_UNDERSCORE to <code>CPPFLAGS</code>. "./configure" will automatically try this solution but maybe you
 have more luck.</li>
</ul>
</div>
