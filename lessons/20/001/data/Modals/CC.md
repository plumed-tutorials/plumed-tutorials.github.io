<div class="modal-header">
<h2>CC Environment Variable</h2>
</div>
<div class="modal-body">
<p>The <code>CC</code> environmental variable controls the c compiler that is used in the building of PLUMED. The majority of PLUMED is built using the c++ compiler that is
specified using the <code>CXX</code> environmental variable. A C compiler must still be specified nonetheless as the wrapper that is used to interface PLUMED with the MD codes is
written in C.</p>

<p>PLUMED does seach for MPI and non-MPI compilers with a number of standard names even if the <code>CC</code> environmental variable is not set.
Only a few of the possible compiler name are searched, however. If your compiler is named "gcc-mp-4.8" you will need to explicitly specify this
by using the <code>CC</code> environmental variable.</p>
</div>

