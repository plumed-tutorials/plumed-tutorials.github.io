Stderr for source:  Steinhardt.md_working_13.dat   
Download: [zipped raw stdout](Steinhardt.md_working_13.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Steinhardt.md_working_13.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cmat : No atoms have been read in
[fv-az1755-505:06578] *** Process received signal ***
[fv-az1755-505:06578] Signal: Aborted (6)
[fv-az1755-505:06578] Signal code:  (-6)
[fv-az1755-505:06578] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fafca845330]
[fv-az1755-505:06578] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fafca89eb2c]
[fv-az1755-505:06578] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fafca84527e]
[fv-az1755-505:06578] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fafca8288ff]
[fv-az1755-505:06578] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fafcaca5ff5]
[fv-az1755-505:06578] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fafcacbb0da]
[fv-az1755-505:06578] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fafcaca5a55]
[fv-az1755-505:06578] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fafcaca5a6f]
[fv-az1755-505:06578] [ 8] plumed(+0x13209)[0x55f9004ca209]
[fv-az1755-505:06578] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fafca82a1ca]
[fv-az1755-505:06578] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fafca82a28b]
[fv-az1755-505:06578] [11] plumed(+0x134a5)[0x55f9004ca4a5]
[fv-az1755-505:06578] *** End of error message ***
</pre>
{% endraw %}
