Stderr for source:  Clusters.md_working_2.dat   
Download: [zipped raw stdout](Clusters.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cm : No atoms have been read in
[fv-az1755-505:08178] *** Process received signal ***
[fv-az1755-505:08178] Signal: Aborted (6)
[fv-az1755-505:08178] Signal code:  (-6)
[fv-az1755-505:08178] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2f12a45330]
[fv-az1755-505:08178] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2f12a9eb2c]
[fv-az1755-505:08178] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2f12a4527e]
[fv-az1755-505:08178] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2f12a288ff]
[fv-az1755-505:08178] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2f12ea5ff5]
[fv-az1755-505:08178] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2f12ebb0da]
[fv-az1755-505:08178] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2f12ea5a55]
[fv-az1755-505:08178] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2f12ea5a6f]
[fv-az1755-505:08178] [ 8] plumed(+0x13209)[0x5652b7a9b209]
[fv-az1755-505:08178] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2f12a2a1ca]
[fv-az1755-505:08178] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2f12a2a28b]
[fv-az1755-505:08178] [11] plumed(+0x134a5)[0x5652b7a9b4a5]
[fv-az1755-505:08178] *** End of error message ***
</pre>
{% endraw %}
