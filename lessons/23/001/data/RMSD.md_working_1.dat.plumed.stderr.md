Stderr for source:  RMSD.md_working_1.dat   
Download: [zipped raw stdout](RMSD.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](RMSD.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONSTANT with label v : cannot understand the following words from the input line : NCOLS=12, NROWS=2
[fv-az1315-757:08340] *** Process received signal ***
[fv-az1315-757:08340] Signal: Aborted (6)
[fv-az1315-757:08340] Signal code:  (-6)
[fv-az1315-757:08340] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2edc245330]
[fv-az1315-757:08340] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f2edc29eb2c]
[fv-az1315-757:08340] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f2edc24527e]
[fv-az1315-757:08340] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f2edc2288ff]
[fv-az1315-757:08340] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2edc6a5ff5]
[fv-az1315-757:08340] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2edc6bb0da]
[fv-az1315-757:08340] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2edc6a5a55]
[fv-az1315-757:08340] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2edc6a5a6f]
[fv-az1315-757:08340] [ 8] plumed(+0x13209)[0x55d48adf7209]
[fv-az1315-757:08340] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f2edc22a1ca]
[fv-az1315-757:08340] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f2edc22a28b]
[fv-az1315-757:08340] [11] plumed(+0x134a5)[0x55d48adf74a5]
[fv-az1315-757:08340] *** End of error message ***
</pre>
{% endraw %}
