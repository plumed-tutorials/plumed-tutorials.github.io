Stderr for source:  contactMatrix.md_working_4.dat   
Download: [zipped raw stdout](contactMatrix.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](contactMatrix.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label c1 : No atoms have been read in
[fv-az1755-505:05761] *** Process received signal ***
[fv-az1755-505:05761] Signal: Aborted (6)
[fv-az1755-505:05761] Signal code:  (-6)
[fv-az1755-505:05761] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc7aa645330]
[fv-az1755-505:05761] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc7aa69eb2c]
[fv-az1755-505:05761] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc7aa64527e]
[fv-az1755-505:05761] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc7aa6288ff]
[fv-az1755-505:05761] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc7aaaa5ff5]
[fv-az1755-505:05761] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc7aaabb0da]
[fv-az1755-505:05761] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc7aaaa5a55]
[fv-az1755-505:05761] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc7aaaa5a6f]
[fv-az1755-505:05761] [ 8] plumed(+0x13209)[0x55b16a020209]
[fv-az1755-505:05761] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc7aa62a1ca]
[fv-az1755-505:05761] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc7aa62a28b]
[fv-az1755-505:05761] [11] plumed(+0x134a5)[0x55b16a0204a5]
[fv-az1755-505:05761] *** End of error message ***
</pre>
{% endraw %}
