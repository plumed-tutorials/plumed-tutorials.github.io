Stderr for source:  Volumes.md_working_3.dat   
Download: [zipped raw stdout](Volumes.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Volumes.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1755-505:07163] *** Process received signal ***
[fv-az1755-505:07163] Signal: Aborted (6)
[fv-az1755-505:07163] Signal code:  (-6)
[fv-az1755-505:07163] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fedc4c45330]
[fv-az1755-505:07163] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fedc4c9eb2c]
[fv-az1755-505:07163] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fedc4c4527e]
[fv-az1755-505:07163] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fedc4c288ff]
[fv-az1755-505:07163] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fedc50a5ff5]
[fv-az1755-505:07163] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fedc50bb0da]
[fv-az1755-505:07163] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fedc50a5a55]
[fv-az1755-505:07163] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fedc50a5a6f]
[fv-az1755-505:07163] [ 8] plumed(+0x13209)[0x560f95187209]
[fv-az1755-505:07163] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fedc4c2a1ca]
[fv-az1755-505:07163] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fedc4c2a28b]
[fv-az1755-505:07163] [11] plumed(+0x134a5)[0x560f951874a5]
[fv-az1755-505:07163] *** End of error message ***
</pre>
{% endraw %}
