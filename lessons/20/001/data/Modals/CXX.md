<div class="modal-header">
<h2>CXX Environment Variable</h2>
</div>
<div class="modal-body">
<p>The <code>CXX</code> environmental variable controls the c++ compiler that will be used to build PLUMED. If you would like to compile PLUMED with
MPI the compiler that is passed to this variable should be an MPI compiler. Consequently, if you work on a machine where <code>CXX</code> is
set to a serial compiler and <code>MPICXX</code> is set to a MPI compiler you should configure PLUMED using the command:</p>
<pre class="fragment">
&gt; ./configure CXX="$MPICXX"
</pre>
<p>If the <code>CXX</code> environmental variable is not set equal to an MPI compiler then MPI is <b>not enabled</b>. This behaviour differs
from what some other configure scripts do. To be clear, when PLUMED is complied variables such as <code>MPICXX</code> are completely ignored.</p>

<p> PLUMED does search for MPI and non-MPI compilers with common names even if the <code>CXX</code> environmental variable is not set.
The search is only a few of the possible compiler names, however. If your compiler is named "g++-mp-4.8" you will need to explicitly specify this
by using the <code>CXX</code> environmental variable.</p>

<p>PLUMED 2.4 requires a compiler that supports C++11. The following compilers (or later versions) should be sufficient:</p>
<ul>
<li> gcc 4.8.1</li>
<li> clang 3.3</li>
<li> intel 15</li>
</ul>

<p>The <code>./configure</code> script will check whether or not your compiler supports C++11.
Some compilers that do not declare full C++11 support have several C++11 features enabled and can thus be used
to compile PLUMED (this is the case for the intel 15 compiler for instance).</p>

<p>If you see a warning about C++11 support during <code>./configure</code> it is then important to check that
PLUMED compiles correctly. The best way to do this to to execute the regtests using the command <code>make regtest</code>.</p>

<p>We regularly test a number of compilers on <a href="https://github.com/plumed/plumed2/actions">GitHub Actions</a>. These compilers should thus always compile PLUMED correctly.</p>
</div>
