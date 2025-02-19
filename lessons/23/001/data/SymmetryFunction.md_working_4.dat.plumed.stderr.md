Stderr for source:  SymmetryFunction.md_working_4.dat   
Download: [zipped raw stdout](SymmetryFunction.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](SymmetryFunction.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label c1 : No atoms have been read in
[fv-az1755-505:07344] *** Process received signal ***
[fv-az1755-505:07344] Signal: Aborted (6)
[fv-az1755-505:07344] Signal code:  (-6)
[fv-az1755-505:07344] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f826c445330]
[fv-az1755-505:07344] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f826c49eb2c]
[fv-az1755-505:07344] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f826c44527e]
[fv-az1755-505:07344] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f826c4288ff]
[fv-az1755-505:07344] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f826c8a5ff5]
[fv-az1755-505:07344] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f826c8bb0da]
[fv-az1755-505:07344] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f826c8a5a55]
[fv-az1755-505:07344] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f826c8a5a6f]
[fv-az1755-505:07344] [ 8] plumed(+0x13209)[0x55565a4b7209]
[fv-az1755-505:07344] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f826c42a1ca]
[fv-az1755-505:07344] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f826c42a28b]
[fv-az1755-505:07344] [11] plumed(+0x134a5)[0x55565a4b74a5]
[fv-az1755-505:07344] *** End of error message ***
</pre>
{% endraw %}
