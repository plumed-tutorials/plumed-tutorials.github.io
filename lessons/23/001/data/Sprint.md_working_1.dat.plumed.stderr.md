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
[fv-az1315-757:06201] *** Process received signal ***
[fv-az1315-757:06201] Signal: Aborted (6)
[fv-az1315-757:06201] Signal code:  (-6)
[fv-az1315-757:06201] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fe202445330]
[fv-az1315-757:06201] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fe20249eb2c]
[fv-az1315-757:06201] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fe20244527e]
[fv-az1315-757:06201] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fe2024288ff]
[fv-az1315-757:06201] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fe2028a5ff5]
[fv-az1315-757:06201] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fe2028bb0da]
[fv-az1315-757:06201] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fe2028a5a55]
[fv-az1315-757:06201] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fe2028a5a6f]
[fv-az1315-757:06201] [ 8] plumed(+0x13209)[0x561435bd8209]
[fv-az1315-757:06201] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fe20242a1ca]
[fv-az1315-757:06201] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fe20242a28b]
[fv-az1315-757:06201] [11] plumed(+0x134a5)[0x561435bd84a5]
[fv-az1315-757:06201] *** End of error message ***
</pre>
{% endraw %}
