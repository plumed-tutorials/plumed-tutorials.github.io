<div class="modal-header">
<h2>--enable-asmjit option</h2>
</div>
<div class="modal-body">
<p>If there are a lot of <a class="el" href="_c_u_s_t_o_m.html">CUSTOM</a> functions or <a class="el" href="switchingfunction.html">switching functions</a>
in your input then you may be heavilty using the lepton library that is included in PLUMED.
The calls to this library can be made significantly faster by using a
<a href="https://github.com/asmjit/asmjit.git">just-in-time compiler</a>. Furthermore,
as of PLUMED 2.6, ASMJIT is embedded in PLUMED. To enable it you use the <code>--enable-asmjit</code> flag in configure</p>

<p>If, for any reason, you want to disable ASMJIT at runtime you can do by setting the <code>PLUMED_USE_ASMJIT</code> environment variable as shown below:</p>

<pre class="fragment">export PLUMED_USE_ASMJIT=no</pre>
</div> 
