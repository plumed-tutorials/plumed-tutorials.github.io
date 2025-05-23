<div class="modal-header">
<h2>--enable-mpi option</h2>
</div>
<div class="modal-body">
<p>An MPI search is enabled by default and so the <code>--enable-mpi</code> flag is not strictly necessary. It is important to note, however, that
if MPI search is enabled then compilers named "mpic++" and "mpicxx" are searched for first, which may be confusing as many
other programs behave in a different way.</p>

<p>When PLUMED is configured with MPI enabled (as it is by default) autoconf checks if a code containing MPI calls can be compiled using the specified
compiler. If this code can be compiled then MPI is enabled. If it cannot then MPI will be disabled. If you thus specify a non-MPI compiler using the
<code>CXX</code> environmental variable there is no reason to also specify <code>--disable-mpi</code>. The <code>--disable-mpi</code> command is only
necessary if you specifed an MPI compiler to the <code>CXX</code> environmental variable but you don't want PLUMED to be compiled with MPI support.
In other words, the correct way to enable MPI is to pass <code>./configure</code> an MPI C++ compiler by using the <code>CXX</code> environmental variable.
If this is done you can then treat the MPI library in the same way that all the other libraries that PLUMED tries to link by default.</p>
</div>

