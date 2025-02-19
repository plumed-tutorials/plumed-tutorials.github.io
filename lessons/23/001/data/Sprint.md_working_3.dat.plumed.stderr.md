Stderr for source:  Sprint.md_working_3.dat   
Download: [zipped raw stdout](Sprint.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action SPRINT with label ss : keyword MATRIX is compulsory for this action
[fv-az1755-505:06161] *** Process received signal ***
[fv-az1755-505:06161] Signal: Aborted (6)
[fv-az1755-505:06161] Signal code:  (-6)
[fv-az1755-505:06161] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f127dc45330]
[fv-az1755-505:06161] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f127dc9eb2c]
[fv-az1755-505:06161] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f127dc4527e]
[fv-az1755-505:06161] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f127dc288ff]
[fv-az1755-505:06161] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f127e0a5ff5]
[fv-az1755-505:06161] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f127e0bb0da]
[fv-az1755-505:06161] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f127e0a5a55]
[fv-az1755-505:06161] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f127e0a5a6f]
[fv-az1755-505:06161] [ 8] plumed(+0x13209)[0x55af7392e209]
[fv-az1755-505:06161] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f127dc2a1ca]
[fv-az1755-505:06161] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f127dc2a28b]
[fv-az1755-505:06161] [11] plumed(+0x134a5)[0x55af7392e4a5]
[fv-az1755-505:06161] *** End of error message ***
</pre>
{% endraw %}
