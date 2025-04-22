Stderr for source:  Clusters.md_working_3.dat   
Download: [zipped raw stdout](Clusters.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Clusters.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label cm : No atoms have been read in
[fv-az1315-757:08309] *** Process received signal ***
[fv-az1315-757:08309] Signal: Aborted (6)
[fv-az1315-757:08309] Signal code:  (-6)
[fv-az1315-757:08309] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4ece845330]
[fv-az1315-757:08309] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f4ece89eb2c]
[fv-az1315-757:08309] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f4ece84527e]
[fv-az1315-757:08309] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f4ece8288ff]
[fv-az1315-757:08309] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4ececa5ff5]
[fv-az1315-757:08309] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4ececbb0da]
[fv-az1315-757:08309] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4ececa5a55]
[fv-az1315-757:08309] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4ececa5a6f]
[fv-az1315-757:08309] [ 8] plumed(+0x13209)[0x55aa28d05209]
[fv-az1315-757:08309] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f4ece82a1ca]
[fv-az1315-757:08309] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f4ece82a28b]
[fv-az1315-757:08309] [11] plumed(+0x134a5)[0x55aa28d054a5]
[fv-az1315-757:08309] *** End of error message ***
</pre>
{% endraw %}
