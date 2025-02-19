Stderr for source:  Sprint.md_working_1.dat   
Download: [zipped raw stdout](Sprint.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action SPRINT with label s1 : keyword MATRIX is compulsory for this action
[fv-az1755-505:06094] *** Process received signal ***
[fv-az1755-505:06094] Signal: Aborted (6)
[fv-az1755-505:06094] Signal code:  (-6)
[fv-az1755-505:06094] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6aa0845330]
[fv-az1755-505:06094] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6aa089eb2c]
[fv-az1755-505:06094] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6aa084527e]
[fv-az1755-505:06094] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6aa08288ff]
[fv-az1755-505:06094] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f6aa0ca5ff5]
[fv-az1755-505:06094] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f6aa0cbb0da]
[fv-az1755-505:06094] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f6aa0ca5a55]
[fv-az1755-505:06094] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f6aa0ca5a6f]
[fv-az1755-505:06094] [ 8] plumed(+0x13209)[0x564d8b15f209]
[fv-az1755-505:06094] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6aa082a1ca]
[fv-az1755-505:06094] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6aa082a28b]
[fv-az1755-505:06094] [11] plumed(+0x134a5)[0x564d8b15f4a5]
[fv-az1755-505:06094] *** End of error message ***
</pre>
{% endraw %}
