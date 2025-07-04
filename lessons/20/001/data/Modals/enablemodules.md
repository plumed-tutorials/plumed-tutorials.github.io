<div class="modal-header">
<h2>--enable-modules option</h2>
</div>
<div class="modal-body">
<p>PLUMED is made up of modules. Some of these are used more frequently than others and so the ones that we believe that are used
less often are disabled in a default compilation. If you configure using the option <code>--enable-modules=all</code> then PLUMED will compile
all these modules. This option would be recommended if you are compiling the code for multiple users and if you are not sure of those
users need.</p>

<p>If, however, you are compiling the code for yourself only then it may be better to only compile those modules you specifically need.
If you would like to compile with the core modules and the dimred and ves modules you could use the command <code>--enable-modules=dimred:ves</code>.</p>
</div>
